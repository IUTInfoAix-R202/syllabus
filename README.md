# <img src="https://raw.githubusercontent.com/IUTInfoAix-R510/Syllabus/main/assets/logo.png" alt="class logo" class="logo" width="120"/> R2.02 — Développement d'applications avec IHM

## BUT Informatique — 1ère année — IUT Aix-Marseille (département Informatique)

---

## 📋 Informations générales

- **Intitulé** : R2.02 - Développement d'applications avec IHM
- **Semestre** : S2
- **Responsable** : [Sébastien NEDJAR](mailto:sebastien.nedjar@univ-amu.fr)
- **Enseignants** :
  - [Frédéric Flouvat](mailto:frederic.flouvat@univ-amu.fr)
  - [Sophie Nabitz](mailto:sophie.nabitz@univ-avignon.fr)
  - [Samir Chtioui](mailto:samir.chtioui@gmail.com)
- **Ressource officielle** : [Annexe 17 PN BUT Informatique](https://cache.media.enseignementsup-recherche.gouv.fr/file/SPE4-MESRI-17-6-2021/35/5/Annexe_17_INFO_BUT_annee_1_1411355.pdf)

---

## 🎯 Objectifs pédagogiques

### Objectif général

Maîtriser la conception et l'implémentation d'applications graphiques interactives en Java/JavaFX, en appliquant les principes d'ergonomie (Nielsen, Gestalt, affordance) et les patrons d'architecture (MVC, MVVM, source unique de vérité).

### Compétences BUT visées

- **C1 AC2** : Élaborer des conceptions simples
- **C1 AC4** : Développer des interfaces utilisateurs
- **C5 AC1** : Appréhender les besoins du client et utilisateur
- **C6 AC1** : Appréhender l'écosystème numérique (GitHub, IDE, outils)

### Acquis d'apprentissage visés

À l'issue de cette ressource, l'étudiant sera capable de :

1. **Concevoir** un graphe de scène JavaFX avec Stage / Scene / Nodes
2. **Utiliser** le modèle événementiel (EventHandler, propagation, filtres)
3. **Structurer** une application avec propriétés observables et bindings
4. **Séparer** vue et logique avec FXML et contrôleurs
5. **Appliquer** les heuristiques de Nielsen (feedback, affordance, prévention d'erreurs)
6. **Architecturer** une application en respectant le pattern MVVM
7. **Maîtriser** un workflow professionnel (TDD, branches, PR, code review)

---

## 📚 Prérequis

### Connaissances requises

- **R1.01 (Initiation au développement)** : bases de la programmation (C++)
- **R2.01 (Développement orienté objets)** : POO Java (classes, héritage, interfaces)
- **R2.03 (Qualité de développement)** : Git et tests unitaires (suivi en parallèle)

### Compétences techniques

- Utilisation d'un IDE (IntelliJ IDEA ou VS Code)
- Ligne de commande Unix/Windows
- Premières notions de Git (clone, commit, push)

### Environnement technique

- **Java 25** (JDK Temurin ou Zulu fx)
- **JavaFX 25** (via pom.xml, aucune installation manuelle)
- **Maven Wrapper 3.9.14** (`./mvnw` fourni dans chaque TP)
- **SceneBuilder** (optionnel, utile à partir du TP3)

---

## 📖 Programme détaillé

### Cours magistraux (4 × 1h30)

| CM | Thème | Prépare | Niveau Bloom | Statut |
|----|-------|---------|--------------|--------|
| [CM1](https://iutinfoaix-r202.github.io/cours/cm1-fondations-ihm.html) | Fondations de l'IHM et première immersion JavaFX | TP1 | Comprendre | ✅ Publié |
| [CM2](https://iutinfoaix-r202.github.io/cours/cm2-donnees-et-liaison.html) | Propriétés, bindings et contrôles | TP2 | Appliquer | ✅ Publié |
| CM3 | Architecture des IHM et FXML | TP3 | Analyser | 🔄 En cours |
| CM4 | MVVM, persistance et synthèse | TP4 + TP5 | Créer / Évaluer | ⏳ À venir |

**Fil rouge des CM** — trois axes traversent l'ensemble des CM :

- **🏗️ Architecture** : code monolithique (CM1) → MVC (CM3) → MVVM (CM4)
- **🧠 Ergonomie / UX** : Nielsen & Gestalt (CM1) → affordance (CM2) → WCAG / Fitts / Hick (CM3)
- **⚡ Modèle événementiel** : `setOnAction` basique (CM1) → propagation complète (CM2) → bindings réactifs (CM2-4)

### Travaux pratiques (5 × séance)

| TP | Thème | Exercices | Difficulté | Statut |
|----|-------|-----------|------------|--------|
| [TP1](https://github.com/IUTInfoAix-R202/tp1) | Bases JavaFX | 6 + 2 bonus | ★ → ★★★★ | ✅ Publié |
| [TP2](https://github.com/IUTInfoAix-R202/tp2) | Propriétés et bindings | 8 + 2 bonus | ★ → ★★★★★ | ✅ Publié |
| [TP3](https://github.com/IUTInfoAix-R202/tp3) | FXML | 7 + 2 bonus | ★ → ★★★★★ | 🔄 En cours |
| TP4 | MVVM | à définir | ★ → ★★★★★ | ⏳ À venir |
| TP5 | Persistance (JDBC, JPA) | à définir | ★ → ★★★★★ | ⏳ À venir |

Chaque TP est autonome (son propre repo Git, sa propre fiche Classroom) mais s'inscrit dans la progression globale : les compétences acquises dans un TP sont systématiquement réinvesties dans les suivants.

---

## 🎓 Philosophie pédagogique

### Approche TDD baby-step

Chaque TP est structuré comme une série de **tests désactivés** (`@Disabled`). L'étudiant active les tests **un par un** dans l'ordre, écrit le code minimal pour les faire passer, puis avance.

Cette approche :

- Évite la panique face à une page blanche
- Rend visible la progression (chaque test vert = un concept maîtrisé)
- Habitue au **développement incrémental** professionnel
- Donne un feedback continu via l'autograding GitHub Classroom

### Workflow professionnel

- **Fork Classroom** de chaque TP : 1 repo par étudiant, créé automatiquement
- **Branches** : les exercices peuvent se développer sur des branches thématiques
- **Pull Request** vers la branche principale pour chaque exercice fini
- **Auto-évaluation** via les tests qui tournent en CI GitHub Actions
- **Code review** pair à pair optionnelle

### Copilot comme tuteur (pas comme copieur)

L'usage de **GitHub Copilot Chat** est **encouragé** dans un rôle pédagogique :

- ✅ Poser des questions conceptuelles ("comment fonctionne `@FXML` ?")
- ✅ Comprendre un message d'erreur
- ✅ Discuter d'une approche **avant** d'écrire le code
- ❌ Demander "écris ce test à ma place"

### Fil rouge : SAE 2.01

Les compétences de R2.02 nourrissent directement la SAE 2.01 — **interface d'extraction et manipulation de données pour des capteurs de détection/identification de chauves-souris**.

La progression est explicite :

- **TP1-2** → composants JavaFX et réactivité
- **TP3** → séparation vue/modèle via FXML
- **TP4** → architecture complète MVVM
- **TP5** → persistance des captures et filtres

---

## 📊 Évaluations

| Contrôle | Coefficient | Modalité | Description |
|----------|------------|----------|-------------|
| **CC1** | 10 | Automatique | Note autograding cumulée sur les TP (tests verts) |
| **CC2** | 10 | Continue | Participation et implication en séance |
| **CC3** | 40 | Écrit final | Mini-application JavaFX sur feuille (2 heures, documents autorisés) |

### CC1 — Autograding TP

Chaque TP publie une note sur GitHub Classroom via le workflow `classroom.yml` :

- Compilation : 10 pts
- Chaque exercice : 90 / N pts (équirépartition sur les N exercices)
- Total sur 100 par TP
- La **moyenne des TP** constitue la note CC1

### CC2 — Participation et implication

Appréciée tout au long du semestre par les enseignants. Critères :

- Présence active en TP
- Qualité des questions posées
- Entraide avec les autres étudiants
- Respect du workflow git (commits clairs, branches, PR)

### CC3 — Examen terminal écrit

- **Durée** : 2 heures
- **Documents autorisés** : oui, anciens sujets conseillés
- **Sujet** : mini-application JavaFX à coder sur feuille (vue, contrôleur, bindings)
- **Barème** : cohérent avec les sujets d'examen des années précédentes

### Anciens sujets d'examen (archive)

- [TestIHM2015 à 2022](https://github.com/IUTInfoAix-R202-archive/) — utilisables comme entraînement. Les plus récents couvrent Othello, Mastermind, Lights Out, Taquin, tracé de fonctions...

---

## 🛠️ Ressources techniques

### Dépôts GitHub (organisation [`IUTInfoAix-R202`](https://github.com/IUTInfoAix-R202))

- [`cours`](https://github.com/IUTInfoAix-R202/cours) — slides Marp des CM
- [`tp`](https://github.com/IUTInfoAix-R202/tp) — index des TP et CM
- [`tp1`](https://github.com/IUTInfoAix-R202/tp1), [`tp2`](https://github.com/IUTInfoAix-R202/tp2), `tp3`... — un repo par TP
- [`template-tp-javafx`](https://github.com/IUTInfoAix-R202/template-tp-javafx) — pivot technique (mainteneurs)
- [`syllabus`](https://github.com/IUTInfoAix-R202/syllabus) — ce document
- [`IUTInfoAix-R202-archive`](https://github.com/IUTInfoAix-R202-archive/) — anciens sujets et archives historiques

### Environnement recommandé

- **IntelliJ IDEA Community** (recommandé) ou **VS Code + extensions Java**
- **SceneBuilder** (facultatif, utile à partir du TP3)
- **GitHub Codespaces** (option cloud gratuite via GitHub Education)

### Documentation officielle

- [Javadoc JavaFX 25](https://openjfx.io/javadoc/25/)
- [OpenJFX Getting Started](https://openjfx.io/openjfx-docs/)
- [dev.java — JavaFX Properties](https://dev.java/learn/javafx/properties/)
- [FXDocs Community](https://fxdocs.github.io/docs/html5/)
- [JavaFX Software (AlmasB)](https://www.youtube.com/playlist?list=PL4h6ypqTi3RR_bhBk6PtLfD83YkaJXXxw) — playlist vidéo

---

## 📞 Contact

- **Responsable** : [Sébastien NEDJAR](mailto:sebastien.nedjar@univ-amu.fr)
- **Équipe pédagogique** : via les issues GitHub du repo concerné, ou e-mail direct
- **Questions d'ordre privé** : e-mail au responsable
