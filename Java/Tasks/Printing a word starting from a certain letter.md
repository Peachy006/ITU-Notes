
The way i first wanted to do this was by making a for loop running length() times of the word, if the charAt(i) was a which is the letter we are searhing for then i would break the for loop, then after the for loop was broken i would make another loop where i would just do word = word + letters coming after a, i would do this by declaring the for loop with an integer c + i which we used in the loop before allowing me to start from that point in the word.

# BUT WAIT

There is 2 much easier ways to do this, the first way is using a boolean, you do this by using this code here:

```JAVA
import java.util.Scanner;

public class finginga {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String s = sc.next();
        String word = "";

        boolean found = false;
        for (int i = 0; i < s.length(); i++) {
            if (s.charAt(i) == 'a') {
                found = true; // start appending once we hit 'a'
            }
            if (found) {
                word = word + s.charAt(i);
            }
        }

        if (!found) {
            System.out.println("No 'a' found in the word.");
        } else {
            System.out.println(word);
        }
    }
}

```

What this code does is using a boolean value it checks if the word has been letter has been found. This is done with a for loop combined with an if statement allowing me to set the boolean value to true if the letter is found

# Honorable mentions for the clever

```JAVA
import java.util.Scanner;

public class finginga {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String s = sc.next();

        int index = s.indexOf('a'); // find first 'a'
        if (index != -1) {
            System.out.println(s.substring(index));
        } else {
            System.out.println("No 'a' found in the word.");
        }
    }
}

```

https://www.w3schools.com/java/ref_string_substring.asp

https://www.w3schools.com/java/ref_string_indexof.asp

[[IndexOf]]

