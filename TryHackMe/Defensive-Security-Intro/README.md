# 🛡️ Rapport d'Incident : Attaque par Force Brute sur FakeBank

**Plateforme d'entraînement :** TryHackMe - Salle "Defensive Security Intro"
**Rôle simulé :** Analyste SOC Niveau 1 (Security Operations Center)
**Date de l'incident :** 26 Septembre 2026
**Sévérité :** 🔴 CRITIQUE
**Statut :** ✅ Résolu et Contenu

---

## 📌 1. Résumé Exécutif

Le Centre Opérationnel de Sécurité (SOC) de FakeBank a détecté une série de tentatives de connexion suspectes et échouées sur son système d'authentification. L'investigation a révélé qu'un groupe de menaces persistant connu sous le nom de **ShadowFigures** tentait de compromettre le compte de l'utilisateur `dave.saunders` via une attaque par **force brute** (Brute Force).

Grâce à une réponse rapide, le compte a été verrouillé avant toute compromission réussie, et l'attaquant a été identifié via la plateforme de renseignement sur les menaces (Threat Intelligence). Un rapport d'incident officiel a été soumis.

---

## 🔍 2. Détails de l'Incident

| Élément | Valeur |
| :--- | :--- |
| **Type d'attaque** | Brute Force (Tentatives de connexion multiples) |
| **Compte ciblé** | `dave.saunders` |
| **Page ciblée** | `/login` |
| **Attaquant identifié** | Groupe **ShadowFigures** |
| **Origine estimée** | Europe de l'Est (Possible) |
| **Objectif de l'attaquant** | Vol d'identifiants bancaires |
| **Référence du rapport** | `SOC-2026-0926-001` |

---

## 🕵️ 3. Démarche d'Investigation (Méthodologie)

Voici les étapes suivies pour analyser et répondre à l'incident :

1. **Détection de l'alerte :**
   - Surveillance du tableau de bord *Event Management*.
   - Détection d'une alerte critique intitulée : *"Suspicious Login Attempts"*.

2. **Analyse de l'alerte :**
   - Extraction des informations clés : le nom d'utilisateur ciblé (`dave.saunders`) et la page visée (`/login`).
   - Constatation d'un volume anormal de tentatives échouées.

3. **Attribution (Threat Intelligence) :**
   - Utilisation de la plateforme de renseignement sur les menaces pour rechercher l'attaquant.
   - Identification du groupe **ShadowFigures** (connu pour cibler les banques et institutions financières via des techniques de force brute et l'utilisation de listes de mots de passe volés).
   - Le groupe est également connu sous les alias : `SF-GROUP`, `DARKLOGIN`, `Ghost-0x1`.

4. **Réponse à Incident (Incident Response) :**
   - **Action immédiate :** Verrouillage du compte `dave.saunders` pour stopper net l'attaque.
   - **Preuve de validation :** Flag obtenu `THM{ACCOUNT-LOCKED}`.

5. **Rédaction du Rapport :**
   - Soumission du rapport d'incident officiel via la plateforme (Réf: `SOC-2026-0926-001`).
   - Mise à jour de la base de données Threat Intelligence avec les informations sur l'incident.

---

## ✅ 4. Recommandations de Sécurité

Pour éviter qu'un tel incident ne se reproduise, voici les mesures préventives à mettre en place :

- [ ] **Authentification Multifacteur (MFA) :** Rendre la MFA obligatoire pour tous les comptes utilisateurs afin de bloquer les attaques par force brute même si le mot de passe est correct.
- [ ] **Limitation de débit (Rate Limiting) :** Configurer le système de connexion pour bloquer les adresses IP après un certain nombre de tentatives échouées (ex: 5 tentatives).
- [ ] **Politique de mots de passe :** Exiger des mots de passe complexes, longs et uniques pour tous les employés.
- [ ] **Sensibilisation des employés :** Former le personnel sur les risques liés au phishing et aux attaques par force brute.

---

## 📚 5. Compétences Démontrées

`Analyse SOC` `Threat Intelligence` `Réponse à Incident` `Rédaction de Rapport` `Sécurité Défensive` `Analyse de Logs`

---

*Rapport rédigé dans le cadre de mon apprentissage en cybersécurité sur TryHackMe.*
