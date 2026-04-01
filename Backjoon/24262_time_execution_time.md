## 알고리즘 수업 - 알고리즘의 수행 시간 1

### 문제
입력의 크기 n이 주어지면 MenOfPassion 알고리즘 수행 시간을 예제 출력과 같은 방식으로 출력해보자.

MenOfPassion 알고리즘은 다음과 같다.
```
MenOfPassion(A[], n) {
    i = ⌊n / 2⌋;
    return A[i]; # 코드1
}
// 배열 A와 크기 n을 받는 함수
```


### 입출력
- 입력 : 첫째 줄에 입력의 크기 n(1<=n<=500,000)이 주어진다.
- 출력 : 
첫째 줄에 코드1의 수행 횟수를 출력한다. 
둘째 줄에 코드1의 수행 횟수를 다항식으로 나타내었을때, 최고차항의 차수를 출력한다.
(단, 다항식으로 나타낼 수 없거나 최고차항의 차수가 3보다 크면 4를 출력한다.)


### 풀이 과정
#### 코드1은 몇 번 실행될까?
반복, 조건, 재귀는 없다.
i는 한 번, return 또한 한 번씩 진행

#### 수행횟수를 n에 대한 식으로 쓰면?
f(n) = 1
즉, 차수는 0이다.

+) n이 커지면 실행 횟수가 변할까? 그건 아니다. 

#### 입력 크기랑 상관없이 실행 횟수가 일정하면 O(1), 차수는 0이다!

#### 최종 코드
```
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        
        System.out.println(1);
        System.out.println(0);
    }
}
```
입력 요구사항을 맞추기위해 Scanner를 사용하긴했으나 실제로 시간계산에 사용하지 않으므로 과감히 생략해도 될 것 같다. 실제로 제외하고 제출해도 정답처리 된다.
