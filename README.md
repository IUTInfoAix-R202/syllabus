# <img src=".github/assets/logo.png" alt="class logo" class="logo" width="120"/> R2.02 - Développement d'applications avec IHM

## BUT Informatique - 1ère année - IUT Aix-Marseille (département Informatique)

---

## 📋 Informations générales

- **Intitulé** : R2.02 - Développement d'applications avec IHM
- **Semestre** : S2 (année BUT1)
- **Volume horaire PN** : 38 h (dont 10 h de TP)
- **Maquette locale IUT Aix-Marseille 2025-2026** : 6 h CM + 20 h TD + 10 h TP + 2 h test écrit. Quatre heures supplémentaires de persistance JDBC sont assurées en semaine 7 en préparation de la SAÉ 2.01.
- **Responsable** : [Sébastien NEDJAR](mailto:sebastien.nedjar@univ-amu.fr)
- **Équipe pédagogique** :
  - [Frédéric Flouvat](mailto:frederic.flouvat@univ-amu.fr)
  - [Sophie Nabitz](mailto:sophie.nabitz@univ-avignon.fr)
  - [Samir Chtioui](mailto:samir.chtioui@gmail.com)
  - [Olivier Gérard](mailto:olivier.GERARD@univ-amu.fr) *(intervention ergonomie, 4 h en semaine 7, préparation SAÉ 2.01)*
- **Format des séances** :
  - **CM** : 4 séances de 1h30, en promo entière (4 groupes réunis)
  - **TD** : blocs de 4h en salle machine, en groupe complet (29 étudiants)
  - **TP** : blocs de 2h ou 4h en salle machine, en demi-groupe (~14 étudiants)
  - **Test final** : 2h, commun avec R2.03
