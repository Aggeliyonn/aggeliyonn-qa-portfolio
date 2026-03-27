# 🐉 Äggeliyonn

## QA / Test & Debug – Video Games

QA / Test & Debug portfolio based on real-world cases (Unity / MelonLoader modding).

---

## 📊 Summary

🔴 Reviews: 1
🟠 Major: 1
🟡 Minor: 1
🟢 Visuals: 0

### 📌 Overall Status

✔ Fixed: 2
🔧 In Progress: 1
❗ Remaining: 1
Total Bugs: 3

---

## 🧠 About

I work on analyzing, testing, and understanding game systems.

I develop and test mods by combining QA, debugging, and technical logic to identify, reproduce, and analyze complex in-game behaviors.

I am particularly interested in interactions between systems (player states, transitions, timing, camera).

---

## 🔍 System Analysis Example

### ⭐ Camera & Player State Desynchronization

During the development of the **PhoneOnSkate** mod, a complex bug appeared when closing the phone.

The player remained correctly on the skateboard (consistent world state), but the camera became desynchronized and incorrectly switched between first and third person.

👉 This bug involves several systems:

* Player state
* Skateboard object
* Phone interface (UI)
* Camera management

### 📌 Analysis

The issue appears to come from a conflict between the player's state being maintained on the skateboard and the camera behavior when exiting the phone interface.

---

## 🔧 Projects

### 🎮 PhoneOnSkate — Schedule I

**Context:** Mod currently under development and testing

**Type:** MelonLoader Mod
**Objective:** Use your phone while skateboarding

**Work Completed:**

* Analysis of player states
* Management of transitions (dismount/remount)
* Identification of system bugs:

  * Object cloning (skateboard)
  * Camera desynchronization
  * Timing issues (frames)

📌 Concrete example (Full QA Report):
👉 [See the QA Report](Mod/Schedule1/PhoneOnSkate/QA_Report_v0.1.md)

📊 ProfitCalculator — Schedule I

Context: Tool in active development

Type: Client-side Mod
Objective: Analyze recipes and calculate profit based on ingredients and effects

Work in Progress:

Data extraction from in-game phone
Recipe analysis system
Profit calculation logic
UI display and filtering (effects, ingredients, profit)

📌 Development tracking:
👉 [See the project](Mod/Schedule1/ProfitCalculator/README.md)

---

## 🧪 QA Reports

* PhoneOnSkate v0.1
* (Upcoming project)

---

## 🧪 QA Approach

* Scenario identification
* Accurate bug reproduction
* Condition and timing analysis
* Structured documentation (Dev Log + QA Report)
* Bug prioritization (critical → visual)

---

## 🛠️ Skills

* Manual testing
* Bug reproduction
* Behavioral analysis
* Multi-state systems analysis
* Log reading (MelonLoader / Unity)
* Modding (Harmony, IL2CPP)
