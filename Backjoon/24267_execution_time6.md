## 알고리즘 수업 - 알고리즘의 수행 시간 5
### 문제
입력 크기 n이 주어지면 아래 알고리즘의 수행 시간을 출력해보자.
```
MenOfPassion(A[], n) {
    sum <- 0;
    for i <- 1 to n - 2
        for j <- i + 1 to n - 1
            for k <- j + 1 to n
                sum <- sum + A[i] × A[j] × A[k]; # 코드1
    return sum;
}
```

### 입출력
- 입력 : 첫째 줄에 입력의 크기 n(1 ≤ n ≤ 500,000)이 주어진다.
- 출력 :
  첫째 줄에 코드1의 수행 횟수를 출력한다.
  둘째 줄에 코드1의 수행 횟수를 다항식으로 나타내었을 때 최고차항의 차수를 출력.
  (단, 다항식으로 나타낼 수 없거나 최고차항의 차수가 3보다 크면 4를 출력)


### 풀이과정
#### 코드 1은 몇 번 반복할까?
중첩 반복문의 규칙을 보자.
i는 1부터 n-2까지,
j는 i+1부터 n-1까지
k는 j+1부터 n까지
결국 1부터 n까지의 숫자 중에서 서로 다른 3개의 숫자 i, j, k를 중복 없이 순서에 상관 없이 뽑는 경우의 수다.
따라서 n개중에 3개를 선택하는 조합 공식을 사용할 수 있다.
n(n-1)(n-2)/6

#### 코드 1의 수행시간을 다항식으로 나타내면?
f(n) = n(n-1)(n-2)/6

#### 최종 코드
```
import java.util.Scanner;

public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        long n = sc.nextInt();
        
        System.out.println(n*(n-1)*(n-2)/6);
        System.out.println(3);
    }
}
```
