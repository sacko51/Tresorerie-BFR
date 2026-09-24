# Dossier 2 - Gestion de la Trésorerie et Pilotage du BFR

Modèle financier prévisionnel sur 12 mois pour une PME fictive de négoce et distribution en croissance rapide. Projet personnel réalisé par un étudiant en Master 2 CGAO. Il montre comment une entreprise structurellement rentable peut se retrouver en situation de cessation de paiements si l'accroissement du Besoin en Fonds de Roulement (BFR) et le financement des investissements ne sont pas anticipés.

Fichiers : [`Dossier2_Tresorerie_BFR.xlsx`](./Dossier2_Tresorerie_BFR.xlsx) · [`Dossier2_Note_Synthese_Tresorerie_BFR.docx`](./Dossier2_Note_Synthese_Tresorerie_BFR.docx)

---

## Synthèse des enseignements financiers

- **L'impasse de trésorerie d'avril à juillet** : partant d'un solde initial de **+25,0 k€**, la trésorerie plonge à **-40,0 k€ fin avril** et reste dans le rouge 4 mois consécutifs, avant de se rétablir en août (+9,1 k€) et d'atteindre **+54,0 k€** en fin d'année (soit +29,0 k€ de variation nette annuelle).
- **Double cause identifiée :**
  1. **Erreur d'adossement financier** : un investissement matériel de 50,0 k€ TTC est financé au comptant sur la trésorerie d'exploitation en avril, au lieu d'une ressource stable de moyen/long terme.
  2. **Effet ciseau du BFR** : en phase de croissance (CA de 60 à 120 k€), les fournisseurs sont payés à 30 jours tandis que 30 % du CA client n'est encaissé qu'à 60 jours - le BFR d'exploitation passe de 45,0 k€ (janvier) à un pic de **84,6 k€ (juillet)**.
- **Effet du refinancement chiffré sur 12 mois** : un emprunt moyen terme de 50 k€ (4,0 %/an sur 48 mois) comble l'impasse d'avril (solde ramené à **+10,0 k€**) et maintient une trésorerie positive sur l'ensemble de l'année, mensualité de remboursement comprise.

---

## Architecture du classeur

| Onglet | Contenu | Décision de gestion |
|---|---|---|
| `00_Sommaire` | Cadrage de la mission | Vue globale des objectifs financiers |
| `01_Hypotheses_BFR` | Règles DSO/DPO, TVA, acomptes IS, hypothèses d'amorçage (CA nov./déc. N-1) | Cadre de calcul intégralement traçable |
| `02_Budget_Tresorerie` | Grille 12 mois — encaissements, décaissements, solde net | Détection de l'impasse d'avril-juillet |
| `03_Indicateurs_BFR` | Créances clients, dettes fournisseurs, BFR, variation de BFR, DSO, DPO | Illustre le mécanisme de l'effet de ciseau |
| `04_Scenario_Financement` | Emprunt MT modélisé mensualité par mensualité + graphique comparatif | Chiffre l'effet du refinancement sur 12 mois |

Le classeur est entièrement **piloté par formules** : la ligne TVA, les encaissements décalés (20 %/50 %/30 %) et les décaissements fournisseurs (M+1) sont calculés à partir des hypothèses, pas saisis en dur.

---

## Mécanique de modélisation

### Règles de flux

- **Encaissements clients (TTC, TVA 20 %)** : 20 % au comptant (mois M), 50 % à 30 jours (M+1), 30 % à 60 jours (M+2), soit un DSO théorique pondéré de 33 jours.
- **Décaissements fournisseurs** : achats = 50 % du CA HT, réglés 100 % à 30 jours (M+1).
- **Charges fixes** : salaires nets 20,0 k€/mois (comptant) · charges sociales 10,0 k€/mois (M+1) · charges externes 8,0 k€/mois (comptant) · acomptes IS 5,0 k€/trimestre.
- **Investissement** : 50,0 k€ TTC décaissés comptant en avril.

### Pilotage du BFR (onglet 03)

| Indicateur | Janvier | Pic (juillet) | Décembre |
|---|---|---|---|
| BFR d'exploitation | 45,0 k€ | **84,6 k€** | 75,6 k€ |
| DSO | 34 j | 33 j | 34 j |
| DPO | 30 j | 30 j | 30 j |

### Scénario de financement corrigé (onglet 04)

| Mois | Trésorerie baseline | Trésorerie avec emprunt MT |
|---|---|---|
| Avril | **-40,0 k€** | **+10,0 k€** |
| Juillet | -5,2 k€ | +41,4 k€ |
| Décembre | +54,0 k€ | +95,0 k€ |

---

## Plan d'action du contrôleur financier

- **Restructuration du financement** : emprunt bancaire MT ou crédit-bail de 50 k€ sur 4 ans dès avril.
- **Optimisation du BFR** : mobilisation des créances à 60 jours via cession Dailly/affacturage lors des pointes d'activité (mai/juin) ; renégociation des délais fournisseurs (30 → 45-60 jours fin de mois).
- **Négociation bancaire préventive** : autorisation de découvert plafonnée à 20 k€, négociée dès janvier en appui du budget prévisionnel.

## Compétences mobilisées

- Gestion de trésorerie d'entreprise : plan de trésorerie glissant mensuel, calcul de la TVA nette à décaisser, calendrier d'acomptes d'IS.
- Analyse du BFR : délais de règlement (DSO/DPO), identification des points de friction de liquidité en phase de croissance.
- Stratégie de financement court/moyen terme : arbitrage entre crédit de trésorerie (Dailly, affacturage), découvert négocié et endettement moyen terme adossé aux actifs immobilisés.
- Modélisation Excel : classeur intégralement formulé, scénario de financement chiffré sur 12 mois.
