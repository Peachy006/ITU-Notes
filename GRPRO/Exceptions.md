Unchecked exceptions  skal extende RunTimeException
Checked Exceptions skal extende Exception

Når en exception bliver kastet viderede hedder det propagering, når den bliver try catchet hedder det håndtering

Make ur own:

```JAVA
class MyUncheckedException extends RUntimeException { // den er nu unchecked pga runtime //

	private int number;
	
	MyUncheckedException(int number) {
		super("Something bad happened");
			//det er en bedre ide at have en string message som du så kalder super med
		this.number = number;
		
	}
	
	int getNumber() {
	return number;
	}

}

```

Du kan nu bruge den:

```JAVA
void m1() {
	try {
		m2();
	} catch(MyUncheckedException e) {
		SOP(e.getMessage());
		SOP(e.getNumber());
	}
}




```

Husk hvis den er checked så skal du throwe den, hvis den er unchecked skal den ikke throwes

