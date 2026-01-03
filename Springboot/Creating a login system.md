sFirst create a file called User, this will use jakarta to create it

start with making the @entity

inside the class you write 
@Id  
@GeneratedValue(strategy = GenerationType.IDENTITY)
the generated value is making sure the id is incremented and is also the primary key

now follow it by your fields:
private Long id;  
private String username;  
private String password;

create a constructor:

public User(String username, String password) {  
    this.username = username;  
    this.password = password;  
}  
  
public User() {  
  
}

and then make some getters and setters


### now we make the repository

in our example i will call it UserRepository, it will be in a package called repository. this will be an interface

it will extend JpaRepository<>
the <> will take 2 things, the name of your thing (user) and the type of your primary key, so in our example:
public interface UserRepository extends JpaRepository<User, Long> {



i use XAMPP with mysql to save data, i use postman to simulate data transactions and yea thats it

### application.properties

### how does it work together?

the jparepo talks with the database, the methods are used by userServiceImplementation, and then userServiceIMplementation is used in userController