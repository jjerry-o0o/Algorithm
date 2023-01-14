```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Solved_2525 {
    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        String str = br.readLine();
        StringTokenizer st = new StringTokenizer(str, " ");

        int hour = Integer.parseInt(st.nextToken());
        int minute = Integer.parseInt(st.nextToken());

        int ovenTime = Integer.parseInt(br.readLine());

        if(minute+ovenTime >= 60) {
            hour = hour + ((minute+ovenTime)/60);
            if (hour >= 24)
                hour = hour - 24;

            minute = minute + ovenTime - ((minute + ovenTime)/60)*60;
        }else {
            minute = minute + ovenTime;
        }

        System.out.println(hour + " " + minute);
    }
}
```
