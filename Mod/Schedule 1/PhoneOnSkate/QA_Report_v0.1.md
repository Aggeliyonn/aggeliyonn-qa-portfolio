# 🧪 QA Report – PhoneOnSkate v0.1

**Jeux :** Schedule 1 - PhoneOnSkate  

---

## 📊 Résumé

🔴 Critiques : 1  
🟠 Majeurs : 1  
🟡 Mineurs : 1  
🟢 Visuels : 0  

### 📌 Statut global

✔ Corrigés : 2  
🔧 En cours : 1  
❗ Restants : 1  

---

## 🔧 Dev Log

**Objectif :**  
Pouvoir utiliser le téléphone sur le skate sans dismount et continuer à rouler.

### Étape – Bloquer le dismount
- Empêcher le dismount à l’ouverture du téléphone  

### Étape – Ralentir le dismount
- Empêcher le dismount pendant 6 frames  

### Étape – Dismount Remount
- Remount automatique après dismount contrôlé  

---

## 🐞 QA Bug Report

---

### 🔴 Bug – Freeze écran

**Origine :** Étape Bloquer le dismount  

#### Conditions
- Être sur le skate  
- Ouvrir le téléphone  

#### Étapes
1. Monter sur le skate  
2. Ouvrir le téléphone  

#### Résultat actuel
- Freeze complet du jeu  
- Apparition d’une zone noire  

#### 📷 Capture du bug
![Bug](Pictures/bug-block-dismount.png)

#### Résultat attendu
- Rester sur le skate avec le téléphone ouvert  

#### Fréquence
- 10/10  

#### Reproductibilité
- Toujours → déclenchable à coup sûr  

#### Analyse
- Semble lié à la caméra, au joueur et au téléphone  
- Se produit uniquement sur le skate  
- Probable conflit entre UI et caméra  

#### Statut
✔ Corrigé  

---

### 🟠 Bug – Remount impossible

**Origine :** Étape Ralentir le dismount  

#### Conditions
- Ouvrir le téléphone  
- Attendre 6 frames  

#### Étapes
1. Monter sur le skate  
2. Ouvrir le téléphone  

#### Résultat actuel
- Aucun remount  

#### Résultat attendu
- Remount après délai  

#### Fréquence
- 10/10  

#### Reproductibilité
- Toujours  

#### Analyse
- Le skate disparaît temporairement  
- Le remount ne peut pas s’appliquer  

#### Statut
✔ Corrigé  

---

### 🟡 Bug – Désynchronisation caméra

**Origine :** Étape Dismount Remount  

#### Conditions
- Ouvrir puis fermer le téléphone  

#### Étapes
1. Monter sur le skate  
2. Ouvrir le téléphone  
3. Fermer le téléphone  

#### Résultat actuel
- Bug caméra  

#### Résultat attendu
- Caméra cohérente  

#### Fréquence
- 10/10  

#### Reproductibilité
- Toujours  

#### Analyse
- Conflit entre état joueur et caméra  
- La caméra ne sait pas si elle doit être en first ou third person  

#### Statut
🔧 En cours  
