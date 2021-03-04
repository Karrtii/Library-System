# Library-System
A client-server library system where users can search for library items available in the database to reserve. The main purpose of this project to is to learn how a client-server system can be set up with a database, and to produce clean code using design patterns and SOLID design principles.

**About the library system**

Users will be prompted with a login request when the program is launhed. If the user has not already registered, they will be given an option to register.

![image](https://user-images.githubusercontent.com/71009398/109950950-68097900-7cdd-11eb-8e8e-ed33f43ded34.png)

Once the user is logged in, they desired item can be searched and found if it exists, and then can be borrowed for a fixed time period.

![image](https://user-images.githubusercontent.com/71009398/109951106-91c2a000-7cdd-11eb-9419-ac5f1cb7f4d4.png)

If a chosen item has already been reserved or borrowed by another user, a prompt will be displayed stating that it has been reserved/borrowed by another person.

![image](https://user-images.githubusercontent.com/71009398/109951230-b9b20380-7cdd-11eb-9772-b8b50eb20b38.png)

The items then must be returned by users before the time period is up. If they failed to return it, a fine will be issued to their account.

**Design of the library system**

The library system is built using the layered architecture, namely with two layers, Client and Server.

![image](https://user-images.githubusercontent.com/71009398/109951976-9fc4f080-7cde-11eb-94be-bc5a9660c52a.png)

In the Client layer, MVVM design pattern is used so that it provides division of responsibilities. 
