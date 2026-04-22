# <img src="https://raw.githubusercontent.com/IUTInfoAix-R510/Syllabus/main/assets/logo.png" alt="class logo" class="logo" width="120"/> R2.02 — Développement d'applications avec IHM

## BUT Informatique — 1ère année — IUT Aix-Marseille (département Informatique)

---

## 📋 Informations générales

- **Intitulé** : R2.02 - Développement d'applications avec IHM
- **Semestre** : S2 (année BUT1)
- **Période** : 8 semaines, du 27 avril au 15 juin 2026
- **Volume horaire** : 38h (6h CM + 22h TD + 10h TP) + 2h de test final
- **Responsable** : [Sébastien NEDJAR](mailto:sebastien.nedjar@univ-amu.fr)
- **Enseignants** :
  - [Frédéric Flouvat](mailto:frederic.flouvat@univ-amu.fr)
  - [Sophie Nabitz](mailto:sophie.nabitz@univ-avignon.fr)
  - [Samir Chtioui](mailto:samir.chtioui@gmail.com)
- **Format des séances** :
  - **CM** : 4 séances de 1h30 (cf. slides sur GitHub Pages)
  - **TD** : blocs de 4h en salle machine (bloc unique ou 2 × 2h selon emploi du temps)
  - **TP** : séances de 2h dédoublées ou 4h dédoublées, salle machine
  - **Test final** : 2h en salle de test
