Basic HelloWorld kan skrives på 2 måder, der er codecademy som siger

`public class Compiling {`
`public static void main(String[] args) {`
`System.out.println("Java is a class-based language.");`
`}`
`}`

Til forlæsning bliver der sagt:

`public class HelloWorld {`
     `static void Hello() {`
        `System.out.println("Hello World!");`
    `}`
`}`

Når vi siger String[] args siger vi at den kan tage imod argumenter fra kommandolinjen ind i mit program.



# Konstanter

Der er konstanter som ikke behøves skrives i "" men istedet bare kan skrive, eksempelvis:

System.out.println(42)

De kan derfor håndteres på andre måder


Husk at kommatal er . istedet for ,


# Scanner
læs evt mere [[Scanner]]
Først skal man importere scanneren:

import java.util.scanner;

Gør så:

Scanner myScannerObj  = new Scanner(System.in);

Hent så whatever:

String userName = myScannerObj.nextLine();

Herefter kan den printes som en variabel.

Når man skriver nextLine(); lytter den efter en linje som du skriver, hvis du eksempelvis skriver nextInt() så lytter den kun efter et heltal

Forskellige Datatyper findes i [[Datatyper]]

Man kan derfor også hente som nextBoolean()

# Variabler

Når du deklarerer en variable skal det gøres sådan:

String name = "Sean";

int tal = 42;

hvis variablen bliver lavet ude fra en static void eksempel()

så skal den deklareres som static:

static String name = "Sean";





For at ændre vores variabel, eksempelvis gøre den 1 højere:

age++;
age = age +1;


# Operatorer:


x * x

9 - x

1 + 1

x / 2




int x = 17;

System.out.println(x/2.0)     ------     8.5


double x = 17;

System.out.println(x / 2);    --------   8.5


# Øvelse james bond:

public class ovelse2 {
    
    static String firstName = "Sean";
    static String lastName = "P";
    
    static void main() {
        System.out.println("My name is " + lastName + ", " + firstName + " " + lastName);
    }
}