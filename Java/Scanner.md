
Først skal man importere scanneren:

import java.util.scanner;

Gør så:

Scanner myScannerObj  = new Scanner(System.in);

Hent så den information du skal hente:

String userName = myScannerObj.nextLine();

Herefter kan den printes som en variabel.

Når man skriver nextLine(); lytter den efter en linje som du skriver, hvis du eksempelvis skriver nextInt() så lytter den kun efter et heltal

Forskellige Datatyper findes i [[Datatyper]]

Man kan derfor også hente som nextBoolean()


## If next int

Hvis du skal tjekke om der er flere tal tilbage så gør det her:


```JAVA
if (sc.hasNextInt()) {
    int x = sc.nextInt();
} else {
    // no more integers available
}

```