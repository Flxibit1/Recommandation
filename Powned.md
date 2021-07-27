# Les gestionnaires de Mots de Passe
Un gestionnaire de Mot de Passe c'est quoi? 

C'est un ensemble de services (généralement un site internet, une application et une extension de navigateur), qui vous permettent de sauvegarder "efficacement" vos mots de passe.

Si vous stocker vos mots de passe dans une feuille Excel ou que vous avez un seul mot de passe sur tous vos sites (déjà honte à vous!), ensuite ce genre d'outils est fait pour vous!

Ils permettent généralement de stocker vos identifiants et mots de passe en les associants à une URL. 
Quand vous visitez ensuite cette URL, l'extension de navigateur vous propose généralement de remplir automatiquement les champs pour les identifiants et les mots de passe.
Ils permettent généralement de "générer" de manière aléatoire un mot de passe.
Le tout est protégé par un mot de passe "maitre" qui vous permet d'accéder à l'application et de lire les mots de passes alors enregistrés. A terme, le but est de ne se souvenir que de ce mot de passe en particulier et de laisse l'application gérer le reste.

Une synchronisation permet alors de retrouver vos mots de passe partout où vous en avez besoin (mobile, un deuxième ordinateur...).
La procédure de synchronisation est "sécurisée" car le fichier transmis entre les appareils est crypté et lisible uniquement avec votre mot de passe "maitre".

Certains services proposent également de stocker des "notes sécurisées", c'est à dire un fichier texte que vous pouvez librement éditer (il peut permettre de stocker des codes d'accès à des immeubles par exemple).

Il existe plusieurs concurrents, certains payants comme [1Password](https://1password.com/) et d'autres avec des offres "Premium" payantes (et donc une offre "de base" gratuite) comme [Dashlane](https://www.dashlane.com/fr) ou encore mon petit chouchou [Bitwarden](https://bitwarden.com/).
Ces gestionnaires sont souvent disponibles en Français, mais sont suffisament simples d'utilisation pour être compréhensibles.

# [I have been Powned?](https://haveibeenpwned.com/)
C'est un site internet monté par un chercheur en sécurité qui tente de ressencer toutes les adresses email présentes dans les fuites de données. 
Il vous propose donc de rentrer votre adresse email et de la comparer au bases de données que le site a pu récupérer. 
Je vous conseille vivement d'aller vérifier si votre adresse email est présente sur le site (spoiler: elle y est très probablement), et de changer le mot de passe sur le site internet qui est responsable de la fuite de votre adresse email.
Vous trouverez également sur le site une section qui permet de vérifier si votre mot de passe a été compromis ou non (il ne vérifie pas le mot de passe directement mais son "Hash").
Le responsable du site a publié récemment le code source du site (sans les bases de données avec lesquelles il compare vos adresses email/mots de passe) afin de prouver qu'il ne collectait pas de données.
Je ne suis pas allé vérifier le code source, donc je ne peut vous dire si le site est sûr ou non (en même temps le site est connu, si une collecte avait lieu, tous les sites de news de la planète en parlerait).

Disponible en Anglais uniquement, mais assez simple pour être compréhensible sans ça (Rouge c'est pas bon, Vert c'est bon).