- **Ressource officielle** : [Annexe 15 du PN BUT Informatique 2022 - fiche R2.02 p. 92](https://cache.media.education.gouv.fr/file/SP4-MESRI-26-5-2022/14/6/spe617_annexe15_1426146.pdf)
- **Mots-clés officiels** : Interface homme-machine, Événementiel, Ergonomie

---

## 🎯 Objectifs pédagogiques

### Objectif général (extrait du PN)

> *Cette ressource permet d'appréhender la conception d'applications interactives en mettant en œuvre une approche événementielle et en respectant les contraintes ergonomiques liées aux utilisateurs.*

En pratique, le module vise à maîtriser les **fondations du développement d'interfaces graphiques** : structurer un graphe de scène, piloter l'application par des événements, séparer vue et logique via des patrons comme MVC ou MVVM, et concevoir des interfaces utilisables en s'appuyant sur les principes d'ergonomie (Nielsen, Gestalt, affordance).

### Compétences BUT ciblées

Deux compétences du référentiel BUT Informatique sont ciblées par R2.02 :

| Compétence | Intitulé |
|---|---|
| **Compétence 1** | Développer - c'est-à-dire concevoir, coder, tester et intégrer - une solution informatique pour un client |
| **Compétence 2** | Optimiser des applications informatiques, en exploitant les principes algorithmiques et les structures de données adaptés |

### Apprentissages critiques (AC)

> [!NOTE]
> **Lecture des codes d'apprentissages critiques** : dans le PN BUT Informatique 2022, le code `ACLCNN` se décompose ainsi :
> - `L` = niveau (1 = BUT1, 2 = BUT2, 3 = BUT3)
> - `C` = numéro de la compétence
> - `NN` = numéro séquentiel de l'AC dans cette compétence à ce niveau
>
> Exemple : `AC11.02` = 2e apprentissage critique de la compétence 1 au niveau BUT1.

Les acquis critiques officiellement rattachés à R2.02 :

- **AC11.02** - Élaborer des conceptions simples *(structurer le graphe de scène, séparer modèle/vue/contrôleur)*
- **AC11.04** - Développer des interfaces utilisateurs *(cœur du module : composants, événements, FXML, bindings, MVVM)*
- **AC12.02** - Choisir les structures de données adaptées aux problèmes posés *(propriétés observables, collections réactives)*

### Savoirs de référence (descriptif PN)

- **Programmation événementielle** : gestion d'événements, callbacks, propagation
- **Composants graphiques** : éléments de base d'une IHM (fenêtres, conteneurs, contrôles)
- **Liaison de données** : propriétés observables, bindings réactifs
- **Séparation vue/logique** : patrons architecturaux (MVC, MVVM) pour une IHM maintenable
- **Ergonomie / utilisabilité** : heuristiques de Nielsen, lois de Gestalt, affordance (Don Norman)

### SAÉ concernée par cette ressource

- **SAÉ 2.01** - Développement d'une application : interface d'extraction et manipulation de données pour capteurs de détection de chauves-souris. **SAÉ portée conjointement avec R2.03 (Qualité de développement)** - les compétences JavaFX/FXML/MVVM y sont mobilisées pour construire l'application, les compétences Git/TDD/revue de code pour en garantir la qualité.

### Acquis d'apprentissage détaillés (implémentation 2025-2026)

À l'issue de cette ressource, vous serez capable de :

1. **Concevoir** un graphe de scène JavaFX avec Stage / Scene / Nodes et choisir le bon conteneur *(AC11.02)*
2. **Utiliser** le modèle événementiel : `EventHandler`, propagation capture/bubbling, `EventFilter`, `consume()` *(AC11.04)*
3. **Structurer** une application avec propriétés observables (`IntegerProperty`, `StringProperty`...) et bindings unidirectionnels / bidirectionnels *(AC11.02, AC12.02)*
4. **Séparer** vue et logique métier avec FXML et contrôleurs *(AC11.02, AC11.04)*
5. **Appliquer** les heuristiques de Nielsen et les lois de Gestalt pour concevoir des interfaces utilisables *(AC11.04)*
6. **Architecturer** une application selon le patron MVVM avec injection de dépendances *(AC11.02)*
7. **Utiliser un workflow professionnel** : branche → PR → autograding CI → code review *(AC11.04)*
8. **Utiliser Copilot Chat comme tuteur** (compréhension, documentation), jamais comme générateur de solution *(AC11.04)*

> **Note** : les compétences de workflow professionnel (Git/GitHub, revue de code) sont formellement développées dans R2.03 (Qualité de développement), module couplé à R2.02 par la SAÉ 2.01 commune. Elles sont mises en pratique dans chaque TP R2.02 pour préparer la SAÉ.

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
- Lecture de messages d'erreur et de traces d'exécution

### Environnement technique

- **Java 25** (JDK Zulu fx)
- **JavaFX 25** (via `pom.xml`, aucune installation manuelle)
- **Apache Maven 3.9.14 via Maven Wrapper** (`./mvnw` fourni dans chaque TP, aucune installation manuelle)
- **SceneBuilder** (optionnel, utile à partir du TP3)
- **GitHub Codespaces** (recommandé, environnement cloud préconfiguré)
- **VS Code** + extensions Java + **GitHub Copilot Chat** (activé en mode tuteur)

---

## 📖 Programme détaillé

### Calendrier 2025-2026

Le module est réparti sur **7 semaines** du 27 avril au 8 juin 2026, suivies d'un **examen écrit** en commun avec R2.03 le 18 juin. Deux semaines sont officiellement libres pour R2.02 :

- **Semaine 5** (25/05) : consacrée aux SAÉ 2.05 et 2.06 - aucune activité R2.02 ni R2.03.
- **Semaine 7** (08/06) : semaine de préparation de la SAÉ 2.01 - accueille le **TP5 Persistance** (non strictement IHM mais indispensable à la SAÉ, et dont la note **compte en CC1 R2.02**) et l'**intervention ergonomie d'Olivier Gérard** (4 h, hors volume R2.02).

| Semaine | Date | CM | TD | TP | Contenu |
|---|---|---|---|---|---|
| 1 | Lun. 27 avril 2026 | 2 × 1h30 | 4 h | - | **CM1** Fondations IHM · **CM2** Propriétés & bindings · **TP1** Bases JavaFX (4 h) |
| 2 | Lun. 4 mai 2026 | - | 4 h | - | **TP1** fin (2 h) + **TP2** Propriétés & bindings début (2 h) |
| 3 | Lun. 11 mai 2026 | 1h30 | 4 h | 2 h | **CM3** Architecture & FXML · **TP2** suite (6 h) |
| 4 | Lun. 18 mai 2026 | 1h30 | 4 h | 4 h | **CM4** MVVM & synthèse · **TP3** FXML (8 h) |
| 5 | Lun. 25 mai 2026 | - | - | - | *(semaine SAÉ 2.05 / 2.06 - hors R2.02)* |
| 6 | Lun. 1er juin 2026 | - | 4 h | 4 h | **TP4** MVVM (8 h) |
| 7 | Lun. 8 juin 2026 | - | - | - | **TP5** Persistance (4 h, budget SAÉ) · *+ 4 h ergonomie assurées par Olivier Gérard, hors R2.02* |
| **Examen** | **Jeu. 18 juin 2026** | - | **2 h** | - | **CC3** test écrit commun avec R2.03 |

Pédagogiquement, TD et TP sont tous deux du travail sur machine : les modules TP1-TP5 s'étalent indifféremment sur les créneaux TD ou TP. Le calendrier ci-dessus est indicatif, les dates peuvent évoluer selon la scolarité et l'avancement.

### Cours magistraux (6 h au total)

| CM | Thème | Prépare | Niveau Bloom | Slides |
|----|-------|---------|--------------|--------|
| CM1 | Fondations de l'IHM et première immersion JavaFX | TP1 | Comprendre | [HTML](https://iutinfoaix-r202.github.io/cours/cm1-fondations-ihm.html) |
| CM2 | Propriétés, bindings et contrôles | TP2 | Appliquer | [HTML](https://iutinfoaix-r202.github.io/cours/cm2-donnees-et-liaison.html) |
| CM3 | Architecture des IHM et FXML | TP3 | Analyser | 🔄 En cours |
| CM4 | MVVM, persistance et synthèse | TP4 + TP5 | Créer / Évaluer | ⏳ À venir |

Index des slides : <https://iutinfoaix-r202.github.io/cours/>. Les slides sont au format [Marp](https://marp.app/) (Markdown + HTML/PDF exportable) et publiés sur GitHub Pages à chaque push.

**Fil rouge des CM** - trois axes traversent l'ensemble :

- **🏗️ Architecture** : code monolithique (CM1) → séparation vue/modèle en FXML (CM3) → MVVM (CM4)
- **🧠 Ergonomie / UX** : Nielsen & Gestalt (CM1) → affordance (CM2) → WCAG / Fitts / Hick (CM3)
- **⚡ Modèle événementiel** : `setOnAction` basique (CM1) → propagation complète (CM2) → bindings réactifs (CM2-4)

### Travaux pratiques (5 modules, 34 h au total)

> [!IMPORTANT]
> **Accès étudiant aux TP** : le point d'entrée unique est l'index public [**`IUTInfoAix-R202/tp`**](https://github.com/IUTInfoAix-R202/tp). Il centralise les liens **GitHub Classroom** de chaque TP et les pointeurs vers les supports de CM. Chaque acceptation d'un devoir Classroom crée automatiquement un dépôt personnel dans l'organisation [`IUTInfoAix-R202-2026`](https://github.com/IUTInfoAix-R202-2026). Les dépôts enseignants `tp1`..`tp5` sont privés et ne sont pas accessibles directement.

Tous les TPs sont évalués par autograding via GitHub Classroom ([barème détaillé](#cc1---autograding-tp)).

| TP | Thème | Exercices | Répartition | Statut |
|----|-------|-----------|-------------|--------|
| **TP1** | Bases JavaFX (Stage, Scene, Node, layouts, événements) | 6 + 2 bonus | s1-s2 (6 h) | ✅ Publié |
| **TP2** | Propriétés et bindings | 8 + 2 bonus | s2-s3 (8 h) | ✅ Publié |
| **TP3** | FXML | 7 + 2 bonus | s4 (8 h) | 🔄 En cours |
| **TP4** | MVVM (Model-View-ViewModel, testabilité) | à définir | s6 (8 h) | ⏳ À venir |
| **TP5** | Persistance (JDBC, JPA) | à définir | s7 (4 h, slot SAÉ) | ⏳ À venir |

Chaque TP est autonome (son propre dépôt, sa propre fiche Classroom) mais s'inscrit dans la progression : les compétences acquises dans un TP sont systématiquement réinvesties dans les suivants (Compteur TP1 → IntegerProperty TP2 → CompteurFXML TP3 ; FormulaireConnexion TP2 bindings → TP3 FXML + CSS, etc.).

---

## 🎓 Philosophie pédagogique

### Approche TDD baby-step

Chaque exercice pendant les TP est structuré comme une série de **tests désactivés** (`@Disabled`). Vous activez les tests **un par un** dans l'ordre, écrivez le code minimal pour les faire passer, puis avancez.

Cette approche :

- Évite la panique face à une page blanche
- Rend visible la progression (chaque test vert = un concept maîtrisé)
- Habitue au **développement incrémental** professionnel
- Donne un feedback continu via l'autograding GitHub Classroom

### Workflow professionnel

- **Acceptation Classroom** : chaque étudiant accepte le devoir via un lien, ce qui génère automatiquement son repo personnel à partir du template
- **Branches** : les exercices doivent être développés sur des branches thématiques
- **Pull Request** vers la branche principale pour chaque exercice fini
- **Auto-évaluation** via les tests qui tournent en CI GitHub Actions
- **Code review** pair à pair conseillée (revue Copilot automatique)

### GitHub Copilot : deux rôles distincts

**Copilot Chat** (tuteur en séance) est **encouragé** dans un rôle pédagogique précis dans chaque TP :

- ✅ Poser des questions conceptuelles (« comment fonctionne `@FXML` ? »)
- ✅ Comprendre un message d'erreur
- ✅ Discuter d'une approche **avant** d'écrire le code
- ❌ Demander « écris ce test à ma place »

**Copilot code review** (reviewer automatique sur les Pull Requests) est activé sur chaque repo : à chaque ouverture de PR, un commentaire automatique signale les problèmes potentiels (style, bugs, incohérences). Consigne : **lire les commentaires avant de merger** et les intégrer quand ils sont pertinents.

**Pourquoi c'est essentiel** : l'évaluation CC3 se fait **sur feuille, sans outil**. Vous devez construire vos propres automatismes.

### Fil rouge : SAÉ 2.01

Les compétences de R2.02 nourrissent directement la SAÉ 2.01 - **interface d'extraction et manipulation de données pour des capteurs de détection/identification de chauves-souris**.

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

### CC1 - Autograding TP

Chaque TP publie un score sur GitHub Classroom via le workflow `classroom.yml` :

- Compilation : 100 pts
- Chaque exercice : 900 / N pts (équirépartition sur les N exercices)
- À l'intérieur d'un exercice : les points sont répartis entre les méthodes de test, chaque test valant au moins 1 point
- Un test `@Disabled` rapporte **0 point** (un TP « non fait » reste à 0, pas à 1000)
- **Total sur 1000 par TP** (affiché brut par Classroom, ex : `Points 250/1000` ; ramené sur 20 au calcul final en divisant par 50)
- La **moyenne des TP** constitue la note CC1

### CC2 - Participation et implication

CC2 est apprécié sur **20 points** à partir de l'observation en séance par l'équipe pédagogique. Les 4 critères contribuent à parts égales :

| Critère | Poids |
|---|---|
| Présence active en TP | /5 |
| Qualité des questions et contributions | /5 |
| Entraide et collaboration | /5 |
| Respect du workflow git (commits clairs, branches, PR, review) | /5 |
| **Total** | **/20** |

Chaque critère se note sur une échelle informelle : **0** = non observé, **2-3** = satisfaisant, **5** = excellent.

### CC3 - Examen terminal écrit

- **Date** : jeudi 18 juin 2026, commun avec R2.03
- **Durée** : 2 heures
- **Salle** : salle de test dédiée
- **Documents autorisés** : oui, anciens sujets conseillés
- **Sujet** : mini-application JavaFX à coder sur feuille (vue, contrôleur, bindings)

**Gabarit de barème** - pondération indicative sur /20 :

| Critère | Poids |
|---|---|
| Architecture (séparation vue/logique, MVC ou MVVM) | /4 |
| FXML et contrôleur (`fx:controller`, `@FXML`, `initialize`) | /4 |
| Modèle événementiel (`EventHandler`, propagation, actions) | /3 |
| Propriétés observables et bindings | /3 |
| Ergonomie / UX (feedback, affordance, prévention d'erreur) | /3 |
| Lisibilité et propreté du code (nommage, structure, commentaires utiles) | /3 |
| **Total** | **/20** |

> Cette pondération est un **gabarit** : la répartition réelle peut évoluer d'une année sur l'autre selon ce qui a été effectivement couvert et approfondi pendant les séances. Le barème exact est publié avec le sujet de l'année. Les anciens sujets (voir archive) suivent une pondération cohérente avec ce gabarit et sont représentatifs du niveau attendu.

### Anciens sujets d'examen (archive)

- [TestIHM2015 à 2022](https://github.com/IUTInfoAix-R202-archive/) - utilisables comme entraînement. Les plus récents couvrent Othello, Mastermind, Lights Out, Taquin, tracé de fonctions...

---

## 🛠️ Ressources techniques

### Dépôts GitHub (organisation [`IUTInfoAix-R202`](https://github.com/IUTInfoAix-R202))

- [`cours`](https://github.com/IUTInfoAix-R202/cours) - slides Marp des CM
- [`tp`](https://github.com/IUTInfoAix-R202/tp) - index des TP et CM
- [`syllabus`](https://github.com/IUTInfoAix-R202/syllabus) - ce document
- [`IUTInfoAix-R202-archive`](https://github.com/IUTInfoAix-R202-archive/) - anciens sujets et archives historiques

### Documentation officielle

- [Javadoc JavaFX 25](https://openjfx.io/javadoc/25/)
- [OpenJFX Getting Started](https://openjfx.io/openjfx-docs/)
- [dev.java - JavaFX Properties](https://dev.java/learn/javafx/properties/)
- [FXDocs Community](https://fxdocs.github.io/docs/html5/)
- [JavaFX Software (AlmasB)](https://www.youtube.com/playlist?list=PL4h6ypqTi3RR_bhBk6PtLfD83YkaJXXxw) - playlist vidéo

---

## 📞 Contact

- **Responsable** : [Sébastien NEDJAR](mailto:sebastien.nedjar@univ-amu.fr)
- **Équipe pédagogique** : via les issues GitHub du repo concerné, ou e-mail direct
- **Questions d'ordre privé** : e-mail au responsable
