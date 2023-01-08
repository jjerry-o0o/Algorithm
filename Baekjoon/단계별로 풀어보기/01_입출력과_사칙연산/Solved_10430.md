```java
import java.io.*;
import java.util.StringTokenizer;

public class Solved_10430 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        String str = br.readLine();
        StringTokenizer st = new StringTokenizer(str, " ");

        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());
        int c = Integer.parseInt(st.nextToken());

        bw.write((a+b)%c+"");
        bw.newLine();
        bw.write(((a%c)+(b%c))%c+"");
        bw.newLine();
        bw.write((a*b)%c+"");
        bw.newLine();
        bw.write(((a%c)*(b%c))%c+"");
        bw.flush();
        bw.close();
    }
}
```
