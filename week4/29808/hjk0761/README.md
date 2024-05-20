# Info
[29808 너의 수능 점수가 궁금해](https://www.acmicpc.net/problem/29808)

## 💡 풀이 방법 요약

TMI: 처음에 두 수의 선형 결합은 두 수의 최대공약수로 나눠어짐을 이용해서 어떻게 해보려고 했는데, 결국 이렇게 해도 an + bm 의 관계에서 n, m 을 구해야 했었다. 그래서 그냥 처음부터 구해줬다.

정수이기 때문에 s = an + bm 에서 m = (s - an) // b 이므로 n에 따라 가능한 m을 일일이 찾았다.

## 👀 실패 이유

0일때 처리를 못해줘서 틀렸다.

## 🙂 마무리

변수명 문과 이과입니다.