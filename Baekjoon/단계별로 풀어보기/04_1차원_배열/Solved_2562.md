```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Arrays;

public class Solved_2562 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int[] arr = new int[9];
        int[] copy = new int[9];

        for (int i = 0; i < 9; i++) {
            arr[i] = Integer.parseInt(br.readLine());
            copy[i] = arr[i];
        }

        Arrays.sort(arr);
        int cnt = 0;

        for (int i = 0; i < 9; i++) {
            cnt++;
            if(arr[8] == copy[i]) {
                break;
            }
        }
        System.out.println(arr[8]);
        System.out.println(cnt);
    }
}
```
