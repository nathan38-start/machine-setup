fichier de configuration d'une machine sous ubuntu pour le développement web 
========
parti une installation e de WSL et ubuntu 

========
Installation de WSL2
========
Pour installer wsl2 il faut lancer powershell en tant qu'administrateur et taper la commande wsl --install

Installation d'ubuntu 
========
Pour installer Ubuntu, il faut se rendre dans le Microsoft store et ensuite recherche ubuntu et l'installer. 

installation de WSL sur VSCode 
========
Pour installer WSL sur VSCode, il faut installer l'extention WSL-Developper dans le gestionnaire d'extention de vscode. 


Configuration de Git sur Ubuntu 

========
Pour configurer git, notre intervenant nous a demandé de créer le répertoir principal dev et le sous-répetoir setup (qui se situ dans dev) avec la commande mkdir 
ensuie, une foit  placé dans le sous-répertoir setup il faillait initialiser git avec la commande git init.
Puis, il fallait créer le fichier note.md avec la commande touch. 
ensuite, il faillait utiliser la commande git status pour voir le status de synchronisation du sous-répertoir setup sur git 
puis, il fallait pouvoir effectuer le premier commit avec la commande git commit -m "first-commit"
Un message est apparu pour nous informer que nous n'avions pas configurer le nom de l'utilisateur et de son adresse mail, il fallait utiliser les commandes git config --global user.email "nathan.varin@outlook.fr" et git config --global user.name "nathan"
Une fois cette étape effectué, on peut faire le premier commit de notre répertoir setup dans git avec la commande git commit -m "first-commit"
ensuite, on utilise la commande git status.

Génération et ajout  d'une clé ssh dans git 

============
pour générer notre clé ssh pour git il faut utiliser la commande ssh-keygen -t ed25519 -C "nathan.varin@outlook.fr"
ensuite, avant d'ajouter notre clé ssh à l'agent ssh pour la gestion des clés, il faut vérifier les clés ssh existantes et pouvoir en généné une en utilisant la commande $ eval "$(ssh-agent -s)"
il faut ensuite, ajouter notre clé privée SSH au ssh agent, il faut utiliser la commande ssh-add ~/.ssh/id_ed25519 
pour copier la clé ssh publique il faut utiliser la commande cat ~/.ssh/id_ed25519.pub
ensuite, il faut se connecter à notre compte github pour ajouter notre clé ssh.

=========
Test de la connection ssh à notre compte github 
pour tester la connexion ssh, il faut utiliser la commende ssh -T git@github.com

