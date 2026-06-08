# Dashboard-TOUG
Dépôt du Dashboard TOUG comprenant 4 vues : un fichier complet avec les 4 vues, et 2 fichiers plus light avec uniquement soit la vue ECS, soit la vue T.One-Chauffage-Climatisation
# Dashboard TOUG AquaAir pour Home Assistant

Ce dépôt met à disposition mes dashboards Home Assistant pour l'intégration **TOUG AquaAir/ESPHome** développée par @djtef.

## Contenu du dépôt

Le dépôt contient :

### Dashboard complet
- `dashboard_toug_complet_4_vues.yaml`

Contient les 4 vues suivantes :
- Températures extérieure - Thermostats

<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-54-52-613_io homeassistant companion android" src="https://github.com/user-attachments/assets/86f749e7-e351-449c-b334-66585c0d987b" />

  
- Configuration et contôles ECS

<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-55-08-466_io homeassistant companion android" src="https://github.com/user-attachments/assets/9d6a3438-d789-411a-b09d-c578d7e6d17e" />

  
- Programmation horaire chauffage climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-55-16-642_io homeassistant companion android" src="https://github.com/user-attachments/assets/32332aad-822c-49df-811f-d6fcb3100081" />


- Configuration T.One - contrôles Chauffage et Climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-55-26-505_io homeassistant companion android" src="https://github.com/user-attachments/assets/77556718-c52c-4d39-a429-a385f5cbeeff" />
<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-55-37-904_io homeassistant companion android" src="https://github.com/user-attachments/assets/f2b5f36c-4fe8-4394-93e0-0af1fb9ab961" />

### Dashboards allégés

- `dashboard_toug_ecs.yaml`
  - Vue dédiée à la gestion de l'Eau Chaude Sanitaire (ECS)

- `dashboard_toug_T.One_chauffage_climatisation.yaml`
  - Vue dédiée à la configuration générale du T.One, au chauffage et à la climatisation
   
## Pourquoi plusieurs fichiers ?

Les vues :

- Thermostats
- Programmation horaire

ont déjà été documentées et publiées par @djtef sur GitHub qui explique notamment, pour le bon fonctionnement du dashboard de programmation horaire, comment créer un automatisme de mise à jour, des entrées, des scripts de synchronisation.
La procédure de création de ces dashboards ainsi que la mise en place des automatismes, helpers et scripts nécessaires à leur fonctionnement sont détaillées dans l'article :

[👉 TOUG Aldes T.One - Partie 2 : thermostats](https://www.hacf.fr/toug-aldes-t-one-partie-2/#thermostats)

[👉 TOUG Aldes T.One - Partie 2 : Programmation horaire](https://www.hacf.fr/toug-aldes-t-one-partie-2/#programmation-horaire)

Les fichiers allégés permettent donc d'utiliser uniquement les vues complémentaires que j'ai développées autour de l'intégration TOUG AquaAir.

## Prérequis

- Home Assistant
- Intégration TOUG AquaAir/ESPHome de @djtef
- Cartes personnalisées utilisées dans les dashboards :
  - Bubble Card
  - Button Card
  - Weather Forecast
  - Climate Template

Selon votre configuration, certains helpers ou entités devront éventuellement être adaptés.

## Installation

1. Télécharger le fichier YAML souhaité.
2. Ouvrir le tableau de bord Home Assistant.
3. Passer en mode YAML ou utiliser l'éditeur YAML brut.
4. Copier / coller le contenu du fichier.
5. Adapter si nécessaire les noms d'entités à votre installation.

## Remerciements

Un grand merci à **@djtef** pour le développement de la TOUG et le travail réalisé autour de l'intégration TOUG AquaAir/ESPHome du T.One.

Documentation complémentaire :

https://www.hacf.fr/toug-aldes-t-one/

https://www.hacf.fr/toug-aldes-t-one-partie-2/


## Avertissement

Ces dashboards ont été réalisés pour mon installation personnelle et sont partagés à titre d'exemple.

Selon votre version de Home Assistant, votre configuration TOUG ou les cartes personnalisées installées, certaines adaptations devront être nécessaires.
