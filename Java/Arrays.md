For at lave en array skal man bruge følgende syntaks:


```cs: JAVA
int[] a = new int[10]
```

Her laver vi en array med integers som vi kalder a, vi deklarerer den som en ny array med integers med en størrelse på 10.

Dette kan derfor også erstattes med andre datatyper som strings


```cs: JAVA
String[] b = new String[8];
```

Husk her at arrays starter med 0

For at udfylde en array med individuel data kan man gøre som følgende:

```cs: JAVA
intArray[0] = 21;
```

For at eksempelvis lave en ny array med preeksisterende data kan man gøre følgende:

```cs: JAVA
int[] intArray = new int[] {21, 15, 27, 15, 24}
```

Hvis du vil bruge scanner til at udfylde din array med date givent i eksempelvis konsollen kan man gøre følgende med et for loop:

```cs: JAVA
 
 int n = sc.nextInt();
 int[] arr = new int[n];
 
 for(int i = 0; i < n; i++) {
	 arr[i] = sc.nextInt()
 }
```


# Hvordan fjerner man et element fra en array

Måden man gør det på er ved at oprette et nyt array som er array.length -1 længde og man laver derefter et for loop som tilføjer alle elementerne sålænge de ikke er det element man ønsker at fjerne

```JAVA
package com.journaldev.java;
import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
        int[] arr = new int[]{1,2,3,4,5}; // lav den første array
        int[] arr_new = new int[arr.length-1]; // lav den anden array
        int j=3; // tallet vi skal fjerne
        for(int i=0, k=0;i<arr.length;i++){ // for loop der kører array.length gange
            if(arr[i]!=j){ // tjekker om j (den vi vil fjerne) eksisterer
                arr_new[k]=arr[i]; // vi bruger også k fordi den skal vøre forskudt
                k++; //increment k
            }
        }
        System.out.println("Before deletion :" + Arrays.toString(arr));
        System.out.println("After deletion :" + Arrays.toString(arr_new));

    }
}
```

Her skal du være opmærksom på at hvis j ikke findes i dit array, altså at det ikke skal fjernes, så opretter du stadigvæk en ny array med n-1 længde hvilket er et problem

