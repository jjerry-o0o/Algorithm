````java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solved_25304 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int x = Integer.parseInt(br.readLine());
        int n = Integer.parseInt(br.readLine());
        int a, b;
        int sum = 0;

        for (int i = 0; i < n; i++) {
            String str = br.readLine();
            StringTokenizer st = new StringTokenizer(str, " ");
            a = Integer.parseInt(st.nextToken());
            b = Integer.parseInt(st.nextToken());
            sum = sum + a * b;
        }

        if (sum == x) {
            System.out.println("Yes");
        }else{
            System.out.println("No");
        }
    }
}
