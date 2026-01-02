
In java you can declare functions and call them later on, the order in which you write the functions in the document is irrelevant. When using your main function it is declared as 

public static void main(String[] args) {

}


you can declare other functions as:

public static void name(int i ) {

}

here it has the argument int i which you can use when calling the function in the main function

# Return

When using the return it allows you to keep the values and save them as data which can be manipulated later on, do this for example by saing:

```JAVA
public static name(int x) {
return x * x;
}
```