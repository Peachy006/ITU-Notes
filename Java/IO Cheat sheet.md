# 🧾 Java I/O Cheat Sheet

> For competitive programming (Kattis-style).  
> Fast input/output with `BufferedReader`, `StringTokenizer`, and `PrintWriter`.

---

## 📥 INPUT

### 🧱 Basic Setup
```java
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        PrintWriter out = new PrintWriter(System.out);
    }
}

🧠 Read a Single Line

String line = br.readLine();

✂️ Split a Line by Spaces

String[] parts = line.trim().split("\\s+");
int a = Integer.parseInt(parts[0]);
int b = Integer.parseInt(parts[1]);

📋 Read Integers into an ArrayList

ArrayList<Integer> list = new ArrayList<>();
String[] parts = br.readLine().trim().split("\\s+");
for (String p : parts) {
    list.add(Integer.parseInt(p));
}

⚡ StringTokenizer (faster for large input)

StringTokenizer st = new StringTokenizer(br.readLine());
int a = Integer.parseInt(st.nextToken());
int b = Integer.parseInt(st.nextToken());

Loop version:

StringTokenizer st = new StringTokenizer(br.readLine());
while (st.hasMoreTokens()) {
    int num = Integer.parseInt(st.nextToken());
    // do something
}

🔁 Read Multiple Lines

int n = Integer.parseInt(br.readLine());
for (int i = 0; i < n; i++) {
    String line = br.readLine();
    // process line
}

♾️ Read Until EOF

String line;
while ((line = br.readLine()) != null) {
    // process line
}

📤 OUTPUT
🖨️ Basic Printing

out.println("Hello");
out.println(42);

🧾 Formatted Output

out.printf("x = %d, y = %d%n", x, y);

🚿 Flush or Close

out.flush();  // ensures everything prints
out.close();  // closes output stream

🔢 Type Conversions

int x = Integer.parseInt("123");
long y = Long.parseLong("456789");
double z = Double.parseDouble("3.14");
String s = String.valueOf(x);

🧩 Common Patterns
📦 Read N Integers into Array

int n = Integer.parseInt(br.readLine());
int[] arr = new int[n];
StringTokenizer st = new StringTokenizer(br.readLine());
for (int i = 0; i < n; i++) {
    arr[i] = Integer.parseInt(st.nextToken());
}

📄 Print Array in One Line

for (int i = 0; i < arr.length; i++) {
    out.print(arr[i]);
    if (i < arr.length - 1) out.print(" ");
}
out.println();

🧮 Sorting

Arrays.sort(arr); // for arrays
Collections.sort(list); // for ArrayList
Collections.sort(list, Collections.reverseOrder()); // descending

⚙️ Pro Tips

    🧠 Always use BufferedReader + PrintWriter for speed.

    🚫 Avoid Scanner — it’s much slower.

    🪶 StringTokenizer is best for reading many numbers fast.

    ✂️ readLine() reads the whole line (you must split it manually).

    🧼 Use .trim() to remove stray spaces before splitting.
    
    
    
    