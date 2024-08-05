# Info
[Link](https://boj.kr/31778)
## 💡 풀이 방법 요약

P는 왼쪽에, C 는 오른쪽으로 보내버리면 되지 않을까?

투 포인터로 P 와 C 가 들어갈 다음 위치를 가리키고 있다면??

아니면, 왼쪽에서부터 한 칸씩 보면서 C 가 나오면 오른쪽 끝에서부터 처음 나오는 P와 위치를 바꾸면?

오른쪽 포인터 = 오른쪽에서부터 처음 P 의 위치 왼쪽 포인터 = 왼쪽에서부터 처음 C의 위치

총 K번 움직였어. 개수는 어떻게 카운트 하지?

누적합을 이용해서 특정 위치 이전의 P 개수, 특정 위치 이후의 C 개수를 찾을 수 있음!!!

왼쪽에서부터 탐색 시작, 처음 C가 나오는 위치에서 이전의 P 개수 추출 => 누적합

동시에 현재 인덱스를 포함해 C 개수 추출 => 위에서 찾은 두 수를 통해 계산! 

두번째 C가 나왔을 때는 첫번째 C 이전의 P 만으로 2개 뽑는 경우를 제외해야 함! 이를 따로 저장해두고 있었음!

```Java
// 처음 C 가 나오는 인덱스 기준으로 그 이전의 P, 그 이후의 C 계산, 그 뒤에 C가 나오는 기준으로
long lastPCount = 0;
for (int i = 1; i <= n; i++) {
    if (chars1[i] == 'P')continue;
    long p = pSum[i] - pSum[0];
    long c = cSum[n] - cSum[i-1];
    pccCount += (p * (p-1) / 2L - lastPCount) * c;
    lastPCount = p * (p-1) / 2L;
}
```

## 👀 실패 이유
String.indexOf 메서드가 값이 없으면 -1을 반환하는데, 이걸 처리를 안했음.
## 🙂 마무리