# Exercices Distributed Ledger Technology #

## _Comment est géré le cas où le nombre de transactions dans le Block à valider est impair pour générer un Merkle root ?_

Comme on peut le voir dans l'exemple ci-dessous, dans le cadre d'une concaténation, le nombre d'empreintes (**hashes**) affichées étant impair (voir à droite de l'image), on combine alors la dernière empreinte avec elle-même. Dans le cas présent, **hEF** sera dupliquée afin de calculer **hEFEF**.

![Ceci est une image](https://cryptoast.fr/wp-content/uploads/2020/05/arbre-de-merkle-exemple.png) 

## _Dans le réseau bitcoin, comment un nouveau noeud arrive t'il à retrouver ses pairs et ainsi rejoindre le réseau ?_

Lorsqu'un nouveau nœud souhaite accéder au réseau, il doit se connecter à un nœud d'amorçage, qui est un client Bitcoin toujours actif et doté d'une adresse IP statique. Ce client fonctionne comme une passerelle vers le réseau Bitcoin, étant l'une des premières connexions établies par les clients Bitcoin au début. Ainsi n'importe quel utilisateur de l'internet peut devenir un noeud du réseau en téléchargeant le registre auprès d'un noeud existant.  

## _Pouvez vous nommer au moins une personne qui a ou aurait pu influencer directement ou indirectement la création de Bitcoin par ses travaux (une personne qui n'a pas été nommée dans le cours)?_ 

J'aimerais aborder ici le cas de Herr Friedrich Hayek, économiste, penseur politique du XXème siècle, prix nobel d'économie, britannique et originaire d'Autriche.

![Ceci est une image](https://i.pinimg.com/originals/4b/a1/fb/4ba1fb7aae2b9c1ca86bc80a7e3e9380.jpg)

Il a travaillé dans le domaine de l'information. Il est issu de la pensée de l'Ecole Autrichienne.

En ce qui nous concerne, son ouvrage intitulé _"Pour une vraie concurrence des monnaies"_ publié en 1976 est considéré par certains comme étant une des oeuvre ayant pu influencer certains créateurs de crypto-monnaies telles que le Bitcoin.
On peut citer par exemple la Banque Centrale Européene qui déclare ainsi, je cite : _"les racines théoriques du Bitcoin peuvent être trouvées dans l'École autrichienne d'économie et ses critiques du système actuel de monnaie fiduciaire"_

Je vous invite d'ailleurs à écouter ce podcast de FranceCulture intitulé _"Bitcoin : la prophétie de Friedrich Hayek"_ :

"https://www.franceculture.fr/player/export-reecouter?content=c28671f4-e5fe-4f81-ad66-81bb2a33f53e"

## _Avec vos propres recherches et grâce aux compétences acquises en cours pouvez vous expliquer comment une Blockchain crée un lien entre ses différents Blocks?_

Chaque bloc est validé par certains utilisateurs baptisés « mineurs » (en référence aux chercheurs d'or), et sont transmis aux « noeuds » du réseau, c'est-à-dire aux détenteurs du registre, ce registre étant la chaîne de blocs elle-même. Cette dernière est actualisée en permanence.

Lorsqu'un noeud crée ou reçoit un nouveau bloc, il l'ajoute à sa copie du registre puis le transmet à ses noeuds pairs. Quand ceux-ci le reçoivent, ils vérifient que ce nouveau bloc est valide, c'est-à-dire qu'ils veillent en particulier à ce que la somme des transactions soit égale en entrée et en sortie. Si le bloc est valide, ils l'intègrent alors à leur registre et le transmettent à leur tour à leurs pairs. À l'échelle planétaire, _« il y a forcément une à vingt secondes de latence pour que le bloc se diffuse dans tout le réseau »_, selon Bilal Chouli, fondateur de Neurochain.

![Ceci est une image](https://bitpanda-academy.imgix.net/nullb38f6ebe-fd30-4a85-b1b2-1f585c236a91/Bitpanda-Infographics_3-blockchain.png?auto=compress%2Cformat&fit=min&fm=jpg&q=80&w=2100)  

## _Quelle structure de données informatique peut représenter le mieux cette chaine de Block: https://en.wikipedia.org/wiki/List_of_data_structures ?_

On pourrait faire le rapprochement avec la linked list: https://en.wikipedia.org/wiki/Linked_list

## _Si je souhaite modifier une transaction de 10 bitcoin que j'ai effectué il y a 6 mois en une transaction de 1 Bitcoin, que dois je modifier dans la Blockchain et que dois je mettre en oeuvre pour que cette modification persiste ?_
## _Est ce possible selon vous ?_

Du tout, en l'état tout du moins, l'immutabilité à travers les registres et la disposition des blocs avec l'arbre de Merkle ainsi présenté plus haut fait en sorte que la moindre altération des transactions est tout de suite visible et reportée.