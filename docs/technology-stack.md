## Outline of Technology Stacks

### Back End:

* Ubuntu Linux OS
* Apache HTTP server configured as reverse proxy
* JRE 7
* Apache Tomcat Java application server
* Web service application, incorporating
    * Data model
        * Embedded Apache Derby database
        * Hibernate ORM
        * Custom entity classes
        * Spring Boot Data
        * Custom data repository interfaces
    * Service Controllers
        * Spring MVC
        * Custom Controllers
    * View Composition & Serialization
        * Jackson JSON
        * Custom View Classes & Interfaces
    * Authentication
        * [Spring Security](https://spring.io/projects/spring-security)
        * Google Sign In
        * [Spotify Sign In](https://developer.spotify.com/documentation/general/guides/authorization-guide/)
        
### Front End:

* Android OS
* Data model
    * SQLite
    * Room ORM
    * Custom entity and other model classes
    * Custom type converters
    * Custom type converters
    * Data access object (DAO) interfaces
* Remote service interfaces
    * Retrofit
    * ReactiveX
    * Gson
    * Custom serializer/deserializers
* View Model Components
    * Android Lifecycle framework (ViewModel & LiveData)
    * Custom View Model Classes
* View
    * Custom RecyclerView.Adapter and RecyclerView.Holder classes
    * Custom Layouts
* Controller
    * Custom activity and fragment classes
* Authentication
    * Google Sign In
    * [Spotify Sign In](https://developer.spotify.com/documentation/general/guides/authorization-guide/)
    
> [Return to previous page](index.md#outlines-of-technology-stacks)