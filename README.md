# Brainrot Royale

Un jeu de baston absurde à 2-4 joueurs, dans le navigateur. Onze combattants inventés (une spatule furieuse, un croissant kamikaze, une pantoufle terrible…), des objets qui tombent du ciel et une arène qui rétrécit.

**Jouer :** https://troplife56-source.github.io/Brainrot-Baston/

## Modes

- **Même appareil** : jusqu'à 4 joueurs sur un clavier (ou J1 au joystick tactile sur téléphone), les places vides peuvent être des bots.
- **En ligne** : un joueur crée une partie et envoie le code de 4 lettres, les autres le tapent dans l'onglet « En ligne ». Pas besoin de compte. Le téléphone ou l'ordinateur de l'hôte fait tourner la partie.
- **Entraînement** : toi contre un mannequin, pour tester les persos.

Réglages : chacun pour soi, 2 contre 2 ou Pizza Bomba ; arène nappe, pizza géante ou patinoire ; vitesse, vies, manches, objets et force des bots.

## Commandes

| | Bouger | Attaque | Dash | Chambrer |
|---|---|---|---|---|
| J1 (AZERTY) | Z Q S D | A | E | X |
| J2 | Flèches | Entrée | Maj droite | Ctrl droit |
| J3 | T F G H | R | Y | V |
| J4 | I J K L | U | O | N |
| Souris (J1) | le perso suit le curseur | A ou clic gauche | clic droit ou Espace | X |

**Super attaque** : attaque + dash en même temps quand la jauge dorée est pleine (touche E à la souris, bouton Super sur téléphone).

## Technique

Tout le jeu tient dans `index.html` (HTML, CSS et JavaScript sans dépendance à installer). Le mode en ligne utilise [PeerJS](https://peerjs.com/) : les appareils se connectent directement entre eux en WebRTC, sans serveur à gérer. Sur certains réseaux très verrouillés (wifi d'école ou d'entreprise), la connexion peut échouer.
