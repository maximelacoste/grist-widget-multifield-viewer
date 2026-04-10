# grist-widget-multifield-viewer

> Grist custom widget — multi-field text viewer with tabs, configurable labels and tooltips auto-populated from native Grist column descriptions.  
> Visionneur de champs texte avec onglets, libellés personnalisables et infobulles issues des descriptions natives des colonnes Grist.

---

## 🇫🇷 Français

### Présentation

Widget personnalisé pour [Grist](https://www.getgrist.com/) qui affiche les champs texte d'un enregistrement sélectionné dans une interface à onglets compacte.

Conçu pour des tables contenant plusieurs champs texte longs — avis de spécialistes, commentaires multiples, notes structurées — et pour s'intégrer dans une page multi-vues : la sélection d'une ligne dans une table principale actualise automatiquement le widget.

### Fonctionnalités

* **Vue en onglets** — un onglet par champ, point coloré selon présence de contenu, texte complet dans le panneau
* **Colonnes dynamiques** — détectées automatiquement depuis l'enregistrement, aucune colonne codée en dur
* **Infobulles au survol** — alimentées automatiquement depuis les **descriptions natives des colonnes Grist** (panneau colonne → Description), surchargeables manuellement
* **Libellés personnalisables** — renommer chaque onglet sans modifier les noms de colonnes Grist
* **Colonnes exclues** — masquer des colonnes du widget en un clic, réintégrables à tout moment
* **Réordonnancement** — glisser-déposer pour changer l'ordre des onglets
* **Colonne titre** — choisir la colonne affichée dans la barre (ex. nom de la personne)
* **Options persistées** via `grist.setOption()` (configuration retenue après rechargement)
* **Bilingue** — détection automatique FR / EN selon `navigator.language`
* **Accessible** — rôles ARIA, navigation clavier, focus visible

### Infobulles et descriptions de colonnes

Le widget lit automatiquement les descriptions natives via la table interne `_grist_Tables_column`. Si une colonne possède une description (renseignée dans **Panneau colonne → Description**), elle est automatiquement utilisée comme infobulle au survol de l'onglet.

Tu peux surcharger cette description dans le panneau ⚙️ — la valeur personnalisée prend le dessus et ne sera plus écrasée.

### Installation

1. Dans ta page Grist, ajouter une vue → **Widget personnalisé**
2. Renseigner l'URL du fichier hébergé (voir ci-dessous)
3. Sélectionner l'accès **"Lire l'enregistrement sélectionné"**
4. Lier le widget à ta table principale via **"Données de"**

### Configuration

Clique sur l'icône ⚙️ dans la barre d'onglets pour :

| Option | Description |
|---|---|
| **Colonne titre** | Colonne affichée dans la barre (ex. Nom, Titre) |
| **Colonnes exclues** | Clic pour exclure / réintégrer une colonne |
| **Libellé** | Renommer l'onglet affiché |
| **Infobulle** | Texte au survol (pré-rempli depuis la description Grist si disponible) |
| **Tout cocher / décocher** | Afficher ou masquer tous les champs en un clic |
| **⠿ Glisser-déposer** | Réordonner les onglets |

### Hébergement

Fichier HTML autonome, sans dépendance npm ni étape de build.

* **GitHub Pages** : activer Pages sur ce dépôt (`Settings → Pages → main / root`), utiliser :  
  `https://maximelacoste.github.io/grist-widget-multifield-viewer/widget_multifield_viewer.html`
* **Tout serveur HTTP statique** (Scalingo, Netlify, WebDAV public…)

---

## 🇬🇧 English

### Overview

A Grist custom widget that displays text fields from a selected record in a compact tabbed interface.

Designed for tables with multiple long text fields — specialist opinions, structured notes, multiple comments — and for multi-view pages: selecting a row in the main table automatically updates the widget.

### Features

* **Tabs view** — one tab per field, colored dot indicating content presence, full text in the panel
* **Dynamic columns** — auto-detected from the record, no hardcoded column names
* **Hover tooltips** — auto-populated from **native Grist column descriptions** (column panel → Description), manually overridable
* **Customizable labels** — rename tabs without changing Grist column names
* **Excluded columns** — hide columns from the widget in one click, re-includable at any time
* **Reordering** — drag and drop to change tab order
* **Title column** — choose which column is displayed in the tab bar
* **Persisted options** via `grist.setOption()` (configuration survives page reload)
* **Bilingual** — automatic FR / EN detection via `navigator.language`
* **Accessible** — ARIA roles, keyboard navigation, visible focus

### Tooltips and column descriptions

The widget automatically reads native column descriptions from Grist's internal `_grist_Tables_column` table. If a column has a description (set in **Column panel → Description**), it is automatically used as the hover tooltip on the tab.

You can override this in the widget's ⚙️ panel — the custom value takes precedence and will no longer be overwritten.

### Setup

1. In your Grist page, add a view → **Custom Widget**
2. Enter the hosted file URL (see below)
3. Select access level **"Read selected record"**
4. Link the widget to your main table via **"Data from"**

### Configuration

Click the ⚙️ icon in the tab bar to configure:

| Option | Description |
|---|---|
| **Title column** | Column displayed in the bar (e.g. Name, Title) |
| **Excluded columns** | Click to exclude / re-include a column |
| **Label** | Rename the displayed tab |
| **Tooltip** | Hover text (pre-filled with native Grist description if available) |
| **Check all / Uncheck all** | Show or hide all fields at once |
| **⠿ Drag & drop** | Reorder tabs |

### Hosting

Single self-contained HTML file — no npm, no build step.

* **GitHub Pages**: enable Pages on this repo (`Settings → Pages → main / root`), use:  
  `https://maximelacoste.github.io/grist-widget-multifield-viewer/widget_multifield_viewer.html`
* **Any static HTTP server** (Scalingo, Netlify, public WebDAV…)

---

## Fichiers / Files

| Fichier | Description |
|---|---|
| `widget_multifield_viewer.html` | Widget principal / Main widget file |

---

## Licence

MIT
