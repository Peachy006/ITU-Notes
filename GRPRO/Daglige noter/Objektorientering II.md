- [[#MyArrayList()|MyArrayList()]]
- [[#Billede beskrivelse|Billede beskrivelse]]
	- [[#Billede beskrivelse#Instansiering|Instansiering]]
	- [[#Billede beskrivelse#Initialisering|Initialisering]]
- [[#Slut|Slut]]
- [[#Hvad er en konstruktør?|Hvad er en konstruktør?]]
	- [[#Hvad er en konstruktør?#2 formål:|2 formål:]]
			- [[#Skabe objekter|Skabe objekter]]
			- [[#Initialisere objekter|Initialisere objekter]]
	- [[#Hvad er en konstruktør?#Eksempelvis:|Eksempelvis:]]
		- [[#Eksempelvis:#Her er konstruktøren account() {|Her er konstruktøren account() {]]
- [[#This.name betyder at den peger på this, altså det som er inde i classen|This.name betyder at den peger på this, altså det som er inde i classen]]
		- [[#Eksempelvis:#Læg mærke til at i det her billeder der bruger han student.display til at display en student inde i sit for each loop, her tager display funktionen automatisk imod værdien gennem Student(String name, int age) og bruger den værdi som han giver der til at printe navn og alderen|Læg mærke til at i det her billeder der bruger han student.display til at display en student inde i sit for each loop, her tager display funktionen automatisk imod værdien gennem Student(String name, int age) og bruger den værdi som han giver der til at printe navn og alderen]]
		- [[#Eksempelvis:#Læg mærke til her at han ikke må printe balancen fordi at den fil ikke må se den viden, istedet for må du kalde funktionen account.status som så printer balancen|Læg mærke til her at han ikke må printe balancen fordi at den fil ikke må se den viden, istedet for må du kalde funktionen account.status som så printer balancen]]

# Recap fra sidst

## MyArrayList()

![[Pasted image 20250918141854.png]]

## Billede beskrivelse
### Instansiering
Når man har sin klasse kan man instansiere :: new Car()
dvs man laver en ny instans med sin bil

### Initialisering
Car car = new Car()    - her er "=" initialiseringen

## Slut

![[Pasted image 20250918142528.png]]

Nøgle pointen med den her slide er at man skal fokusere på funktioner, altså for eksempel person.birthday(); så slipper man for at gøre tingene i andre filer ved eksempelvis at sige age++;

## Hvad er en konstruktør?

### 2 formål:
##### Skabe objekter
##### Initialisere objekter
### Eksempelvis:
![[Pasted image 20250918142756.png]]

#### Her er konstruktøren account() {
balance = 0.0;
}


## This.name betyder at den peger på this, altså det som er inde i classen
Så når du siger, this.name = name; så siger man at den name som allerede er deklareret skal være den værdi som man tager imod i funktionen, som ses her:

![[Pasted image 20250918143339.png]]



![[Pasted image 20250918143541.png]]

#### Læg mærke til at i det her billeder der bruger han student.display til at display en student inde i sit for each loop, her tager display funktionen automatisk imod værdien gennem Student(String name, int age) og bruger den værdi som han giver der til at printe navn og alderen


![[Pasted image 20250918144026.png]]

#### Læg mærke til her at han ikke må printe balancen fordi at den fil ikke må se den viden, istedet for må du kalde funktionen account.status som så printer balancen

# toString() && ineffektivitet på strenge

# Aggregering (sum, avg, min, max)

# Datastrukturer med objekter

# def, Use, Use -> Def