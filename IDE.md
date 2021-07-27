# Réfléchissez à vos outils, l'IDE
Déjà petit disclaimer, ce que je vais raconter est assez personnel (Comprenez, c’est mon point de vue), et si vos outils vous conviennent, zapper ce post.
Bien, on va commencer par les IDE ; alors, un IDE c’est quoi ? D’après [Wikipédia](https://fr.wikipedia.org/wiki/Investissement_direct_%C3%A0_l%27%C3%A9tranger), un IDE c’est un Investissement Direct à l’Etranger… 
*Regarde ces notes*
Ah non, c’est pas ça !

Donc un [IDE](https://fr.wikipedia.org/wiki/Environnement_de_d%C3%A9veloppement#Environnements_de_d%C3%A9veloppement_int%C3%A9gr%C3%A9), c’est un environnement de développement. 
C’est à dire un logiciel qui peut être utilisé pour développer des programmes informatiques. 

Un IDE intègre généralement 4 programmes principaux:
- un éditeur de texte (la page qui va afficher votre fichier de code)
- un compilateur (le logiciel qui va transformer votre code informatique en langage machine)
- un débugger (généralement associé au compilateur et qui permet de faire tourner votre programme étape par étape (en suivant en réalité chacune des lignes de votre code source)  
- enfin un analyseur de texte (en gros le programme qui rajoute de la couleur sur les mots clés de vos langages (if .. else… par exemple)).

Aujourd’hui un IDE c’est beaucoup plus que ça, ils intègrent des outils de gestion de version (type GIT), des outils de communication collaborative (Slack, Microsoft Teams…), des outils de conception d’interface, de prototypage, de gestion de tests Unitaires…

L’idée est d’avoir un seul programme capable de tout faire, et que le développeur n’ai jamais besoin de le quitter.


Pour citer les plus connus dans cette catégorie, Visual Studio (celui que recommande le CNED pour le C#), Eclipse pour Java, ou encore Code::Blocks pour le C++.
Attention, ce sont de très bon outils hein, mais là j’essaye de vous faire prendre conscience d’un truc.

Le résultat de cette agrégation d’outils?

Ces IDE sont devenus au fil du temps des usine à gaz peu performante et assez intimidante pour un néophyte…
La première fois que ma copine m’a vu en train de bosser sur Visual Studio (pas Code), elle m’a dis ça : "Comment tu fait pour t’y retrouver avec tous ces boutons ?"
Sur le moment j’ai pas tilté, et puis en y réfléchissant, je me suis rendu compte que j’utilisais Visual Studio uniquement parce que c’est celui vu avec le CNED et que c’est celui que je connaissait, mais qu’en réalité je n’ai pas besoin de la moitié des fonctionnalités…
Donc je suis parti à la recherche d’autres outils, d’autres IDE plus léger…

J’ai donc écumé le web à la recherche des "10 meilleurs IDE" ou encore des "5 meilleurs IDE de 2020" (sur une recherche effectué en 2019). (Critiquez pas, on les a tous fait ces sites :p)
Après quelques recherches donc, un nom revenais souvent, les produits [JetBrains](https://www.jetbrains.com/); ils font effectivement de très bon produits, mais une grande partie est payante (et non, si on se respecte on ne "crack"  pas un IDE (pour plein de raisons)) et finalement leurs produits sont assez proches des usines à gaz que peuvent être Eclipse ou Visual Studio (même si ils sont plus léger, on est d'accord).

Et puis j’ai découvert [Visual Studio Code](https://code.visualstudio.com/), une version lite de Visual Studio (je vais l’appeler Code à partir de maintenant).

Quels sont les avantages de Code par rapport à son grand frère Visual Studio et autres IDE ?

Ben pour commencer, Code N’EST PAS un IDE, enfin pas vraiment (on va y venir) ; mais surtout, il n’intègre pas tous les outils de collaboration qui peuvent parasiter votre travail (ou au moins votre interface). Et ensuite, Code (du moins dans sa version de base) n’intègre qu’un simple éditeur de texte.
Il vous faudra donc installer et configurer vous même votre compilateur/debugger ainsi que votre analyseur de texte (si vous en souhaitez un).

*Oui mais pourquoi c’est mieux ? Ca fait plus de boulot non ?*

Alors, oui, et non.
Oui, vous avez plus de boulot à l’installation, il faut tout bien configurer, tout installer et votre premier Hello World qui tourne est une petite victoire ; mais est-ce que vous vous rappelez de la première fois où vous avez installé Visual Studio ou un autre IDE ? 
Les installations de ces outils sont longues, très très longues… et puis elles prennent de la place (35Go environ pour Visual Studio avec les outils pour le C# et le C++. 
De plus, comme beaucoup de choses que vous faites vous même, vous allez apprendre plein de trucs!
Code " prend" 250 Mo sur votre disque, l’ensemble des outils pour le C# et le C++ installé à coté de Code, environ 2,5Go (et en visant large)…
Alors oui, Code a des désavantages, il est pas plug&play, il peut paraître austère, il est basé sur électron ( :face_vomiting: ), mais il est aujourd’hui pour moi indispensable, et en ajoutant quelques plug-in bien choisit (sa grande force), on obtient un véritable IDE, tout aussi puissant et performant que son grand-frère mais bien plus léger !

Si vous voulez aller plus loin encore, vous pouvez partir sur [Vim](https://www.vim.org/) qui est un simple éditeur de texte qui ne peut être directement lié au compileur/debugger (et encore, je suis pas certain qu’un mec a pas fait un plug-in :p ) et qui permet d’éditer tout et n’importe quoi…

Bref, réfléchissez aux outils que vous utilisez, vous serez de meilleurs développeurs !