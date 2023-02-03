```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solved_1110 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int N = n;
        int cnt = 1;

        while(true) {
            int a = N / 10;
            int b = N % 10;

            int sum = a + b;

            int c = sum % 10;
            int newN = b * 10 + c;

            if (newN == n) {
                System.out.println(cnt);
                break;
            } else {
                N = newN;
                cnt++;
            }
        }
    }
}
```

위 코드가 너무 지저분해서 구글링 후 코드를 조금 정리해보았다.

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solved_1110 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int copy = n;
        int cnt = 0;

        do {
            n = (n % 10) * 10 + (((n / 10) + (n % 10)) % 10);
            cnt++;
        }while(n != copy);

        System.out.println(cnt);
    }
}
```
