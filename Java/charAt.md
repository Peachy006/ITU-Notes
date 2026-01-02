hvis man skal iterere mellem alle bogstaver i et ord, kan man lave et for loop med det. Lad os sige man skal sortere efter store bogstaver og printe dem kan man starte med at lave det her for loop:

`for(int i = 0; i < word.length(); i++)`

her er word.length længden af vores variabel word som nok indeholder en string eller whatever.  Man kan derefter lave en if statement inde i loopet til at tjekke det bogstav man er nået til:

`if(Character.isUpperCase(word.charAt(i))) {`
`System.out.println(word.charAt(i))`
`}`

man kan derfor bruge i som kører 1 højere hver gang og itererer igennem og derefter tjekke hver bogstav med charAt

```cs: JAVA

```

