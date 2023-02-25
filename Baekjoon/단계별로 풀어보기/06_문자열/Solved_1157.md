```java
package level_6;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Arrays;

public class Solved_1157_1 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String str = br.readLine();
        String upperStr = str.toUpperCase();
        System.out.println("upperCase = "+ (int)upperStr.charAt(0));
        //A~Z 26칸 배열을 만든다
        int arr[] = new int[26];
        //A-65를 해서 일치한 N번째 칸에 +1을 해준다
        for (int i = 0; i < upperStr.length(); i++) {
            for (int j = 0; j < 26; j++) {
                if(j == (int)upperStr.charAt(i)-65){
                    arr[j]++;
                }
            }
        }
        //해당 배열을 sort 한다
        Arrays.sort(arr);
        //앞에 두 수가 동일하면 ? 출력, 다르면 0번째 값만 출력한다.
        if(arr[25] == arr[24]){
            System.out.println("?");
        }else{
            char a = (char)(arr[25]+65);
            System.out.println((char)(arr[25]+64));
        }

    }
}

```
문제를 다 못 풀었다... 내일 꼭 풀거다. 
```java
package level_6;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class Solved_1157_2 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String str = br.readLine();
        int arr[]  = new int[str.length()];
        int result[] = new int[str.length()];

        for (int i = 0; i < str.length(); i++) {
            arr[i] = str.charAt(i);
        }

        Arrays.sort(arr);

        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < 26; j++) {
                if(arr[i] == j+65){
                    result[i]++;
                }
            }
        }

        Arrays.sort(result);

        if(result[result.length-1] == result[result.length-2]){
            System.out.println("?");
        }else{
            System.out.println(result[result.length-1]);
        }

    }
}

```
고민하다 결국 다른분 답안을 참고했다.
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Solved_1157_3 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int[] arr = new int[26];
        String str = br.readLine();

        for (int i = 0; i < str.length(); i++) {
            if('a' <= str.charAt(i) && str.charAt(i) <= 'z') {
                arr[str.charAt(i) - 97]++; //소문자인 경우
            } else {
                arr[str.charAt(i)-65]++; //대문자인 경우
            }
        }
        int max = -1;
        char ch = '?';
        for (int i = 0; i < 26; i++) {
            if(arr[i] > max) {
                max = arr[i];
                ch = (char)(i+65);
            }else if (arr[i] == max) {
                ch= '?';
            }
        }
        System.out.println(ch);
    }
}
```
