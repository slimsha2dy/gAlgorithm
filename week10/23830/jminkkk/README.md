# Info
[MEX](https://www.acmicpc.net/problem/23820)

## 💡 풀이 방법 요약
"sum(scores) < S 가 true가 나오는 K 구하기"

~~보자마자 이진탐색 생각남 하지만 연속인가? yyyynnn가 아닐듯?~~ 

1. 일단 각 score는 무조건 아래 4가지 중 하나
   + score 
   + score += q
   + score -= p
2. 최소인 K = 얼마나 +연산을 많이 시킬 수 있도록 하여 S를 만드냐
3. 불가능한 경우를 제외하고 "+ 연산을 시켜야 하는 점수가 몇 개"여야를 구해야 함
   + 0부터 N까지 탐색하기
4. 몇개인지 구한 후 그 수가 무엇인지 최소로 구하기 
   + 무조건 -1인 경우는 모든 a에 다 +연산을 해도 S를 못 넘는 경우
## 👀 실패 이유


```java
3
0 1 2
1 1 3 1
```
## 🙂 마무리
