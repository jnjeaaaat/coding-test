# 프로그래머스
## ad 제거하기
</br>

### 문제
[ad 제거하기](https://school.programmers.co.kr/learn/courses/30/lessons/181870)
</br></br>

### 풀이
``` java
import java.util.*;

class Solution {
    public String[] solution(String[] strArr) {
        List<String> answer = new ArrayList<>();
        
        for (String s : strArr) {
            if (!s.contains("ad")) answer.add(s);
        }
        
        return answer.toArray(new String[answer.size()]);
    }
}
```
</br>

### 풀이 과정
문자열 배열 `strArr`에서 “ad”를 포함하지 않는 문자열만 반환하는 문제이기 때문에

List를 사용해 “ad”가 없는 문자열만 add 시켜주는 방법을 택함

`forEach`문으로 `contains`메소드를 사용해 **“ad”를 포함하지 않는 문자열**이라면 List에 추가

그렇게 만들어진 answer은 다시 문자열 배열로 변환해 return
