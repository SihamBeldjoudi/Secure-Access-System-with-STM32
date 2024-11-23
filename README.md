# **Système d'accès sécurisé avec STM32**

Ce projet implémente un système d'accès sécurisé basé sur un mot de passe, conçu avec un microcontrôleur **STM32F401RE**. Le système permet de contrôler l'accès via un clavier matriciel et fournit un retour visuel avec un écran LCD et des LEDs. Un moteur (simulant une serrure électronique) est activé lorsque le mot de passe correct est saisi.

## **Fonctionnalités principales**
- **Saisie sécurisée du mot de passe** : Un clavier matriciel (4x4) permet à l'utilisateur d'entrer un mot de passe.
- **Vérification du mot de passe** : Le microcontrôleur compare l'entrée utilisateur avec un mot de passe prédéfini.
- **Retour visuel** : 
  - Un écran LCD affiche les instructions et le statut (par exemple : "Entrez le mot de passe", "Accès autorisé").
  - Une LED verte s'allume en cas de mot de passe correct.
- **Activation du moteur** : Un moteur DC est activé via un driver L293D, simulant l'ouverture d'une porte.
- **Extensibilité** : Peut être étendu avec d'autres technologies comme RFID ou communication Bluetooth.

## **Technologies utilisées**
- **STM32CubeMX** : Utilisé pour configurer les broches du STM32F401RE et générer le code d’initialisation.
- **Proteus 8 Professional** : Simulation du circuit, incluant le clavier, l’écran LCD, la LED et le moteur.
- **Microcontrôleur STM32F401RE** : Cœur du système, assurant le traitement des entrées et la gestion des périphériques.

## **Schémas et capture d’écran**
### **Schéma électronique dans Proteus**
![Schéma Proteus](5.PNG)

### **Configuration des broches dans STM32CubeMX**
![Configuration des broches](configuration.PNG)

## **Comment utiliser ce projet ?**
1. **Simulation dans Proteus** :
   - Ouvrez le fichier de simulation dans Proteus.
   - Lancez la simulation pour tester le fonctionnement.
2. **Déploiement sur STM32** :
   - Importez la configuration CubeMX dans STM32CubeIDE.
   - Compilez et téléversez le code sur une carte STM32F401RE.
3. **Interagir avec le système** :
   - Entrez le mot de passe via le clavier matriciel.
   - Observez le retour visuel (LED, écran LCD).
   - Si le mot de passe est correct, le moteur s'active.

## **Structure du projet**
- **/Proteus** : Contient les fichiers du schéma de simulation dans Proteus.
- **/CubeMX** : Fichiers de configuration pour STM32CubeMX.
- **/Code** : Le code source généré et modifié pour STM32.

## **Améliorations possibles**
- Ajout d'un buzzer pour signaler les erreurs ou succès.
- Mise en place d'une double authentification avec RFID ou biométrie.
- Connexion Bluetooth/Wi-Fi pour contrôler et surveiller le système à distance.
- Verrouillage temporaire après plusieurs échecs.

