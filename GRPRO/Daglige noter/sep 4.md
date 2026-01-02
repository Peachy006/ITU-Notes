Data betyder repræsentation af information

Java er sekventielt, det betyder at det læses linje for linje
ASCII = American std code for info interchange

![[Pasted image 20250904153353.png]]

System.out.prtinln((int) 'A') = 65
(char)


# Kollektioner
## Datastrukturer


# ArrayLists

Tillader os at opbevare et vilkårligt antal af 1 slags værdi

Vi kan tilføje og fjerne værdier

import java.util.ArrayList;

```Java

ArrayList<String> list = new Arraylist<>();
```

man kan nu sige:

list.add("En");
list.remove(1); -- fjerne værdien ved index 2, så værdi nummer 2 fordi den starter fra 0


Vi kan også læse/hente elementer:

String a = list.get(1);


