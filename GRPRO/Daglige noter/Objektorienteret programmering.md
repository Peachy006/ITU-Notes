

Vi tager et kig på prøver om objektorienteret programmering

# Recap fra sidst:


1. [[ArrayLists]] - list = new ArrayList<"Integer">();


Linkedlists er lineære ved insertion altså O(n) og de er kvadratiske ved accessing, altså O(n²)

Arraylists er omvendt, altså kvadratisk insertion og lineær accessing



![[Pasted image 20250916125732.png]]


Hvis man koder det her:

class Car {
    int speed;
    
    Car() {
        speed = 0;
    }
    
    void accellerate() {
        speed = speed + 5;
    }
}


Kald på den i en anden fil


Car car;

car = new Car();

System.out.println(car.speed);


static betyder at det kører uden et objekt

en metode der ikke indeholder static kører altid på et objekt

