# Library-System
A client-server library system where users can search for library items available in the database to reserve. The main purpose of this project to is to learn how a client-server system can be set up with a database, and to produce clean code using design patterns and _SOLID_ design principles.

**About the library system**

Users will be prompted with a login request when the program is launhed. If the user has not already registered, they will be given an option to register.

![image](https://user-images.githubusercontent.com/71009398/109950950-68097900-7cdd-11eb-8e8e-ed33f43ded34.png)

Once the user is logged in, they desired item can be searched and found if it exists, and then can be borrowed for a fixed time period.

![image](https://user-images.githubusercontent.com/71009398/109951106-91c2a000-7cdd-11eb-9419-ac5f1cb7f4d4.png)

If a chosen item has already been reserved or borrowed by another user, a prompt will be displayed stating that it has been reserved/borrowed by another person.

![image](https://user-images.githubusercontent.com/71009398/109951230-b9b20380-7cdd-11eb-9772-b8b50eb20b38.png)

The items then must be returned by users before the time period is up. If they failed to return it, a fine will be issued to their account.

**Design of the library system**

The library system is built using the layered architecture, namely with two layers, Client and Server. Both Client and Server layers are implemented in _Java_, and _JavaFX_ and _Scenebuilder_ was used for the GUI.

![image](https://user-images.githubusercontent.com/71009398/109951976-9fc4f080-7cde-11eb-94be-bc5a9660c52a.png)

An important aspect of this project is to learn and properly apply _SOLID_ design principles, _CRUD_ operations and _DRY_ rule. For the most part, this was doable, expect for the _DRY_ rule, where is is broken in one class in the Server layer.

In the Client layer, _MVVM_ design pattern is used so that it provides division of responsibilities. _Observer_ and _Singleton_ patterns are also used in this layer.

The Client and Server layers communicate with each other using _RMI_.

In the Server layer, the _RMI_ server and the _Data Access Objects_ (DAO) can be found. _Singleton_ pattern is used here so that the DAOs can get an instance of the database without instantiating it each time it is called. An _Adpater_ pattern is also used so that the methods from the DAOs can be called.

The database was made in _PostgreSQL_, and _JDBC_ was used to connect the Server layer to the database.

**Testing of the system**

The two main types of tests made for the system were unit tests and usability tests.

Usability testing is concerned with the intuitiveness of the system, testing on users who had no prior experience with the system. 

Unit testing’s purpose is to test the logical functionality of the system. The reason why this testing was included was to ensure the functionality in case of future system’s improvements, enhancements and/or upgrades. 
