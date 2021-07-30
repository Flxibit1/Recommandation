## .Dotfiles

Alors un peu de digrèssion ici mais je voulais vous en parler parce que cela peut vous intéresser si comme moi vous utilisez plusieurs machines ou si comme moi vous utilisez une version de Linux pour vos machines de développement. 

Le système Linux utilise un paradigme très important, l'ensemble des éléments qui constituent le système d'exploitation ainsi que les programmes qui tournent sur le système sont des fichiers ([Everything is a file](https://en.wikipedia.org/wiki/Everything_is_a_file)); c'est à dire que tout ce avec quoi l'ordinateur peut intéragir est représenté au sein du système d'exploitation par un fichier (du programme gérant l'affichage à celui gérant la communicayion avec les imprimantes par exemple). 

Ainsi, le système utilise des fichiers pour gérer les configurations spécifiques à la machine que vous utilisez. Ces fichiers sont généralement des fichiers texte utilisant une structure similaire au JSON ou au XML. 

Ces fichiers de configurations sont parfois cachés au sein du système de fichiers mais restent accessibles. Ils commencent par un "." (d'où le "Dot" des Dotfiles) et n'apparaissent pas directement dans l'explorateur de fichier de votre distribution mais peuvent être affichés dans le terminal en utilisant la commande "ls -a"¹ dans un dossier. 

Ces fichiers de configuration restant des fichier texte, cela signifie qu'ils peuvent être facilement modifiés par l'utilisateur (ils sont modifiables dans un IDE par exemple). 

Maintenant, en utilisant une autre feature de Linux, les liens symboliques, on peut créer un système de configuration très intéressant.

Dans un système Linux; un lien symbolique est la même chose qu'un raccourcit dans le monde Windows; c'est à dire un fichier qui pointe vers un autre. Cela peut permettre par exemple de déplacer un fichier dans un dossier autre que celui où il a été crée mais sans empêcher les programmes d'accèder à ce fichier.

Ainsi si mon fichier de configuration se trouve dans "/etc/mon_programme/.mon_fichier_de_config", je peut créer un lien symbolique de ce fichier qui pointe vers le dossier "/home/mes_config/mon_fichier_de_config" sans que mon_programme ne cesse de fonctionner car il ne retrouve pas le fichier de config.²

*Mais quel intérêt de faire cela?* 

Cela permet notamment de conserver l'ensemble des configurations de vos programmes dans un seul et même dossier; ainsi, plus besoin de chercher où se trouve le fichier de configuration pour tel ou tel programme.

De plus, cela permet également de versionner vos fichier de configuration. En utilisant un système tel que GIT cela peut également permettre de sauvegarder sur une forge vos fichiers de configuration et de permettre un déployement vers un autre système plus simple en cas de problème avec votre machine. 
De plus, on peut imaginer que vous utilisez un système de branches en fonction des machines ou même des projets sur lesquels vous travaillez.

Par exemple, j'ai une branche de mes fichiers de config dédié au développement web qui modifie les fichiers de config de mon IDE afin de lui faire installer et configurer certaines extensions que je n'utilse que dans ce cas précis.   

Vous pouvez utiliser un script bash afin de configurer automatiquement une nouvelle machine en installant les programmes que vous souhaitez mais en les configurant dans le même temps en créant les liens symboliques pointant vers vos .dotfiles. 

Enfin, je vous donne quelques ressources pour voir comment ces dotfiles sont utilisés par d'autres: 
- [Dotphiles.io](http://dotfiles.github.io), qui héberge notamment des dizaines de repository présentant des configurations via des Dotfiles. 
- [The Missing Semester Dotfiles](https://github.com/missing-semester/missing-semester/blob/master/_2019/dotfiles.md), le chapitre 2019 sur les Dotfiles de l'excellent cours [The Missing Semester](https://missing.csail.mit.edu) dont on a déjà parlé [ici](The_Missing_Semester.md).


---
¹ Je vous invite à consulter le manuel (en utilsant la commande "man ls" (Si vous n'arrivez pas à quitter le manuel; tapez ":q")) pour la commande "ls" pour comprendre comment cette commande fonctionne. 

² Pour créer un lien symbolique, vous devez utiliser la commande "ln" suivit du flag "-s" qui spécifie que le lien est symbolique (voir la commande"man ln" pour plus d'informations). Ainsi, placez vous dans le dossier où se trouve le fichier de configuration que vous voulez déplacer et utilisez la commande avec cette structure: "ln -s /home/nom_utilisateur/mond_dossier_de_config/nouveau_fichier_de_config nom_du_lien_symbolique". 
Attention néanmoins, le nom du lien symbolique doit être le nom exact du fichier de config que vous voulez remplacer sinon le programme ne le cherchera pas. 