- **Ressource officielle** : [Annexe 17 PN BUT Informatique](https://cache.media.enseignementsup-recherche.gouv.fr/file/SPE4-MESRI-17-6-2021/35/5/Annexe_17_INFO_BUT_annee_1_1411355.pdf)

---

## 🎯 Objectifs pédagogiques

### Objectif général (extrait du PN)

Cette ressource vise à développer les compétences relatives à la **conception et au développement d'applications interactives** : la modélisation et la mise en œuvre d'interfaces homme-machine (IHM), la programmation événementielle, la séparation claire entre données / vue / logique, et la prise en compte de l'utilisateur final (ergonomie, utilisabilité).

### Compétences BUT ciblées

- **C1 AC2** — Élaborer des conceptions simples *(architecture des applications graphiques)*
- **C1 AC4** — Développer des interfaces utilisateurs *(cœur du module)*
- **C5 AC1** — Appréhender les besoins du client et utilisateur *(heuristiques ergonomiques)*
- **C6 AC1** — Appréhender l'écosystème numérique *(GitHub, IDE, Maven, CI)*

### Apprentissages critiques (AC)

Les acquis critiques officiellement rattachés à R2.02 :

- **C1 AC2** — Élaborer des conceptions simples *(structurer le graphe de scène, séparer modèle/vue/contrôleur)*
- **C1 AC4** — Développer des interfaces utilisateurs *(composants, événements, FXML, bindings, MVVM)*
- **C5 AC1** — Appréhender les besoins du client et utilisateur *(heuristiques de Nielsen, affordance, prévention d'erreurs)*
- **C6 AC1** — Appréhender l'écosystème numérique *(workflow Git/GitHub, autograding Classroom, IDE)*

### Savoirs de référence (descriptif PN)

- **Programmation événementielle** : `EventHandler`, propagation (capture/bubbling), gestionnaires multiples
- **Composants graphiques de base** : Stage, Scene, Nodes, layouts, contrôles (Button, Label, TextField, Slider, ComboBox…)
- **Liaison de données** : propriétés observables, bindings unidirectionnels et bidirectionnels
- **Séparation vue/logique** : FXML déclaratif, contrôleurs, patron MVC puis MVVM
- **Ergonomie / utilisabilité** : heuristiques de Nielsen, lois de Gestalt, affordance (Don Norman)
- **Persistance simple** : sérialisation, JDBC, JPA (ouverture vers R3/R4)

### SAÉ concernée par cette ressource

- **SAÉ 2.01** — Développement d'une application *(fil rouge du module : interface d'extraction et manipulation de données pour capteurs de détection de chauves-souris)*

### Acquis d'apprentissage détaillés (implémentation 2025-2026)

À l'issue de cette ressource, l'étudiant sera capable de :

1. **Concevoir** un graphe de scène JavaFX avec Stage / Scene / Nodes et choisir le bon conteneur *(C1 AC2)*
2. **Utiliser** le modèle événementiel : `EventHandler`, propagation capture/bubbling, `EventFilter`, `consume()` *(C1 AC4)*
3. **Structurer** une application avec propriétés observables (`IntegerProperty`, `StringProperty`…) et bindings unidirectionnels / bidirectionnels *(C1 AC2, C1 AC4)*
4. **Séparer** vue et logique métier avec FXML et contrôleurs *(C1 AC2, C1 AC4)*
5. **Appliquer** les heuristiques de Nielsen et les lois de Gestalt pour concevoir des interfaces utilisables *(C5 AC1)*
6. **Architecturer** une application selon le patron MVVM avec injection de dépendances *(C1 AC2)*
7. **Utiliser un workflow professionnel** : branche → PR → autograding CI → code review *(C6 AC1)*
8. **Utiliser Copilot Chat comme tuteur** (compréhension, documentation), jamais comme générateur de solution *(C6 AC1)*

---

## 📚 Prérequis

Le PN ne formalise **aucun prérequis** pour R2.02. En pratique, le module s'appuie sur :

### Connaissances recommandées

- **R1.01 (Initiation au développement)** : bases de la programmation (C++)
- **R2.01 (Développement orienté objets)** : POO Java (classes, héritage, interfaces, collections génériques)
- **R2.03 (Qualité de développement)** : Git, tests unitaires (suivi en parallèle)

### Compétences techniques

- Utilisation d'un IDE Java (VS Code, IntelliJ IDEA) ou Codespaces dans le navigateur
- Ligne de commande Unix
- Premières notions de Git (clone, commit, push, branches)
- Lecture de messages d'erreur et de stacks traces

### Environnement technique

- **Java 25** (JDK Zulu fx)
- **JavaFX 25** (via `pom.xml`, aucune installation manuelle)
- **Maven Wrapper 3.9.14** (`./mvnw` fourni dans chaque TP)
- **SceneBuilder** (optionnel, utile à partir du TP3)
- **GitHub Codespaces** (recommandé, environnement cloud préconfiguré)
- **VS Code** + extensions Java + **GitHub Copilot Chat** (activé en mode tuteur)

---

## 📖 Programme détaillé

### Calendrier 2025-2026

Le module est réparti sur **8 semaines** du 27 avril au 15 juin 2026, suivies d'un **examen écrit** en commun avec R2.03 :

| Semaine | Date | CM | TD | TP | Contenu |
|---|---|---|---|---|---|
| 1 | Lun. 27 avril 2026 | 1h30 | 4 h | — | **CM1** Fondations IHM · **TD1** Premiers composants JavaFX |
| 2 | Lun. 4 mai 2026 | 1h30 | 4 h | 2 h | **CM2** Propriétés & bindings · **TD2** · **TP1** Bases JavaFX |
| 3 | Lun. 11 mai 2026 | — | 4 h | 2 h | **TD3** · **TP2** Propriétés et bindings |
| 4 | Lun. 18 mai 2026 | 1h30 | 4 h | 2 h | **CM3** Architecture & FXML · **TD4** · **TP3** FXML |
| 5 | Lun. 25 mai 2026 | — | 4 h | — | **TD5** (suite FXML / MVVM) |
| 6 | Lun. 1er juin 2026 | 1h30 | 2 h | 2 h | **CM4** MVVM & synthèse · **TP4** MVVM |
| 7 | Lun. 8 juin 2026 | — | — | 2 h | **TP5** Persistance |
| **Examen** | **Lun. 15 juin 2026** | — | **2 h** | — | **CC3** test écrit commun avec R2.03 (salle de test) |

**Durée d'une séance** : CM de 1h30, TD en blocs de 4h (ou 2 × 2h), TP dédoublés de 2h ou 4h. Le responsable organise le découpage avec la scolarité. Le calendrier ci-dessus est indicatif — les dates de publication des CM/TP peuvent bouger selon l'avancement.

### Cours magistraux (6 h au total)

| CM | Thème | Prépare | Niveau Bloom | Slides |
|----|-------|---------|--------------|--------|
| CM1 | Fondations de l'IHM et première immersion JavaFX | TP1 | Comprendre | [HTML](https://iutinfoaix-r202.github.io/cours/cm1-fondations-ihm.html) |
| CM2 | Propriétés, bindings et contrôles | TP2 | Appliquer | [HTML](https://iutinfoaix-r202.github.io/cours/cm2-donnees-et-liaison.html) |
| CM3 | Architecture des IHM et FXML | TP3 | Analyser | 🔄 En cours |
| CM4 | MVVM, persistance et synthèse | TP4 + TP5 | Créer / Évaluer | ⏳ À venir |

Index des slides : <https://iutinfoaix-r202.github.io/cours/>. Les slides sont au format [Marp](https://marp.app/) (Markdown + HTML/PDF exportable) et publiés sur GitHub Pages à chaque push.

**Fil rouge des CM** — trois axes traversent l'ensemble :

- **🏗️ Architecture** : code monolithique (CM1) → séparation vue/modèle en FXML (CM3) → MVVM (CM4)
- **🧠 Ergonomie / UX** : Nielsen & Gestalt (CM1) → affordance (CM2) → WCAG / Fitts / Hick (CM3)
- **⚡ Modèle événementiel** : `setOnAction` basique (CM1) → propagation complète (CM2) → bindings réactifs (CM2-4)

### Travaux pratiques (10 h TP + 22 h TD)

| TP | Thème | Exercices | Format | Noté | Statut |
|----|-------|-----------|--------|------|--------|
| [TP1](https://github.com/IUTInfoAix-R202/tp1) | Bases JavaFX (Stage, Scene, Node, layouts, événements) | 6 + 2 bonus | TD + TP (semaines 1-2) | ✅ autograding | ✅ Publié |
| [TP2](https://github.com/IUTInfoAix-R202/tp2) | Propriétés et bindings | 8 + 2 bonus | TD + TP (semaines 2-3) | ✅ autograding | ✅ Publié |
| [TP3](https://github.com/IUTInfoAix-R202/tp3) | FXML | 7 + 2 bonus | TD + TP (semaines 4-5) | ✅ autograding | 🔄 En cours |
| [TP4](https://github.com/IUTInfoAix-R202/tp4) | MVVM (Model-View-ViewModel, testabilité) | à définir | TD + TP (semaine 6) | ✅ autograding | ⏳ À venir |
| [TP5](https://github.com/IUTInfoAix-R202/tp5) | Persistance (JDBC, JPA) | à définir | TP (semaine 7) | ✅ autograding | ⏳ À venir |

Les énoncés et le code de chaque TP sont distribués aux étudiants exclusivement via **GitHub Classroom** : l'index public [`tp`](https://github.com/IUTInfoAix-R202/tp) centralise les liens et chaque acceptation crée un dépôt personnel dans l'organisation Classroom [`IUTInfoAix-R202-2026`](https://github.com/IUTInfoAix-R202-2026).

Chaque TP est autonome (son propre dépôt, sa propre fiche Classroom) mais s'inscrit dans la progression : les compétences acquises dans un TP sont systématiquement réinvesties dans les suivants (Compteur TP1 → IntegerProperty TP2 → CompteurFXML TP3 ; FormulaireConnexion TP2 bindings → TP3 FXML + CSS, etc.).

---

## 🎓 Philosophie pédagogique

### Approche TDD baby-step

Chaque exercice pendant les TP est structuré comme une série de **tests désactivés** (`@Disabled`). L'étudiant active les tests **un par un** dans l'ordre, écrit le code minimal pour les faire passer, puis avance.

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
- **Code review** pair à pair optionnelle (revue Copilot automatique)

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
- **Salle** : salle de test dédiée
- **Documents autorisés** : oui, anciens sujets conseillés
- **Sujet** : mini-application JavaFX à coder sur feuille (vue, contrôleur, bindings)
- **Barème** : cohérent avec les sujets d'examen des années précédentes
- **Date** : dernière semaine du module (semaine du 15 juin 2026)

### Anciens sujets d'examen (archive)

- [TestIHM2015 à 2022](https://github.com/IUTInfoAix-R202-archive/) — utilisables comme entraînement. Les plus récents couvrent Othello, Mastermind, Lights Out, Taquin, tracé de fonctions...

---

## 🛠️ Ressources techniques

### Dépôts GitHub (organisation [`IUTInfoAix-R202`](https://github.com/IUTInfoAix-R202))

- [`cours`](https://github.com/IUTInfoAix-R202/cours) — slides Marp des CM
- [`tp`](https://github.com/IUTInfoAix-R202/tp) — index des TP et CM
- [`syllabus`](https://github.com/IUTInfoAix-R202/syllabus) — ce document
- [`IUTInfoAix-R202-archive`](https://github.com/IUTInfoAix-R202-archive/) — anciens sujets et archives historiques

### Environnement recommandé

- **VS Code + extensions Java**
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
