## 알고리즘 수업 - 알고리즘의 수행 시간 1
### 문제
입력 크기 n이 주어지면 아래 알고리즘 수행 시간을 출력해보자.
```
MenOfPassion(A[], n) {
    sum <- 0;
    for i <- 1 to n
        sum <- sum + A[i]; # 코드1
    return sum;
}
```

### 입출력
- 입력 : 첫째 줄에 입력의 크기 n이 주어진다.
- 출력 :
  첫째 줄에 코드1의 수행 횟수를 출력한다.
  둘째 줄에 코드1의 수행 횟수를 다항식으로 나타내었을 때, 최고차항의 차수를 출력한다.
  (단, 다항식으로 나타낼 수 없거나 최고차항의 차수가 3보다 크면 4를 출력한다.)

### 문제 풀이 과정
#### 코드 1은 몇 번 실행될까?
재귀는 없으나 반복이 존재. i가 1부터 n까지 도달할때까지 총 n번 반복한다.
결국 시간은 O(n)만큼 소요

#### 수행 횟수를 다항식으로 나타내면?
f(n) = n
최고차항의 차수는 1이다!

#### 최종 코드
```
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc = new Scaner(System.in);
        int n = sc.nextInt();
        
        System.out.println(n);
        System.out.println(1);
    }
}
```
