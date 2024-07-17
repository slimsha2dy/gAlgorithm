# Info
[뮤직 플레이리스트](https://www.acmicpc.net/problem/25049)

## 💡 풀이 방법 요약

n^2 는 분명 시간 초과가 난다느 것을 알 수 있습니다.

한 번 이상 완전 탐색을 해야하는 것은 자명하므로, logN 으로 반복했을 때의 최대값을 알 수 있다면 되겠죠.

그래서 이를 현재 인덱스를 기준으로 왼쪽에서의 부분수열의 최대값과 오른쪽에서의 부분수열의 최대값의 합을 가지도록 했습니다.

## 👀 실패 이유

## 🙂 마무리
