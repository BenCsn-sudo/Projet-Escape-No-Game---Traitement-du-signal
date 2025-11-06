#  Traitement du signal – Projet Python
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

##  Description

Ce projet simule le fonctionnement complet d’une **chaîne de communication numérique**.
À partir d’un message texte (`"SOS, besoin d’aide ! K57"`), le programme illustre toutes les étapes de transformation du signal, depuis l’écriture jusqu’à la réception et la reconstitution du message.

Le tout est réalisé dans un **notebook Python interactif** (`livrable.ipynb`), entièrement commenté et accompagné de schémas explicatifs.

---

##  Fonctionnement

1. ✍️ **Écriture du message**
   Exemple : `"SOS, besoin d’aide ! K57"`

2. 💾 **Conversion en binaire (ASCII)**
   Chaque caractère est transformé en une suite de bits (`A → 1000001`).

3. 🔀 **Codage Manchester**
   Permet une meilleure synchronisation des signaux (`1010 → 10011001`).

4. 📶 **Modulation FSK (Frequency Shift Keying)**
   Transformation du signal binaire en onde sinusoïdale à deux fréquences distinctes.

5. 📡 **Transmission et réception du signal**
   Simulation d’un envoi vers une station distante.

6. 🔁 **Démodulation et décodage**

   * Démodulation FSK → récupération du signal binaire
   * Décodage Manchester → retour au message ASCII

7. 🖥️ **Affichage du message reçu**
   Le texte original est reconstitué :
   `"SOS, besoin d’aide ! K57"`

---

##  Contenu du dépôt

* `livrable.ipynb` → Notebook principal du projet
* `chaine.png`, `agence.png`, `micro.png`, `tablette.png`, etc. → Illustrations pédagogiques
* `README.md` → Documentation du projet

---

##  Exécution

Assurez-vous d’avoir installé **Jupyter Notebook** et les dépendances Python (comme `numpy` et `matplotlib`).

```bash
# Lancer le notebook
jupyter notebook livrable.ipynb
```

Ou exécutez-le en ligne de commande :

```bash
jupyter nbconvert --to notebook --execute livrable.ipynb
```

---

##  Objectif pédagogique

Ce projet illustre :

* la **numérisation d’un signal**,
* les **principes de modulation FSK**,
* le **codage Manchester** et le **décodage ASCII**,
* la **chaîne complète d’un système de communication numérique**.

Il s’adresse à toute personne souhaitant comprendre concrètement comment un message textuel peut être transformé en onde électromagnétique puis reconverti.

---

##  Licence

Ce projet est distribué sous licence MIT — libre à vous de le modifier et de l’améliorer.
