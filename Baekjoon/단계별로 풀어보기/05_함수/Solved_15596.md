```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solved_15596 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int a[] = new int[n];
        StringTokenizer st = new StringTokenizer(br.readLine());

        for (int i = 0; i < n; i++) {
            a[i] = Integer.parseInt(st.nextToken());
        }

        sum(a);
    }

    public static long sum(int[] a) {
        long sum = 0;
        for (int i = 0; i < a.length; i++) {
            sum += a[i];
        }
        return sum;
    }
}
```
다시 확인해보니 내가 문제를 잘못 이해한 거였다. 함수만 작성하면 되는 문제였다. 그래서 다시 풀어보았다.
```java
public class Test {
    long sum(int[] a) {
        long ans = 0;
        for(int i=0; i<a.length; i++){
            ans += a[i];
        }
        return ans;
    }
}

```
