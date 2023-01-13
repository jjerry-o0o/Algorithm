```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solved_2884 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        String str = br.readLine();
        StringTokenizer st = new StringTokenizer(str, " ");

        int h = Integer.parseInt(st.nextToken());
        int m = Integer.parseInt(st.nextToken());

        if(m-45 < 0) {
            m = 60 - (45 - m);
            if(h == 0){
                h = 23;
            }else {
                h = h - 1;
            }
        }else {
            m = m - 45;
        }
        System.out.println(h + " " + m);
        
    }
}
```
