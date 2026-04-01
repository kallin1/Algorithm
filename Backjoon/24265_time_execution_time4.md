## 알고리즘 수업 - 알고리즘의 수행 시간 3
### 문제
입력 크기 n이 주어지면 아래 알고리즘의 수행 시간을 출력해보자.
```
MenOfPassion(A[], n) {
    sum <- 0;
    for i <- 1 to n - 1
        for j <- i + 1 to n
            sum <- sum + A[i] × A[j]; # 코드1
    return sum;
}
```

### 입출력
- 입력 : 첫째 줄에 입력의 크기 n(1 ≤ n ≤ 500,000)이 주어진다.
- 출력 :
  둘째 줄에 코드1의 수행 횟수를 다항식으로 나타내었을 때 최고차항의 차수를 출력.
  (단, 다항식으로 나타낼 수 없거나 최고차항의 차수가 3보다 크면 4를 출력)


### 풀이과정
#### 코드 1은 몇 번 반복할까?
외부 for문은 n-1만큼 반복,
내부 for문은 루프마다 i가 증가하기 때문에 도는 횟수가 1씩 줄어든다. 
따라서 내부횟수를 전체 더하면 (n-1)+(n-2)+...+1 = n(n-1)/2이다.

#### 코드 1의 수행시간을 다항식으로 나타내면?
f(n) = n(n-1)/2

#### 최종 코드
```
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        long n = sc.nextInt();
        
        System.out.println(n*(n-1)/2);
        System.out.println(2);
    }
}
```
이전에 매번 동일한 횟수로 반복하는 문제는 내부,외부 for문을 곱하여 게산했으나
횟수가 변하면 합으로 계산해야한다.
