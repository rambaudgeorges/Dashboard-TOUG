# Dashboard-TOUG-V2

Après utilisation du dashboard-TOUG-V1, j'ai un peu réorganisé les entités pour que ce soit plus convivial. Par contre il est un peu plus long à mettre en place, notamment en ce qui concerne la vue Consommations et coûts qui nécessite de créer en mode UI 18 Entrées dont 12 compteurs de services et 6 capteurs template. 
J'ai fait ce choix car les entités de consommations ne sont pas réinitialisées tous les ans mais seulement lors de certaines maintenances comme lors de la mise à jour du Firmware.
L'entité "Reset Consommation" permet par contre de réinitialiser tous les ans les consommations si vous le souhaitez, avec un automatisme ou manuellement.
Ce dépôt du Dashboard TOUG-V2 comprend 5 vues : un fichier complet avec les 5 vues, et 3 fichiers plus light avec uniquement soit la vue T.One-Chauffage-Climatisation, soit la vue ECS, soit la vue Consommations et coûts

# Dashboard TOUG AquaAir pour Home Assistant

Ce dépôt met à disposition mes dashboards Home Assistant pour l'intégration **TOUG AquaAir/ESPHome** développée par @djtef.

## Contenu du dépôt

Le dépôt contient :

### Dashboard complet
- `dashboard_toug_complet_5_vues.yaml`

Contient les 5 vues suivantes :

- Configuration T.One - contrôles Chauffage et Climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-13-17-24-19-746_io homeassistant companion android" src="https://github.com/user-attachments/assets/2ebb61b5-3e86-4fed-98c2-4b4f3d9fdf8d" />

Ici on voit bien que les chambres ont dépassé la température de consigne (26°) en climatisation  et que les bouches se sont fermées (couleur gris foncé) lorsque la température a atteint 25,6°. J'aime bien les cartes Bubble Card pour les thermostats, car elles donnent parfaitement leur état ainsi que celui de la bouche associée. Par exemple en mode ventilation il apparaît l'icône d'un ventilateur au lieu de celui du froid (en Mode Air Ventilation, ou au début et à la fin du cycle de climatisation).


- Configuration et contôles ECS

<img width="2136" height="3200" alt="Screenshot_2026-06-13-12-11-21-510_io homeassistant companion android" src="https://github.com/user-attachments/assets/5f782d44-19e3-4fa6-9dff-8e42b5b5fa1a" />



- Températures extérieures - Thermostats

<img width="2136" height="3200" alt="Screenshot_2026-06-13-12-11-29-196_io homeassistant companion android" src="https://github.com/user-attachments/assets/baddbec4-50bf-47e8-a1a5-8cd6debbcca6" />


  
- Programmation horaire chauffage climatisation

<img width="2136" height="3200" alt="Screenshot_2026-06-13-12-11-37-401_io homeassistant companion android" src="https://github.com/user-attachments/assets/57a671f6-7604-469e-b221-75d35d31b550" />




- Consommations et coûts

<img width="2136" height="3200" alt="Screenshot_2026-06-13-12-11-45-744_io homeassistant companion android" src="https://github.com/user-attachments/assets/b7416eaa-deda-4380-bc79-915d010f6186" />




### Dashboards allégés à intégrer dans une nouvelle vue et/ou section d'un dashboard existant


- `dashboard_toug_T.One_chauffage_climatisation.yaml`
  - Vue dédiée à la configuration générale du T.One, au chauffage et à la climatisation

- `dashboard_toug_ecs.yaml`
  - Vue dédiée à la gestion de l'Eau Chaude Sanitaire (ECS)

- `dashboard_toug_consommations_couts.yaml`
  - Vue dédiée à la mise en page des entités de consommations et des coûts nécessitant de créer en mode UI 18 Entrées dont 12 compteurs de services des consommations et 6 capteurs template pour les coûts.

<img width="1472" height="1896" alt="image" src="https://github.com/user-attachments/assets/7e0a1fff-30f4-4a05-a4dd-d32c3046e832" />
 
 
#  Exemple de création d'une Entrée de Compteur de services


<img width="1513" height="1885" alt="image" src="https://github.com/user-attachments/assets/8a30864d-23a5-49e7-89a2-2ddc16cc0c87" />


<img width="893" height="1689" alt="image" src="https://github.com/user-attachments/assets/6320710b-ae4f-409a-b317-87ba9ba85676" />



#  Exemple de création d'une Entrée de capteur template

<img width="911" height="1069" alt="image" src="https://github.com/user-attachments/assets/8db10170-837f-4f64-aafd-80f238e5c12c" />

<img width="882" height="1506" alt="image" src="https://github.com/user-attachments/assets/a99b8f65-096e-461b-88a7-d4828ee5a286" />

<img width="800" height="1800" alt="image" src="https://github.com/user-attachments/assets/447c3494-3a68-44e0-8038-97d0ad260996" />

   
## Pourquoi plusieurs fichiers de dashboards ?

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
