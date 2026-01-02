
First, you need to declare the IO after 

```JAVA
    public static void main(String[] args) throws IOException {
```


Also, import it like this:

import java.io.*

```Java
import java.util.*;
import java.io.*;

public class classphoto {
public static void main(String[] args) throws IOException {

BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

int a = Integer.parseInt(br.readLine());

int b = Integer.parseInt(br.readLine());

System.out.println(a*b);

}

}

```











CHAT:
---

# 📝 Java Input Methods Cheat Sheet

## 1️⃣ Classic I/O Streams (`java.io`)

### Character-based (text)

- **`BufferedReader.readLine()`**
    
    ```java
    String line = br.readLine();
    ```
    
    • Fast. Reads an entire line of text (without the newline).
    
- **`BufferedReader.read()`**
    
    ```java
    int c = br.read();
    ```
    
    • Reads a single character (`int` 0–65535, `-1` for EOF).
    
- **`BufferedReader.read(char[] buf, int off, int len)`**
    
    ```java
    int n = br.read(buf, 0, buf.length);
    ```
    
    • Reads into a char array chunk at a time.
    
- **`Console.readLine()`**
    
    ```java
    String s = System.console().readLine();
    ```
    
    • Only works in a real terminal (not in most online judges or IDEs).
    

### Byte-based (binary)

- **`InputStream.read()`**
    
    ```java
    int b = System.in.read();
    ```
    
    • Reads one byte.
    
- **`InputStream.read(byte[] b)`**
    
    ```java
    int n = System.in.read(b);
    ```
    
    • Reads up to `b.length` bytes.
    
- **`BufferedInputStream.read(...)`**  
    • Buffered and faster for large binary input.
    
- **`DataInputStream.readInt()` / `readLong()` …**  
    • Reads Java primitive types in binary form.
    

---

## 2️⃣ Token-based Utilities

- **`Scanner`**
    
    ```java
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    String s = sc.next();
    ```
    
    • Easiest but **slow** (regex + synchronization). Fine for small input.
    
- **`StringTokenizer`**
    
    ```java
    StringTokenizer st = new StringTokenizer(line);
    String token = st.nextToken();
    ```
    
    • Very fast token splitter for whitespace or custom delimiters.
    
- **Custom FastReader**  
    • Implement your own byte buffer and parse digits manually.  
    • Fastest for tens of millions of integers (Codeforces/Kattis templates).
    

---

## 3️⃣ NIO (`java.nio` / `java.nio.file`)

- **`Files.readAllLines(Path)`**
    
    ```java
    List<String> lines = Files.readAllLines(Path.of("file.txt"));
    ```
    
    • Reads the entire file into memory as a list of lines.
    
- **`Files.lines(Path)`**
    
    ```java
    try (Stream<String> s = Files.lines(Path.of("file.txt"))) {
        s.forEach(System.out::println);
    }
    ```
    
    • Returns a lazy `Stream<String>` of lines.
    
- **`FileChannel` + `ByteBuffer`**  
    • Low-level, fast, good for very large files or memory mapping.
    
- **`MappedByteBuffer`**  
    • Memory-map a file for random access.
    

---

## 4️⃣ High-level Convenience

- `new Scanner(new File("input.txt"))` – read tokens from a file.
    
- `new BufferedReader(new FileReader("input.txt"))` – classic text-file reading.
    
- `Files.newBufferedReader(Path, Charset)` – NIO way with explicit charset.
    
- `Console.readPassword()` – secure password input (no echo).
    

---

## 5️⃣ Reading Different Types of Input

| Goal                      | Fast Competitive Way                                                                                                           | Simpler Way                                    |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| Single integer            | `int n = Integer.parseInt(br.readLine());`                                                                                     | `sc.nextInt();`                                |
| Single word               | `StringTokenizer st = new StringTokenizer(br.readLine()); String w = st.nextToken();`                                          | `sc.next();`                                   |
| Whole line                | `String line = br.readLine();`                                                                                                 | `sc.nextLine();`                               |
| Multiple ints on one line | `StringTokenizer st = new StringTokenizer(br.readLine()); while(st.hasMoreTokens()) int x = Integer.parseInt(st.nextToken());` | `while(sc.hasNextInt()) int x = sc.nextInt();` |
| Char by char              | `int c = br.read();`                                                                                                           | `sc.next().charAt(0);`                         |
| Binary data               | `System.in.read(byteArray);`                                                                                                   | —                                              |

---

## Competitive Programming Recommendations

- **Default template:**  
    `BufferedReader` + `StringTokenizer` for input, `PrintWriter` for output.
    
- **Massive input (10⁷+ numbers):**  
    Custom `FastReader` that reads bytes and parses digits manually.
    
- **Output:**  
    `PrintWriter` or `BufferedWriter`, flush once.
    

---

### Quick Summary Table

|Task|Best Choice (fast)|
|---|---|
|Line of text|`BufferedReader.readLine()`|
|Next word / token|`StringTokenizer.nextToken()`|
|Many ints quickly|Custom FastReader|
|Character-by-character|`BufferedReader.read()`|
|Binary file|`BufferedInputStream.read(byte[])`|
|Whole file as list of lines|`Files.readAllLines()`|
|Stream of file lines|`Files.lines()`|

---

_Tip:_ For contests, stick to **BufferedReader + StringTokenizer + PrintWriter**—it’s the standard fast I/O combo.