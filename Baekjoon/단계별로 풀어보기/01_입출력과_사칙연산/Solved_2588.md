```java
import java.io.*;

public class Solved_2588 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int A = Integer.parseInt(br.readLine());
        int B = Integer.parseInt(br.readLine());

        int B3 = B%10;
        int B2 = (B-B3)/10%10;
        int B1 = (B-B3-B2)/100%10;

        bw.write(A*B3+"");
        bw.newLine();
        bw.write(A*B2+"");
        bw.newLine();
        bw.write(A*B1+"");
        bw.newLine();
        bw.write((A*B3)+(A*B2*10)+(A*B1*100)+"");
        bw.flush();
        bw.close();
    }
}
```
