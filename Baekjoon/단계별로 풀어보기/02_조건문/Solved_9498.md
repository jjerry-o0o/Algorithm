```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solved_9498 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(br.readLine());

        if(100 >= n && n >= 90) {
            System.out.println("A");
        }else if(89 >= n && n >= 80) {
            System.out.println("B");
        }else if(79 >= n && n >= 70) {
            System.out.println("C");
        }else if(69 >= n && n >= 60) {
            System.out.println("D");
        }else {
            System.out.println("F");
        }
    }
}
```
