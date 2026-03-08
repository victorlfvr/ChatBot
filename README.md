# Chat Réseau UDP — Java

Projet réseau 3A INFO | Victor LEFEVRE & Bastien MALLET

Application de chat en réseau basée sur une architecture client/serveur UDP (DatagramSocket/DatagramPacket).

---

## Architecture

- **Client** — se connecte au serveur, envoie et reçoit des messages
- **ClientReceiveProcess** — thread d'écoute des messages entrants
- **Server** — gère les connexions et le routage des messages
- **Process** — traite chaque message reçu (privé ou broadcast)

---

## Utilisation

### Démarrage

1. Lancer le serveur en définissant `port_serveur`
2. Lancer le(s) client(s) en renseignant l'IP et le port du serveur
3. Choisir un pseudo au lancement du client

> Même machine : utiliser `127.0.0.1`  
> Plusieurs machines : spécifier l'IP de la machine hébergeant le serveur

### Messages

| Type | Format |
|---|---|
| Message à tous | `texte` |
| Message privé | `pseudoDestinataire/ texte` |

---

## Prérequis

- Java (JDK 8+)
- Tous les clients et le serveur sur le même réseau
