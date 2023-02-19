## Annotation @SpringBootTest | @WebMvcTest | Spring Boot

Dans ce repo, nous allons voir les différences entre l'annotation `@SpringBootTest` et `@WebMvcTest` de Spring Boot.

`@SpringBootTest` - nous permet d'effectuer des tests d'intégration dans les applications Spring Boot. Spring Boot fournit l'annotation `@SpringBootTest` pour les tests d'intégration.
Fondamentalement, l'annotation @SpringBootTest indique à Spring Boot de rechercher la classe de configuration principale (une avec @SpringBootApplication, par exemple) et de l'utiliser pour démarrer un contexte d'application Spring.

**@SpringBootTest vs @WebMvcTest**
	
Spring Boot fournit l'annotation `@SpringBootTest` pour les tests d'intégration. Cette annotation crée un contexte d'application et charge le contexte d'application complet.

`@SpringBootTest` démarrera le contexte complet de l'application, ce qui signifie que nous pouvons  @Autowire  n'importe quel bean récupéré par l'analyse des composants dans notre test.
	
**Annotation @WebMvcTest**
SpringBoot fournit une annotation `@WebMvcTest` pour tester les contrôleurs Spring MVC. De plus, le test basé sur @WebMvcTest s'exécute plus rapidement car il ne chargera que le contrôleur spécifié et ses dépendances uniquement sans charger l'application entière. 
	
Spring Boot instancie uniquement la couche Web plutôt que l'ensemble du contexte de l'application. Dans une application avec plusieurs contrôleurs, vous pouvez même demander qu'un seul soit instancié en utilisant, par exemple, @WebMvcTest(HomeController.class).
	
**@SpringBootTest vs @WebMvcTest**

1. L'annotation `@SpringBootTest` charge le contexte complet de l'application afin que nous puissions tester divers composants. Donc, fondamentalement, l'annotation @SpringBootTest indique à Spring Boot de rechercher la classe de configuration principale (une avec @SpringBootApplication, par exemple) et de l'utiliser pour démarrer un contexte d'application Spring.

L'annotation `@WebMvcTest` charge uniquement le contrôleur spécifié et ses dépendances uniquement sans charger l'intégralité de l'application. Par exemple, supposons que vous ayez plusieurs contrôleurs Spring MVC dans votre projet de démarrage Spring - EmployeeController , UserController , LoginController , etc., nous pouvons utiliser l'annotation @WebMvcTest pour tester uniquement des contrôleurs Spring MVC spécifiques sans charger tous les contrôleurs et leurs dépendances. 
	
2. Spring Boot fournit l'annotation @SpringBootTest pour les **tests d'intégration**.
	
**Quand utiliser les annotations @SpringBootTest et @WebMvcTest ?**
- Utilisez l'annotation @SpringBootTest pour les tests d'intégration.
- Utilisez l'annotation @WebMvcTest pour les tests unitaires du contrôleur Spring MVC.
	
Ressources utiles :
- [@SpringBootTest Spring Boot Example](https://www.javaguides.net/2022/03/springboottest-spring-boot-example.html)
- [@SpringBootTest vs @WebMvcTest](https://www.javaguides.net/2022/03/springboottest-vs-webmvctest.html)