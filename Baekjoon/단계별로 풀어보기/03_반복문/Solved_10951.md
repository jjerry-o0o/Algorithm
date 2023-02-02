```java
import java.io.*;
import java.util.StringTokenizer;

public class Solved_10951 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String str;
        StringTokenizer st;

        while((str=br.readLine()) != null){
            st = new StringTokenizer(str, " ");

            int a = Integer.parseInt(st.nextToken());
            int b = Integer.parseInt(st.nextToken());

            System.out.println(a+b);
        }
    }
}
```
