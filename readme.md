Ce projet utilise MkDocs avec le theme Material pour generer le site internet. Le site est deploye automatiquement via GitHub Actions.

Visualiser et modifier le site en local

Pour tester vos modifications sur votre machine avant de les publier :

Ouvrez votre terminal dans le dossier du projet.

Activez l'environnement virtuel Python :
source venv/bin/activate

Lancez le serveur de developpement local :
mkdocs serve

Ouvrez votre navigateur a l'adresse suivante : http://127.0.0.1:8000/

Note : Le site s'actualise automatiquement dans le navigateur a chaque fois que vous sauvegardez un fichier dans le dossier docs/. Pour arreter le serveur local, faites Ctrl + C dans le terminal.

Publier les modifications sur GitHub

Une fois que vos modifications locales vous conviennent, suivez ces etapes pour les envoyer sur le serveur.

Important : Ne jamais ajouter ou pusher les dossiers site/ ou venv/. Ils sont automatiquement ignores par le fichier .gitignore.

Verifiez le statut de vos fichiers modifies :
git status

Ajoutez vos modifications (fichiers sources uniquement) :
git add docs/ mkdocs.yml

Enregistrez vos modifications avec un message clair :
git commit -m "Mon message decrivant les modifications"

Envoyez les modifications sur GitHub :
git push origin main

Verifier la mise en ligne

Apres avoir effectue votre git push :

Rendez-vous sur votre depot en ligne : https://github.com/pellierd/miai-hubot-chair

Cliquez sur l'onglet Actions en haut de la page.

Verifiez le workflow en cours :

Icone orange / jaune : Le site est en cours de compilation et de deploiement (attendre 1 a 2 minutes).

Icone verte : Le deploiement a reussi. Votre site est officiellement a jour en ligne !

Icone rouge : Une erreur est survenue (consultez les logs de l'Action pour voir le probleme, souvent une erreur de syntaxe dans le fichier mkdocs.yml).
