# 🧠 Lesson 04 — Harmony Patches & Hooks

## 🔍 Concept

A mod does not modify the game directly.
It connects to it by intercepting existing methods.

This is called a **hook**.

> When a game method is triggered, your mod can inject logic before or after it.

---

## 🧩 Harmony (Core Tool)

We use **Harmony** to patch methods at runtime.

It allows:

* Executing code **before** a method
* Executing code **after** a method
* Blocking a method completely
* Modifying behavior dynamically

---

## ⚙️ Patch Structure

```csharp
[HarmonyPatch(typeof(ClassName), "MethodName")]
public class Patch_Name
{
    static void Prefix() { }

    static void Postfix() { }
}
```

---

## 🔹 Prefix (Before Execution)

Runs **before** the original game method.

### Use cases:

* Block an action
* Modify inputs
* Prepare state

```csharp
static bool Prefix()
{
    return false; // Blocks the original method
}
```

---

## 🔹 Postfix (After Execution)

Runs **after** the original method.

### Use cases:

* Observe results
* Adjust behavior
* Fix side effects

---

## 🚫 Blocking Behavior (Real Use Case)

```csharp
[HarmonyPatch(typeof(Skateboard), "Dismount")]
public class Patch_Dismount
{
    static bool Prefix()
    {
        if (Core.BlockDismount)
        {
            return false;
        }

        return true;
    }
}
```

### Result:

* If condition is true → game method is skipped
* If false → game behaves normally

---

## 🔗 Patch Activation

```csharp
HarmonyInstance.PatchAll();
```

This applies all patches in your mod.

> Without this → nothing is hooked

---

## 🧬 Execution Flow

When a method is called:

```
Prefix → Game Method → Postfix
```

If Prefix returns `false`:

```
Prefix → (Game Method skipped) → Postfix NOT executed
```

---

## ⚠️ Important Understanding

* A patch does not replace game code
* It injects logic into the existing flow
* Timing is critical (frame, transitions, state)

---

## 🎯 Key Takeaway

Harmony gives you control over **when** and **how** the game behaves.

You are no longer just observing the game.
You are shaping its execution.
