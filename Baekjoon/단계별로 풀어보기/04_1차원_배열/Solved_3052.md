```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Arrays;

public class Solved_3052_1 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int[] arr = new int[10];
        int cnt = 0;

        for (int i = 0; i < 10; i++) {
            arr[i] = Integer.parseInt(br.readLine())%42;
        }

        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                if(arr[i] == arr[j] && i != j){
                    arr[j] = 42;
                }
            }
        }
        
        Arrays.sort(arr);
        
        for (int i = 0; i < 10; i++) {
            if(arr[i] == 42) {
                break;
            }
            cnt++;
        }
        System.out.println(cnt);
    }
}
```

내 코드가 너무 길고 지저분한 것 같아서 다른 분의 코드를 참고해봤다.

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.HashSet;

public class Solved_3052_2 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        HashSet<Integer> hs = new HashSet<Integer>();

        for (int i = 0; i < 10; i++) {
            hs.add(Integer.parseInt(br.readLine()) % 42);
        }
        System.out.println(hs.size());
    }
}
```
