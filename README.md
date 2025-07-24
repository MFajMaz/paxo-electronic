![logo](https://github.com/paxo-phone/paxo-electronic/assets/45568523/3084b431-1ca6-4c1e-95bb-b80da2699dba)

Ce répertoire rassemble tous les fichiers relatifs au hardware du projet Paxo (plans, modèles 3D etc.) permettant à chacun d'étudier le fonctionnement du téléphone et / ou de le fabriquer chez soi. 

# Schéma
Disponible en PDF ici: [https://github.com/paxo-phone/paxo-electronic/blob/main/schematic.pdf](https://github.com/paxo-phone/paxo-electronic/blob/main/schematic.pdf)
Et sur ovhlab ici: [https://oshwlab.com/gabriel.rochet/paxo-phone-5-r1](https://oshwlab.com/gabriel.rochet/paxo-phone-5-r1)

# Architecture générale

Voici la liste de tout les composants présent sur le **Pcb** du Paxo : 

**ESP32-WROVER-B**

C’est le microcontrôleur principal, le “cerveau” du téléphone. Doté de deux cœurs cadencés à 240 MHz, il gère tous les calculs, le système d’exploitation, l’affichage à l’écran ainsi que la coordination entre les composants (communication, capteurs, etc.).

**SIMCOM A7682E**

Module 4G qui assure la connectivité réseau : appels, SMS, accès à Internet. Il utilise le micro et le haut-parleur pour la voix, synchronise l’heure avec les antennes, et peut également transmettre des informations comme l’état de la batterie ou la localisation.

**CH340C**

Convertisseur USB vers série (TTL), il permet à l’ESP32 de communiquer avec un ordinateur via USB. Idéal pour le débogage, les mises à jour du firmware et la visualisation des données en temps réel.

**DW01A**

Circuit de protection de batterie Li-ion. Il surveille les tensions de charge et de décharge pour éviter toute surtension, sous-tension ou court-circuit.

**TP4056**

Contrôleur de charge pour batterie Li-ion, il permet de recharger la batterie via le port USB. Il gère la charge en toute sécurité selon un protocole adapté à la chimie de la batterie.

**ME6219C33M5G**

Régulateur de tension qui abaisse la tension de la batterie (3,7 V) à une tension stable de 3,3 V, compatible avec la plupart des composants du téléphone (dont l’ESP32).

**TF-018 (module microSD)**

Module de stockage via carte microSD. Il compense le stockage limité de l’ESP32 en permettant d’enregistrer des fichiers (images, messages, logs système, etc.).

**Écran 320x480 avec tactile capacitif**
Affiche l’interface graphique de l’OS. L’écran tactile permet une interaction intuitive avec le système, comme sur un smartphone classique.

**K2-1806AN-A3DW-04 (bouton Reset)**

Permet de redémarrer manuellement le téléphone. Utile pour les tests ou en cas de blocage logiciel.

**TS-1157-B-A (bouton Home)**

Bouton physique principal servant à revenir à l’écran d’accueil de l’OS ou effectuer des actions contextuelles selon l’interface.

**523450(batterie lithium)**

Cette batterie alimente l’ensemble du téléphone Paxo. Grâce à sa tension de 3,7 V et sa capacité de 1000 mAh, elle fournit suffisamment d’énergie pour faire fonctionner le microcontrôleur ESP32, le module 4G SIMCOM A7682E, l’écran tactile, et les autres composants du téléphone.


# Nous contacter

Vous pouvez nous contacter via notre [site web](https://www.paxo.fr) ou notre [serveur discord](https://discord.com/invite/MpqbWr3pUG).

# En savoir plus

Visiter [notre site](https://www.paxo.fr) pour en savoir plus sur le projet Paxo.

# Contributeurs 

<a href="https://github.com/paxo-phone/PaxOS-8/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=paxo-phone/paxo-electronic" />
</a>
