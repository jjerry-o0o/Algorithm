```java
import java.io.*;
import java.util.StringTokenizer;

public class Solved_3003 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        String str = br.readLine();
        StringTokenizer st = new StringTokenizer(str, " ");
        int k = Integer.parseInt(st.nextToken());
        int q = Integer.parseInt(st.nextToken());
        int l = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());
        int n = Integer.parseInt(st.nextToken());
        int p = Integer.parseInt(st.nextToken());

        bw.write(1-k+" ");
        bw.flush();
        bw.write(1-q+" ");
        bw.flush();
        bw.write(+2-l+" ");
        bw.flush();
        bw.write(2-b+" ");
        bw.flush();
        bw.write(2-n+" ");
        bw.flush();
        bw.write(8-p+"");
        bw.flush();
        bw.close();
    }
}
```
