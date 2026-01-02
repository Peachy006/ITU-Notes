

```Java

static void record() { // husk: import java.util.regex.*;
	String input = "brabrand@itu.dk";
	Pattern pattern = Pattern.compile("([a-z]+)@([a-z]+)[.]([a-z]+)");
	Matcher matcher = pattern.matcher(input);
	if ( matcher.find() ) {
		System.out.println("Entire match: '" + matcher.group(0) + "'");
		System.out.println("- Userid: '" + matcher.group(1) + "'");
		System.out.println("- Domain: '" + matcher.group(2) + "'");
		System.out.println("- Country: '" + matcher.group(3) + "'");
	} else {
		System.out.println("NO MATCH");
	}
}

```
![[Pasted image 20251106175114.png]]![[Pasted image 20251106175118.png]]