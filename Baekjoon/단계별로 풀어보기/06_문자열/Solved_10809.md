```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solved_10809 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String str = br.readLine();
        int cnt = 0;
        int arr[] = new int[26];

        for (int i = 0; i < 26; i++) {
            arr[i] = -1;
        }

        //a = 97, b = 98...z = 122
        for (int i = 0; i < str.length(); i++) {
            int a = str.charAt(i);
            cnt = 0;
            for (int j = 97; j <= 122; j++) {
                if(a == j && arr[cnt] == -1){
                    arr[cnt] = i;
                    break;
                }
                cnt++;
            }
        }

        for (int i = 0; i < 26; i++) {
            System.out.print(arr[i]+" ");
        }
    }
}
```
