# Projet TXM : Analyse du corpus MPT (Mariage pour tous)

## 📖 Présentation du projet
Dans le cadre du cours **Corpus, ressources et linguistique outillée**, ce projet propose une **analyse quantitative approfondie** du corpus des débats à l’Assemblée nationale française sur la légalisation du mariage pour tous (MPT).  
À l’aide du logiciel **TXM**, l’étude explore les différences significatives entre les discours des **partisans** du projet de loi (représentés par le groupe SRC) et les **opposants** (UMP) en termes de stratégies discursives, de polarité émotionnelle et d’usage du lexique politique.

## 🗂 Source des données

- **Corpus principal** : `MPT-2023-06-23.txm`  
- **Contenu** : Registres de débats de l’Assemblée nationale à partir du **29 janvier 2013**, relatifs à la légalisation du mariage homosexuel.  
- **Structure des données** : 1 727 interventions de locuteurs, organisées en **11 niveaux** comprenant texte (`text`), sections (`div`), métadonnées des locuteurs (`metadata`), etc.

## 🎯 Hypothèses de recherche

1. **Partisans (SRC/PS)** : tendance à utiliser un lexique positif et progressiste, par exemple :
   - `égalité`, `droits`, `progrès`  

2. **Opposants (UMP)** : tendance à recourir à un lexique conservateur et familialiste, par exemple :
   - `famille`, `tradition`, `valeurs`  

3. **Polarité émotionnelle** :
   - Les opposants utilisent davantage des termes négatifs ou alarmistes : `danger`, `menace`, `détruire`  
   - Les partisans mettent en avant le progrès social avec des mots comme : `avancée`, `réforme`

## 🛠 Méthodologie et outils

L’ensemble de l’analyse a été réalisé avec **TXM (version 0.8.1 Mac)**.  

### Principales analyses

- **Lexiques et fréquence des mots (Lexique)** : extraction des mots fréquents du débat : `amendement`, `loi`, `mariage`, `droit`  
- **Partition du corpus** : création de sous-corpus **UMP** et **SRC** selon `metadata@politicalgroup` pour comparaison horizontale  
- **Progression textuelle (Progression)** : suivi dynamique de mots-clés (`danger`, `réforme`, `avancée`) au fil des débats  
- **Concordances** : analyse contextuelle pour identifier les intentions et fonctions rhétoriques selon le positionnement politique  

## 📊 Principaux résultats

- **Fréquence des mots inattendue** : certains termes sont utilisés par les deux camps mais avec des sens pragmatiques très différents.  
- **Stratégie rhétorique de l’UMP** : usage stratégique des termes négatifs :
  - `danger` (30 occurrences), `détruire` (11 occurrences)  
  - Ces mots augmentent avec le temps pour exprimer une inquiétude forte face à la transformation de la structure familiale.  
- **Stratégie rhétorique du SRC** : emploi de termes positifs pour valoriser le projet de loi :
  - `réforme` (31 occurrences), `avancée` (32 occurrences)  
  - Usage ponctuel de `danger` pour réfuter les arguments de l’UMP, en soulignant que le vrai danger est la persistance des discriminations.  

## ⚠️ Limites et perspectives

- **Biais de représentativité** : le groupe SRC inclut plusieurs partis de gauche (ex. PRG), ce qui peut nuancer la pureté de la position PS et introduire des variables confondantes dans les statistiques de fréquence.  
- **Limites de l’outil** : TXM n’a pas permis d’effectuer facilement une comparaison quantitative précise par soustraction des mots caractéristiques entre sous-corpus.  
- **Évolution future** : exportation des données pour analyse avancée en **Python/NLP**, afin de mieux comprendre la polarité émotionnelle et la structure argumentative des débats.  
