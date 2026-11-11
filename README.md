# Brainrot Baston

Le jeu de baston des **Brainrots de San Carbonara**, dans le navigateur. Quinze combattants inventés (une spatule furieuse, un croissant kamikaze, une pantoufle terrible, Mattarello le justicier, une olive tireuse d’élite…), des objets qui tombent du ciel et une arène qui rétrécit.

**Jouer :** https://troplife56-source.github.io/Brainrot-Baston/

## En un coup d'œil

- **Accueil** : choisis ton brainrot avec les flèches (ou en glissant le doigt), puis **JOUER** lance tout de suite une partie contre 3 bots.
- **Défi du jour** : un nouveau défi chaque jour (gagner ou faire 3 K.O. avec un perso imposé). Réussis-les à la suite pour faire monter ta série 🔥.
- **Progression** : victoires, K.O., record et série sont gardés sur l'appareil. Trois persos se débloquent : **Mattarello** (1 victoire ou 3 parties), **Olivetta** (10 K.O. au total) et **Grattugia** (1 défi du jour réussi).
- **Sur téléphone** : l'arène prend tout l'écran, la caméra suit l'action et zoome quand l'arène rétrécit. Le jeu s'installe sur l'écran d'accueil (« Ajouter à l'écran d'accueil »).

## Modes

- **Rapide** (bouton JOUER) : toi contre 3 bots.
- **Entre amis** : jusqu'à 4 joueurs sur un clavier (ou J1 au joystick tactile sur téléphone), les places vides peuvent être des bots.
- **En ligne** : un joueur crée une partie et envoie le code de 4 lettres, les autres le tapent dans l'onglet « En ligne ». Pas besoin de compte. Le téléphone ou l'ordinateur de l'hôte fait tourner la partie.
- **Entraînement** : toi contre un mannequin, pour tester les persos.

Réglages (partie perso) : chacun pour soi, 2 contre 2 ou Pizza Bomba ; arène nappe, pizza géante ou patinoire ; vitesse, vies, manches, objets et force des bots.

## Commandes

| | Bouger | Attaque | Dash | Chambrer |
|---|---|---|---|---|
| J1 (AZERTY) | Z Q S D | A | E | X |
| J2 | Flèches | Entrée | Maj droite | Ctrl droit |
| J3 | T F G H | R | Y | V |
| J4 | I J K L | U | O | N |
| Souris (J1) | le perso suit le curseur | A ou clic gauche | clic droit ou Espace | X |

En partie rapide, J1 peut aussi jouer avec les flèches et Entrée.

**Super attaque** : attaque + dash en même temps quand la jauge dorée est pleine (touche E à la souris, bouton Super sur téléphone).

## Statistiques (Google Analytics)

Le jeu envoie quelques événements pour savoir ce qui plaît : `play` (type de partie, perso), `match_end` (résultat, place, K.O., durée), `rematch`, `daily_done`, `unlock`, `share`, `channel_click`, `online_create`, `online_join`, `open_party`, `open_online`.

## Technique

Tout le jeu tient dans `index.html` (HTML, CSS et JavaScript sans dépendance à installer). `manifest.webmanifest` et les icônes permettent de l'ajouter à l'écran d'accueil, et `preview.png` est l'image affichée quand on partage le lien. Le mode en ligne utilise [PeerJS](https://peerjs.com/) : les appareils se connectent directement entre eux en WebRTC, sans serveur à gérer. Sur certains réseaux très verrouillés (wifi d'école ou d'entreprise), la connexion peut échouer.

Pour changer le lien de la chaîne YouTube affiché dans le jeu, modifie la constante `CHANNEL_URL` en haut du script.
