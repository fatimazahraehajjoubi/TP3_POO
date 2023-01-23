# TP3_POO
## Etape 5
### La dépendance web : 
Dans un projet Spring Boot cette dépendance permet d'utiliser les composants de Spring MVC pour créer une application web. Elle inclut des classes pour gérer les demandes HTTP, les routes, les contrôleurs, les vues et les modèles, comme elle permet d'utiliser l'injection de dépendances et la gestion de la sécurité,
pour créer une application web complète et fonctionnelle.

### La dépendance JPA (Java Persistence API):
La dépendance JPA de Spring Boot permet d'utiliser les fonctionnalités de Spring Data JPA pour faciliter l'accès aux données en utilisant des concepts tels que les repositories et les Entity Managers, ainsi que de configurer automatiquement un EntityManagerFactory et un Transaction Manager pour l'application. Il permet également d'utiliser un ORM ( Object-Relational Mapping) tel que Hibernate pour gérer les relations entre les objets Java et les tables de la base de données.

### La dépendance Hibernate
La dépendance Hibernate dans un projet Spring Boot permet d'utiliser les fonctionnalités de persistance de données dans une application Java, les fonctionnalités de Spring Data JPA pour faciliter l'accès aux données. elle permet également d'utiliser un ORM ( Object-Relational Mapping) tel que Hibernate pour gérer les relations entre les objets Java et les tables de la base de données.

### La dépendance H2
La dépendance H2 dans un projet Spring Boot permet d'utiliser la base de données H2 en mémoire pour des tests ou des développements de prototypes. H2 est une base de données relationnelle écrite en Java qui peut être embarquée dans une application Java, il est léger, rapide et peut être utilisé pour des tests unitaires ou des applications de développement.

### La dépendance Spring Boot DevTools
Spring Boot DevTools est un ensemble d'outils qui rend le développement plus facile et plus efficace en automatisant certaines tâches et en fournissant des informations de débogage utiles.

### La dépendance Thymeleaf
La dépendance Thymeleaf dans un projet Spring Boot permet d'utiliser le moteur de template Thymeleaf pour générer des pages HTML dynamiques dans une application web. 
elle permet de générer des pages HTML valides et respectant les normes d'accessibilité.

## Etape 13
### Avec quelle partie du code avons-nous paramétré l'url d'appel /greeting ?
L'URL d'appel /greeting est paramétrée avec l'annotation @GetMapping("/greeting"). Cette annotation permet de mapper les requêtes HTTP GET à une méthode spécifique dans le contrôleur.
### Avec quelle partie du code avons-nous choisi le fichier HTML à afficher ?
Le fichier HTML à afficher est choisi avec la méthode "return "greeting";" de la fonction greeting(). Cette méthode retourne une chaîne de caractères qui correspond au nom de la vue.
### Comment envoyons-nous le nom à qui nous disons bonjour avec le second lien ?
Le nom à qui nous disons bonjour avec le second lien est envoyé en utilisant l'annotation @RequestParam et la méthode addAttribute() de l'objet Model. L'annotation @RequestParam permet de récupérer les paramètres de la requête HTTP, ici "nameGET", qui est utilisé pour définir le nom par défaut "World" si il n'est pas fourni. Le nom est ensuite ajouté à l'objet Model avec la méthode addAttribute() pour être utilisé dans la vue. 

## Etape 17
En Relanceant l'application on remarque l'apparition de la nouvelle table Adresse dans notre database.

## Etape 18
### explication : 
Comme on a ajouté la dépendance Hibernate en tant que gestionnaire de persistance, Hibernate va automatiquement créer les tables de la base de données en fonction des entités déclarées dans l'application. Cela est possible grâce à la propriété "hibernate.hbm2ddl.auto" qui peut être configurée pour différentes valeurs telles que "create", "create-drop", "update" etc. Si cette propriété est définie sur "create" ou "create-drop", Hibernate va automatiquement créer les tables de la base de données en fonction des entités déclarées. Dans ce cas, on peut voir l'apparition de la nouvelle table qui est générée automatiquement à partir de l'entité déclarée.

## Etape 20
Oui on peut voir le contenu de la database.

## Etape 22
### l'annotation @Autowired :
C'est une annotation de Spring qui permet d'injecter automatiquement une dépendance dans un bean géré par Spring. Dans le code précédent, elle est utilisée pour injecter l'instance d'AddressRepository dans le champ addressRepository de la classe AddressController.

## Etape 30
j'ai utilisé une méthode basée sur les liens externes. j'ai ajouté une référence CSS à Bootstrap dans la balise head de chaque vue HTML, en utilisant l'attribut href pour pointer vers un lien externe (CDN) pour les fichiers Bootstrap CSS. De même, j'ai ajouté une référence JS à Bootstrap dans le bas de la page, en utilisant un lien externe (CDN) pour les fichiers Bootstrap JS. Cette méthode est pratique car elle permet de charger les fichiers Bootstrap à partir d'un serveur distant, plutôt que de les héberger sur notre serveur.
