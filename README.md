# programmation-oriente-objet

## Sommaire
1. [Intro](#Paradigme-orienté-objet)
2. [Objet](#Objet)
3. [Encapsulation](#Encapsulation)
4. [Interface, Implémentation et Remplaçabilité](#Interface,-Implémentation-et-Remplaçabilité)
5. [Classes et Instances](#Classes-et-Instances)
6. [Attributs et Méthodes](#Attributs-et-Méthodes)
7. [Les Méthodes](#Les-Méthodes)
8. [Constructeur, Destructeur et Accesseur](#Constructeur,-Destructeur-et-Accesseur)
9. [Éléments Statiques](#Éléments-Statiques)
10. [Extension](#Extension)
    - [Propriétés](#Propriétés)
    - [Polymorphisme](#Polymorphisme)
    - [Héritage](#Héritage)
    - [Redéfinition et Surcharge](#Redéfinition-et-Surcharge)
    - [Classes Abstraites et Interfaces](#Classes-Abstraites-et-Interfaces)
    - [La Délégation](#La-Délégation)
    - [Le Sous-typage](#Le-Sous-typage)
11. [Projets](#Projets)



## Paradigme orienté objet

Le paradigme orienté objet est une approche de programmation qui cherche à résoudre l'état global des langages impératifs en introduisant des concepts tels que les objets distincts et les interfaces homme-machine.

Dans le paradigme orienté objet, les programmes sont construits autour d'objets distincts. Chaque objet possède son propre comportement, défini par ses méthodes et fonctions. Cela permet de modéliser le monde réel de manière plus précise et de représenter les entités du problème de manière individualisée.

Les objets dans le paradigme orienté objet interagissent entre eux en se communiquant des messages. Ces messages sont envoyés d'un objet à un autre pour déclencher des actions spécifiques. Cette communication entre objets permet une collaboration efficace et une division claire des responsabilités.

Contrairement aux langages impératifs, où l'état global est omniprésent, dans le paradigme orienté objet, chaque objet détient son propre état. L'information et le comportement d'un objet sont encapsulés, ce qui signifie que seule l'objet lui-même peut modifier son état. L'état d'un objet n'est pas visible depuis l'extérieur, favorisant ainsi l'encapsulation et l'isolation.

Le paradigme orienté objet permet d'adopter des approches spécifiques pour résoudre différents types de problèmes. Certains langages orientés objet sont conçus pour être plus adaptés à certains problèmes, grâce à leurs fonctionnalités spécifiques. Cela permet aux développeurs de choisir le langage qui convient le mieux à leur contexte particulier.

De nos jours, de plus en plus de langages de programmation sont conçus pour prendre en charge plusieurs paradigmes, y compris l'orientation objet. De plus, des plates-formes multi-langages sont également disponibles, permettant aux développeurs d'utiliser différents langages dans le même projet. Cette flexibilité offre des possibilités étendues pour résoudre les problèmes de manière efficace et adaptée.

## Objet

L'objet dans le paradigme orienté objet est une entité autonome et isolée du reste du programme, avec un état masqué qui n'est pas directement accessible pour la lecture ou la modification. Il est manipulé par un comportement, contenant à la fois des données et des méthodes pour manipuler cet état. L'objet lui-même est responsable de son état, et on ne peut manipuler cet état qu'à travers les fonctions qui lui sont associées, garantissant ainsi l'exactitude des opérations. L'objet dépend uniquement de son propre état, similaire au paradigme fonctionnel, et l'état global correspond à la somme des états individuels des objets. L'isolation des objets, grâce à l'encapsulation, facilite le raisonnement sur le programme, tandis que le comportement de l'objet est mis à disposition pour interagir avec les autres parties du programme.

## Encapsulation

L'état, représentant les données, et le traitement, constitué des fonctions, sont regroupés dans une entité unique appelée objet, dont les détails internes sont masqués, comme une boîte opaque. L'interface d'un objet expose les moyens de communication avec lui, sans révéler les détails internes. Cela permet d'éviter les fuites d'information et confère une responsabilité unique à chaque objet, avec les interactions entre objets se faisant par le biais des interfaces. Le principe "tell, don't ask" encourage à déléguer les décisions à l'objet lui-même plutôt que de lui donner des instructions précises. L'encapsulation, qui englobe le masquage de l'état, facilite la séparation entre l'interface et l'implémentation, où les données et les traitements sont regroupés et isolés de l'extérieur. L'interface expose les fonctionnalités offertes par l'objet, permettant une interaction contrôlée avec celui-ci.

## Interface, Implémentation et Remplaçabilité

L'interface d'un objet représente un contrat abstrait qui garantit les fonctionnalités et les comportements qu'il est capable de fournir. Elle définit les messages et les interactions qui sont accessibles et disponibles pour interagir avec l'objet. L'interface spécifie les opérations autorisées, un peu comme les fichiers `.h` en `C` qui définissent une signature. Une interface constitue un type abstrait, défini par la manière dont on peut l'utiliser. Une bonne encapsulation est caractérisée par le fait que l'implémentation n'est pas visible à travers l'interface. Une mauvaise encapsulation survient lorsque la manière dont une tâche est réalisée est visible dans l'interface, ce qui conduit à une dépendance indésirable entre l'implémentation et l'interface. L'implémentation est la réalisation effective du code qui respecte l'interface, c'est-à-dire le contrat spécifié. Différentes implémentations peuvent exister pour la même interface. La capacité de remplacer une implémentation par une autre, tout en maintenant la même interface, favorise la modularité et permet des évolutions indépendantes grâce, par exemple, à l'utilisation de l'annotation @override pour substituer une méthode existante.

## Classes et instances

Une classe représente un type concret avec une implémentation, similaire à une structure en langage `C`. C'est un ensemble d'objets qui partagent des caractéristiques communes. Une classe peut servir de modèle pour créer des instances ou des objets, où de nouvelles valeurs sont dérivées ou créées. Une instance est une valeur définie par une classe, représentée par un objet. Par exemple, dans le cas d'un entier, l'instance 43 est une valeur spécifique de la classe int. En d'autres termes, une instance est une réalisation concrète du type défini par une classe.

## Attributs et Méthodes
Les valeurs stockées au sein d'une instance sont généralement représentées par des variables d'objet, qui sont des données spécifiques à cette instance. Ces variables d'objet contiennent des informations locales à l'instance, lui permettant de stocker et de manipuler des données propres à son état. En utilisant le langage de modélisation UML, il est possible de spécifier des contraintes, telles que des attributs en lecture seule (read-only), qui indiquent que certaines variables d'objet ne peuvent pas être modifiées après leur initialisation. Cela permet de garantir l'intégrité des données et de prévenir les modifications non autorisées. Enfin, le masquage d'attribut fait référence à la capacité de définir des attributs avec le même nom dans une classe dérivée, masquant ainsi l'attribut hérité de la classe de base. Cela permet de spécialiser et de personnaliser le comportement des attributs dans la classe dérivée, offrant une flexibilité supplémentaire dans la modélisation des objets.

## Les Méthodes
Les méthodes, également appelées opérations, sont des fonctions qui travaillent sur un objet spécifique, effectuant des traitements et manipulant son état interne. Elles sont invoquées en envoyant un message à une instance, c'est-à-dire en appelant la méthode sur la référence de l'objet. Dans le contexte des méthodes, le paramètre explicite est généralement appelé "self" tandis que le paramètre implicite est souvent désigné par le mot-clé "this" et fait référence à l'instance de l'objet sur laquelle la méthode est appelée. Les noms des méthodes sont généralement écrits en camelCase.

La visibilité des méthodes permet de contrôler leur accessibilité. L'utilisation de la visibilité "private" permet de créer des méthodes qui ne peuvent être utilisées que par l'objet lui-même, les rendant utiles pour la mise en œuvre interne et les opérations auxiliaires. Les méthodes "query" sont des méthodes qui ne modifient pas l'état de l'objet, elles retournent simplement une valeur, permettant ainsi d'accéder aux attributs de l'objet ou de calculer des informations à partir de celui-ci.

La séparation entre les commandes (méthodes avec effet de bord) et les requêtes (méthodes sans effet de bord) est un principe important. Une opération qui agit comme une requête doit être une expression sans effet de bord, renvoyant une valeur sans modifier l'état global ou de l'objet. Une opération de commande modifie l'état global ou de l'objet, mais elle ne retourne pas de valeur (void). Il est préférable de séparer clairement ces deux types d'opérations, afin de faciliter la compréhension et la maintenance du code. Cette distinction est similaire à celle entre les fonctions (expressions) et les procédures (commandes). L'utilisation de paramètres de sortie est recommandée pour les opérations de commande, afin de signaler explicitement les effets de bord. Les méthodes de requête impliquent généralement un passage par valeur (copie) des arguments, tandis que les méthodes de commande peuvent impliquer un passage par référence (modification de la valeur) dans certains langages, bien que cela ne soit pas le cas en Java où tout est passé par référence. La transparence référentielle, qui permet de remplacer un appel à une fonction par son résultat, est garantie uniquement lorsque les méthodes sont des requêtes sans effets de bord.

Ces principes de conception aident à écrire un code plus clair, modulaire et prévisible, favorisant une bonne encapsulation et un découplage des opérations sur les objets.

## Constructeur, Destructeur et Accesseur
Pour créer une instance d'un objet, on utilise le constructeur. Un constructeur par défaut est un constructeur sans paramètres qui initialise les attributs avec des valeurs par défaut, tandis qu'un constructeur paramétré accepte des arguments pour initialiser les attributs de l'objet. L'instanciation comprend deux étapes : l'allocation d'espace mémoire pour l'objet et l'initialisation de ses attributs via le constructeur approprié. Le mot-clé "this" fait référence à l'instance elle-même et peut être utilisé en tant que paramètre implicite dans les constructeurs pour appeler d'autres constructeurs de la même classe, permettant ainsi la délégation d'initialisation. La surcharge des constructeurs permet de créer plusieurs versions de constructeurs avec des nombres différents de paramètres.

En ce qui concerne les destructeurs, ils ne sont pas utiles en Java car la gestion de la mémoire est gérée par le garbage collector. Le garbage collector se charge de libérer automatiquement la mémoire des objets qui ne sont plus référencés. Cependant, la méthode "finalize" peut être définie dans une classe pour effectuer des actions spécifiques avant que l'objet soit libéré de la mémoire.

Les accesseurs sont des méthodes qui permettent d'accéder aux attributs privés d'un objet. Ils fournissent un moyen de lecture et, éventuellement, de modification des attributs tout en préservant l'encapsulation. Les accesseurs peuvent effectuer des vérifications et des validations des paramètres avant de modifier l'état de l'objet, garantissant ainsi l'intégrité des données. Les accesseurs divisent l'implémentation de l'objet de son interface, en cachant la façon dont les valeurs sont stockées et fournissant uniquement des propriétés de l'objet. Il existe différentes conventions pour les noms des accesseurs, tels que l'utilisation de la convention `beans` ou la convention `builder`. Les setteurs peuvent également retourner l'objet lui-même (this) pour permettre le chaînage des appels de méthodes, ce qui n'affecte pas l'encapsulation car l'objet est responsable de son état.

En résumé, la création d'une instance d'objet implique l'appel du constructeur approprié, la gestion des destructeurs n'est pas nécessaire en Java grâce au garbage collector, et les accesseurs fournissent des méthodes pour accéder et modifier les attributs privés d'un objet tout en préservant l'encapsulation et l'intégrité des données.

example de constructeur en java avec initialisation des atributs et acesseurs
```java
public class Personne{

private String name;    //atributs privees de la classe
private int age;

public Personne(String name, int age){   //constructeur 
  this.name = name;
  this.age = age;
}

public String getName(){    //accesseur de l'atribut priveé
  return this.name;
}

public int age(){
  return this.age
}

public void setName(String name){
  this.name = name;
}
```


## Éléments Statiques

Une classe peut également contenir des attributs et des méthodes statiques qui sont propres à la classe elle-même et non à une instance spécifique de la classe. Les attributs statiques sont des attributs qui sont associés à la classe et non à une instance individuelle. Ils peuvent être accédés à partir de n'importe où dans la classe et n'ont pas besoin d'une instance de la classe pour y accéder. Les attributs statiques sont souvent utilisés pour définir des constantes communes à toutes les instances de la classe.

Les méthodes statiques sont des fonctions qui appartiennent à la classe elle-même plutôt qu'à une instance particulière. Elles n'ont pas de paramètre implicite "this" car elles ne nécessitent pas d'instance spécifique pour être appelées. Les méthodes statiques sont limitées à la classe dans laquelle elles sont définies et ne peuvent pas être invoquées sur des instances de la classe. Elles sont souvent utilisées pour des opérations qui ne dépendent pas de l'état d'une instance spécifique, comme des fonctions mathématiques. Les méthodes de classe peuvent également prendre en paramètre une classe elle-même, ce qui peut être utilisé pour des opérations telles que la création d'une nouvelle instance de la classe.

## Extension

### Propriétés
- Propriétés recherchées par la modularité et que l'encapsulation nous apporte
    - Remplaçabilité : séparation de l'implémentation et de l'interface d'un objet, permettant de remplacer un objet par un autre tant que l'interface reste la même.
    - Réutilisabilité : regroupement des données et méthodes dans un objet, facilitant sa réutilisation dans différents contextes.
    - Extensibilité : possibilité d'ajouter de nouvelles fonctionnalités à un objet existant sans le modifier, grâce à l'encapsulation.

Le principe d'ouverture/fermeture (Open/Closed Principle) stipule que les objets doivent être fermés à la modification mais ouverts à l'extension. Cela signifie qu'un objet ne devrait pas être modifié une fois créé, afin de ne pas perturber le système existant, mais il devrait permettre l'ajout de nouveaux comportements sans modification du code source. Cette ouverture à l'extension est souvent réalisée grâce au polymorphisme.

### Polymorphisme
- Qu'est-ce que le polymorphisme ?
    - Il s'agit de l'utilisation (méthodes/fonctions) indépendante du type réel des éléments manipulés (des arguments des méthodes ou des classes).
    - Les valeurs peuvent avoir concrètement plusieurs types ou les fonctions peuvent travailler sur plusieurs types, ce qui permet une adaptation à plusieurs types. C'est une notion importante pour la réutilisabilité, la remplaçabilité et l'extension.
    - Il existe deux formes principales de polymorphisme :
        - Polymorphisme ad hoc :
            - Transtypage : Conversion implicite du type d'une valeur, permettant de changer le type d'une valeur par un autre (cast).
            - Surcharge : Plusieurs fonctions ou routines ayant le même nom mais des paramètres différents, en fonction du type de la variable prise en compte ou du nombre de paramètres. Cela se base sur la signature de la fonction.
        - Polymorphisme universel :
            - Générique/paramétré : Une seule implémentation qui gère plusieurs types à la fois, soit n'importe quel type ou un type et ses sous-types.
            - Inclusion (passage par sous-typage) : Traitement générique indépendant du type de la variable, permettant de manipuler n'importe quel type concret. Il est utilisé pour créer des structures complexes (comme un conteneur) dont le comportement est indépendant de l'objet qu'ils contiennent. Par exemple, une liste chaînée avec des opérations qui travaillent sur les listes chaînées indépendamment du type de la liste.
    - pour le polymorphisme à la demande (polymorphisme ad hoc) :
        - Chaque type a une implémentation spécifique pour la fonction correspondante. Ainsi, le système choisit l'implémentation la plus appropriée en fonction du type réel des éléments manipulés.
    - pour le polymorphisme universel :
        - polymorphisme generique  
          - Une seule implémentation qui gère plusieurs types à la fois, soit n'importe quel type ou un type et ses sous-types.
        - Inclusion :
          - Il s'agit de la notion de sous-type et d'héritage/redéfinition.
          - Les sous-types sont des sous-ensembles des ensembles de types, acceptant les familles de types et créant une hiérarchie de types.

### Héritage

L'héritage est l'un des concepts fondamentaux de la programmation orientée objet. Il permet la création de nouvelles classes (sous-classes) basées sur des classes existantes (superclasses), en héritant de leurs attributs et de leurs méthodes. L'héritage permet de définir une hiérarchie de classes, où les sous-classes héritent du comportement et des caractéristiques des superclasses, tout en ayant la possibilité de modifier ou d'étendre ce comportement. Cela favorise la réutilisation du code et facilite la gestion des classes en les regroupant selon leurs similarités et leurs différences. L'héritage permet également de mettre en œuvre des relations "est-un", où une sous-classe est considérée comme une spécialisation ou une extension de sa superclasse. Grâce à l'héritage, il est possible de concevoir des architectures logicielles plus flexibles, évolutives et modulaires, tout en favorisant la lisibilité et la maintenabilité du code.

### Redéfinition et Surcharge

La redéfinition et la surcharge sont deux mécanismes importants en POO, mais elles diffèrent dans leur fonctionnement.

La redéfinition, permet de fournir une implémentation différente d'une méthode d'une superclasse pour chaque type spécifique de la sous-classe. Lorsque nous appelons une méthode sur une instance, la méthode appropriée est choisie en fonction du type réel de l'objet (this) qui reçoit le message. Ainsi, la résolution de la méthode est effectuée dynamiquement lors de l'exécution en fonction de la classe concrète de l'instance. Cela permet d'obtenir un comportement spécifique à chaque sous-classe, offrant une flexibilité et une adaptation aux différents types.

La surcharge, quant à elle, consiste à fournir plusieurs implémentations d'une même méthode au sein d'une classe, mais avec des paramètres différents. Cela permet d'avoir plusieurs versions d'une méthode qui acceptent différents types ou nombres de paramètres. Par exemple, une classe peut avoir plusieurs constructeurs qui prennent différents ensembles de paramètres. La surcharge est résolue statiquement au moment de la compilation, où le compilateur détermine quelle méthode doit être appelée en fonction du type déclaré des paramètres passés. Ainsi, la méthode à appeler est décidée avant l'exécution, en fonction des types statiques des arguments.

### Classes Abstraites et Interfaces

Les classes abstraites et les interfaces sont des concepts clés en POO pour la création de modèles et de structures flexibles. Une classe abstraite est une classe qui ne peut pas être instanciée directement, mais sert de modèle pour d'autres classes dérivées. Elle peut contenir des méthodes abstraites, qui ne sont pas implémentées dans la classe abstraite elle-même, mais doivent être implémentées par ses sous-classes. Les classes abstraites permettent de définir des comportements communs et de fournir une base pour les classes spécialisées qui en héritent.

D'autre part, les interfaces sont des contrats de comportement. Elles définissent un ensemble de méthodes (sans implémentation) qu'une classe doit implémenter pour adhérer à cette interface. Une classe peut implémenter plusieurs interfaces, ce qui lui permet d'offrir différentes fonctionnalités à travers ces interfaces. Les interfaces permettent la réalisation de multiples héritages et favorisent la modularité et la réutilisabilité du code.

### La Délégation

la délégation en POO permet de créer des relations flexibles et modulaires entre les objets en déléguant certaines responsabilités à des objets spécialisés. Cela favorise la réutilisabilité du code, la séparation des préoccupations et la flexibilité dans l'évolution du comportement des objets.

### Le Sous-typage

Le sous-typage est un concept clé en POO qui permet de définir des relations hiérarchiques entre les classes. Il repose sur le principe selon lequel une classe dérivée ou sous-classe peut être considérée comme un type plus spécifique de sa classe parente ou superclasse. En d'autres termes, une instance de la sous-classe peut être utilisée partout où une instance de la superclasse est attendue.

Le sous-typage offre de nombreux avantages en termes de modularité et de réutilisabilité du code. Il permet de créer des hiérarchies de classes qui partagent des caractéristiques communes, tout en étendant ou en spécialisant le comportement de la classe parente. Cela permet d'écrire du code générique qui peut être utilisé avec des instances de différentes sous-classes, offrant ainsi une grande flexibilité et une conception plus modulaire.

Le sous-typage facilite également le polymorphisme, qui est la capacité d'un objet à prendre différentes formes et à répondre de manière adaptée aux messages qu'il reçoit. Grâce au sous-typage, les instances de sous-classes peuvent être traitées de manière uniforme lorsqu'elles sont manipulées via des références de la superclasse, ce qui permet d'écrire du code plus générique et plus flexible.

## Projets

//todo
