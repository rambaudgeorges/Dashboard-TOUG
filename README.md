# Dashboard-TOUG-V1

Ce dépôt du Dashboard-TOUG-V1 comprend 4 vues : un fichier complet avec les 4 vues, et 2 fichiers plus light avec uniquement soit la vue ECS, soit la vue T.One-Chauffage-Climatisation

# Dashboard TOUG AquaAir pour Home Assistant

Ce dépôt met à disposition mes dashboards Home Assistant pour l'intégration **TOUG AquaAir/ESPHome** développée par @djtef.

## Contenu du dépôt

Le dépôt contient :

### Dashboard complet

- `dashboard_toug_complet_4_vues.yaml`

Contient les 4 vues suivantes :
- Températures extérieure - Thermostats

<img width="2136" height="3200" alt="Screenshot_2026-06-08-18-38-56-384_io homeassistant companion android" src="https://github.com/user-attachments/assets/fe714d2b-b489-4183-8b50-67ac47bbe1a4" />

  
- Configuration et contôles ECS

<img width="2136" height="3200" alt="Screenshot_2026-06-08-19-02-47-376_io homeassistant companion android" src="https://github.com/user-attachments/assets/07788e2e-8b35-4645-b8f2-bcd7147f3442" />

  
- Programmation horaire chauffage climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-07-21-55-16-642_io homeassistant companion android" src="https://github.com/user-attachments/assets/32332aad-822c-49df-811f-d6fcb3100081" />


- Configuration T.One - contrôles Chauffage et Climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-08-20-07-18-298_io homeassistant companion android" src="https://github.com/user-attachments/assets/ee24f65f-3026-4b49-a926-4337ac47edeb" />


### Dashboards allégés à intégrer dans une nouvelle vue et/ou section d'un dashboard existant

- `dashboard_toug_ecs.yaml`
  - Vue dédiée à la gestion de l'Eau Chaude Sanitaire (ECS)

- `dashboard_toug_T.One_chauffage_climatisation.yaml`
  - Vue dédiée à la configuration générale du T.One, au chauffage et à la climatisation
 
Il est intégré dans ces deux vues des entités de consommations et de coûts issues directement du T.One sans compteurs de services ni modèles de capteurs. 
Ces consommations ne sont pas annuelles, elles sont cumulatives et réinitialisées uniquement lors de certaines maintenances, notamment lors de la mise à jour du micrologiciel.
Mais vous avez la possibilité d'utiliser l'entié "Reset Consommation" dans un automatisme pour réinitialiser ces données tous les ans le 1er janvier à 00:00:00
   
## Pourquoi plusieurs fichiers ?

Les vues :

- Thermostats
- Programmation horaire

ont déjà été documentées et publiées par @djtef sur GitHub qui explique notamment, pour le bon fonctionnement du dashboard de programmation horaire, comment créer un automatisme de mise à jour, des entrées, des scripts de synchronisation.
La procédure de création de ces dashboards ainsi que la mise en place des automatismes, helpers et scripts nécessaires à leur fonctionnement sont détaillées dans l'article :

[👉 TOUG Aldes T.One - Partie 2 : thermostats](https://www.hacf.fr/toug-aldes-t-one-partie-2/#thermostats)

[👉 TOUG Aldes T.One - Partie 2 : Programmation horaire](https://www.hacf.fr/toug-aldes-t-one-partie-2/#programmation-horaire)

Les fichiers allégés permettent donc d'utiliser uniquement les vues complémentaires que j'ai développées autour de l'intégration TOUG AquaAir. ATTENTION ce sont des vues dont le yaml commence par "type: grid" et non pas par "views:", à intégrer donc dans une nouvelle vue d'un dashboard existant.

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
