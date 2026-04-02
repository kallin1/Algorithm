## 알고리즘 수업 - 알고리즘의 수행 시간 5
### 문제
입력 크기 n이 주어지면 아래 알고리즘의 수행 시간을 출력해보자.
```
MenOfPassion(A[], n) {
    sum <- 0;
    for i <- 1 to n
        for j <- 1 to n
            for k <- 1 to n
                sum <- sum + A[i] × A[j] × A[k]; # 코드1
    return sum;
}
```

### 입출력
- 입력 : 첫째 줄에 입력의 크기 n(1 ≤ n ≤ 500,000)이 주어진다.
- 출력 :
  첫째 줄에 코드1 의 수행 횟수를 출력한다.
  둘째 줄에 코드1의 수행 횟수를 다항식으로 나타내었을 때 최고차항의 차수를 출력.
  (단, 다항식으로 나타낼 수 없거나 최고차항의 차수가 3보다 크면 4를 출력)


### 풀이과정
#### 코드 1은 몇 번 반복할까?
k, j, i 의 for문 모두 1부터 n까지로 n번씩 반복하므로 코드1은 총 n의 세제곱횟수만큼 반복하게 된다.

#### 코드 1의 수행시간을 다항식으로 나타내면?
f(n) = n^3

#### 최종 코드
```
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        long n = sc.nextInt();
        
        System.out.println(n*n*n);
        System.out.println(3);
    }
}
```
