# Home Assistant - Thème Tempo Énergie

[![Validate with HACS](https://github.com/hekmon/hatempotheme/actions/workflows/hacs.yaml/badge.svg)](https://github.com/hekmon/hatempotheme/actions/workflows/hacs.yaml)

Ce thème Home Assistant change les couleurs des 6 premiers compteurs d'énergie de Home Assistant pour correspondre aux couleurs Tempo :

![Exemple de compteurs d'énergie avec les couleurs tempo](https://github.com/hekmon/hatempotheme/raw/v1.0.0/res/tempo_energy.png)

## Usage

Ce thème se basant sur l'ordre des compteurs assurez-vous d'abord d'avoir configuré votre dashboard Énergie avec les compteurs dans l'ordre suivant :

 1. Bleu Heures Creuses
 2. Bleu Heures Pleines
 3. Blanc Heures Creuses
 4. Blanc Heures Pleines
 5. Rouge Heures Creuses
 6. Rouge Heures Pleines

### Installation

Vous devez tout d'abord [activer](https://hacs.xyz/docs/categories/themes/) la surveillance du dossier `themes` qui sera utilisé par la suite si cela n'est pas déjà fait (pour un autre thème par exemple).

Rajoutez ces lignes dans votre fichier `configuration.yaml` :

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

Redémarrez votre Home Assistant.

#### Avec HACS

[![Ouvre votre instance Home Assistant et ajoute un dépôt dans la boutique communautaire Home Assistant](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=hekmon&repository=hatempotheme&category=theme)

Plus d'informations sur HACS [ici](https://hacs.xyz/).

#### Manuellement

Créez le dossier `themes` au même niveau que votre fichier `configuration.yaml` Home assistant :

 * Si votre fichier de configuration est dans `/path/to/ha/config/configuration.yaml`
 * Vous devez créer le dossier `/path/to/ha/config/configuration.yaml`

Télécharger le fichier `themes/tempo.yaml` de ce repo à l'intérieur du dossier `themes` que vous venez de créer. Vous devez optenir : `/path/to/ha/config/themes/tempo.yaml`

Rendez-vous ensuite dans :
 * Menu `Outils de développement`
 * Onglet `Services`
 * Cherchez le service `Home Assistant Frontend: Recharger les thèmes`
 * Activez le

### Utilisation

#### Thème par défault

Pour définir ce thème par default (et pour tous vos utilisateurs à moins qu'ils aient spécifiquement sélectionné un thème différent) rendez vous dans:
 * Menu `Outils de développement`
 * Onglet `Services`
 * Cherchez le service `Home Assistant Frontend: Définir le thème par défaut`
 * Sélectionner le thème `Tempo Énergie`
 * Décochez le `Mode`
 * Activez le service

#### Par utilisateur

Un utilisateur peut se rendre dans son profil pour activer un thème spécifique différent du thème par défault.
