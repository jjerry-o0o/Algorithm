```java
import java.io.*;
import java.util.StringTokenizer;

public class Solved_15552 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int t = Integer.parseInt(br.readLine());
        int[] sum = new int[5];

        for (int i=0; i<t; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine(), " ");
            bw.write(Integer.parseInt(st.nextToken())+Integer.parseInt(st.nextToken())+"\n");
        }
        
        bw.flush();
        bw.close();
    }
}
```

처음에 쉽다 생각하고 문제를 풀었는데 런타임 에러가 났다.
난 바보같이 a+b 값을 배열에 담아 for문을 돌려 출력을 시키고 있었다.
결국 풀이방법을 찾아봤는데 엄청난 신세계를 발견할 수 있었다.

* StringTokenizer를 사용할때 바로 br.readLine()을 넣어줘도 된다는 것
* 해당 값을 더할때 변수에 한번 더 담지 않고 바로 st.nextToken 끼리 더해도 된다는 것
