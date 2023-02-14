---
layout: page
title: Utiliser le générateur de mail pour demande de stage
importance: 1
---

Si vous souhaitez gagner du temps dans vos demandes de stages, action souvent chronophage et répétitive, pourquoi ne pas utiliser un bot python pour le faire ? Sur cette page, je vais vous décrire comment faire usage du bot que j'ai conçu.

# Python
Tout d'abord, assurer vous de bien avoir Python d'installé sur votre machine ainsi qu'un éditeur de code (je vous recommande ici [Sublime Text](https://www.sublimetext.com/) mais rien ne vous y oblige).

# Le bot

J'ai crée au fil des années mon propre bot qui me sert grandement à gagner du temps lors de mes demandes de stages. Il vous sera simplement demander de disposer d'une email afin que le bot puisse en faire usage pour envoyer des mails ansi que d'un accès SMTP à celle-ci. Cet accès est facilement trouvable après quelques recherches et est souvent utilisé pour faire usage de certains services tel que ThunderBird.

## Usage
Pour utiliser le bot,

1. Rendez-vous sur [la page](https://github.com/mpek29/internshipEmailGenerator) GitHub de celui-ci.

2. Faites un "git clone" OU Appuyer sur "Code" puis "Download ZIP".

3. Ouvrez "main.py" avec votre editeur de code et compléter les champs "username", "password", "smtp_server", "port".

4. Compléter "attachment" avec le nom du PDF que vous souhaitez joindre (un CV par exemple) si ce n'est pas le cas vous pouvez commenter les lignes qui y font référence. Attention, le fichier PDF devra etre déposé dans le même répertoire que le fichier "main.py".

5. Ouvrez processing.py et dans la fonction body remplacer le texte par le votre. À des fins de personnalisation, vous pourrez insérer le nom, le mail et la specialitée de l'entreprise.

6. Remplissez le fichier companies.csv à l'aide d'un logiciel tel que LibreOffice Calc (je vous propose de faire un premier test avec votre propre email et celle de vos amis).

7. Vous pouvez désormais executer le fichier Python "main.py" (la démarche est aisément trouvable en ligne).
