```java
import java.io.*;

public class Solved_8958 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int n = Integer.parseInt(br.readLine());
        String arr[] = new String[n];

        for (int i = 0; i < n; i++) {
            arr[i] = br.readLine();
        }

        for (int i = 0; i < n; i++) {
            int cnt = 0;
            int sum = 0;

            for (int j = 0; j < arr[i].length(); j++) {
                if(arr[i].charAt(j) == 'O') {
                    cnt++;
                }else {
                    cnt = 0;
                }
                sum += cnt;
            }
            bw.write(sum+"\n");
        }
        bw.flush();
        bw.close();
    }
}
```
기존에 풀던 방식으로 2시간 고민하다가 도저히 답이 안보여서 다른 사람의 풀이를 참고하였다.
내가 얼마나 바보 같고 힘든 방법으로 풀고 있던건지 알 수 있었다.
