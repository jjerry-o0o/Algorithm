```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solved_4344 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int C = Integer.parseInt(br.readLine());

        for (int i = 0; i < C; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            int N = Integer.parseInt(st.nextToken());
            int arr[] = new int[N];
            int sum = 0;
            int avg = 0;

            for (int j = 0; j < N; j++) {
                arr[j] = Integer.parseInt(st.nextToken());
                sum += arr[j];
            }
            avg = sum/N;
            double cnt = 0;

            for (int j = 0; j < N; j++) {
                if (avg < arr[j]) {
                    cnt++;
                }
            }
            double rate = cnt/N*100;
            System.out.printf("%.3f",rate);
            System.out.println("%");
        }
    }
}
```
