
```java

import java.io.*;
import java.util.StringTokenizer;

public class Solved_1000 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        String str = br.readLine();
        StringTokenizer st = new StringTokenizer(str, " ");
        int a = Integer.parseInt(st.nextToken());
        int b = Integer.parseInt(st.nextToken());

        bw.write(a+b+"");
        bw.flush();
        bw.close();
    }
}

```

1. 문자열 형태로 사용자가 입력한 값을 한줄 모두 str에 담는다
2. StringTokenizer(문자열을 여러개의 토큰으로 분리해주는 클래스)를 이용하여 공백을 기준으로 str을 분리해준다
3. a와 b에 각각 토큰을 하나씩 담는다
4. BufferedWriter는 int형을 출력할 수 없으므로 공백을 더해주어 문자열로 변환 후 출력해준다
