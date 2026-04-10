# grist-widget-multifield-viewer

> Grist custom widget — affichage des commentaires spécialistes / Specialist comments viewer.  
> Affiche les champs texte longs d'un enregistrement avec 3 modes de rendu et des libellés personnalisables.

---

## 🇫🇷 Français

### Présentation

Widget personnalisé pour [Grist](https://www.getgrist.com/) qui affiche les champs texte longs d'un enregistrement sélectionné — typiquement des avis de spécialistes ou commentaires multiples — dans une interface compacte et lisible.

Conçu pour s'intégrer dans une page multi-vues : la sélection d'une ligne dans une table principale actualise automatiquement le widget.

### Fonctionnalités

* **3 modes d'affichage** — Onglets, Liste accordéon, Grille 2 colonnes
* **Onglets** — un onglet par champ, point coloré selon présence de contenu, texte complet affiché au clic
* **Liste accordéon** — dépliage animé, badge ✓ / — par champ
* **Grille** — aperçu compact 2 colonnes avec scroll par carte
* **Champs configurables** — activer/désactiver chaque champ, personnaliser son libellé
* **Options persistées** via `grist.setOption()` (mode et libellés retenus après rechargement)
* **Bilingue** — détection automatique FR / EN selon `navigator.language`
* **Accessible** — rôles ARIA, navigation clavier, focus visible

### Installation

1. Dans ta page Grist, ajouter une vue → **Widget personnalisé**
2. Dans le panneau de droite, renseigner l'URL du fichier hébergé (voir ci-dessous)
3. Sélectionner l'accès **"Lire l'enregistrement sélectionné"**
4. Lier le widget à ta table principale via **"Données de"**

### Configuration

Clique sur l'icône ⚙️ en haut à droite du widget pour :
- Choisir le mode d'affichage (Onglets / Liste / Grille)
- Cocher/décocher les champs à afficher
- Renommer les libellés affichés (sans modifier les noms de colonnes Grist)

### Colonnes attendues par défaut

Le widget est préconfiguré pour les champs suivants (modifiables dans le panneau ⚙️) :

| Colonne Grist | Libellé par défaut |
|---|---|
| `Avis_famille_internat` | Avis famille internat |
| `Avis_famille_apprentissage` | Avis famille apprentissage |
| `Motivation_de_l_eleve_et_de_sa_famille` | Motivation élève & famille |
| `avis_de_l_enseignant_accompagnateur_du_projet_de_l_eleve` | Enseignant accompagnateur |
| `avis_du_chef_d_etablissement_prenant_appui_sur_la_decision_du_conseil_de_classe` | Chef d'établissement |
| `avis_du_medecin_de_l_education_nationale_si_besoin_et_dans_la_mesure_du_possible` | Médecin EN |
| `avis_des_partenaires_de_soin_esms_sessad_etc_nom_et_fonction` | Partenaires de soin |
| `situation_particuliere` | Situation particulière |
| `commentaires` | Commentaires |

> Ces colonnes correspondent à un formulaire Démarches Numériques (procédure 131937). Adapte-les à ta propre table via le panneau de réglages.

### Hébergement

Le widget est un fichier HTML autonome, sans dépendance npm ni étape de build.

* **GitHub Pages** : activer Pages sur ce dépôt, utiliser l'URL  
  `https://<user>.github.io/grist-widget-multifield-viewer/widget_multifield_viewer.html`
* **Tout serveur HTTP statique** (Scalingo, Netlify, serveur WebDAV public…)

---

## 🇬🇧 English

### Overview

A Grist custom widget that displays long text fields from a selected record — typically specialist opinions or multiple comments — in a compact, readable interface.

Designed for multi-view pages: selecting a row in the main table automatically updates the widget.

### Features

* **3 display modes** — Tabs, Accordion list, 2-column Grid
* **Tabs** — one tab per field, colored dot indicating content presence, full text on click
* **Accordion list** — animated expand/collapse, ✓ / — badge per field
* **Grid** — compact 2-column preview with per-card scrolling
* **Configurable fields** — enable/disable each field, customize its label
* **Persisted options** via `grist.setOption()` (mode and labels survive page reload)
* **Bilingual** — automatic FR / EN detection via `navigator.language`
* **Accessible** — ARIA roles, keyboard navigation, visible focus

### Setup

1. In your Grist page, add a view → **Custom Widget**
2. In the right panel, enter the hosted file URL (see below)
3. Select access level **"Read selected record"**
4. Link the widget to your main table via **"Data from"**

### Configuration

Click the ⚙️ icon in the widget's top-right corner to:
- Choose the display mode (Tabs / List / Grid)
- Toggle fields on/off
- Rename labels (without changing Grist column names)

### Hosting

Single self-contained HTML file — no npm, no build step.

* **GitHub Pages**: enable Pages on this repo, use  
  `https://<user>.github.io/grist-widget-multifield-viewer/widget_multifield_viewer.html`
* **Any static HTTP server** (Scalingo, Netlify, public WebDAV…)

---

## Fichiers / Files

| Fichier | Description |
|---|---|
| `widget_multifield_viewer.html` | Widget principal / Main widget file |

---

## Licence

MIT
