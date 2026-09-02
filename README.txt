APRILTAG ANDROID + CHROME V1
===============================

IMPORTANT
---------
Chrome ne donne pas toujours accès à la caméra pour un fichier ouvert directement
depuis le gestionnaire de fichiers (file://).

Cette version est conçue pour être ouverte depuis:
  http://localhost:PORT
ou une page HTTPS.

METHODE SIMPLE AVEC TERMUX
--------------------------
1. Installer Termux depuis une source fiable.
2. Copier le dossier AprilTag_Android_Chrome_V1 dans un dossier accessible.
3. Dans Termux:
   pkg update
   pkg install python
   cd /chemin/vers/AprilTag_Android_Chrome_V1
   python -m http.server 8080 --bind 127.0.0.1

4. Dans Chrome Android, ouvrir:
   http://127.0.0.1:8080

5. Appuyer sur "Autoriser la caméra".
6. Chrome doit afficher la demande native d'accès à la caméra.

ATTENTION
---------
Si Chrome refuse encore la caméra, vérifier:
Chrome > Paramètres > Paramètres des sites > Caméra
et vérifier que l'accès est autorisé.

ETAT V1
-------
- caméra arrière
- demande de permission via getUserMedia
- affichage vidéo
- FPS
- interface ID / X / Y / distance
- API updateTags() prête pour le moteur AprilTag

Le détecteur AprilTag réel doit encore être branché au flux vidéo.
