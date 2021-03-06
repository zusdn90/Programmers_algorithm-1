# <span style="color: orange; font-size:17pt">프로그래머스(Programmers) 코딩테스트 연습</span>
# <span style="color: orange; font-size:17pt">LEVEL 1 문자열 내 마믐대로 정렬하기 연습문제 자바(java) 풀이</span>
- [프로그래머스 문자열 내림차순으로 배치하기](https://programmers.co.kr/learn/courses/30/lessons/12917)
<br><br>

# <span style="color: red; font-size:15pt">문제 풀이<span>
이 문제를 푸는 방법 2가지를 생각했습니다.  
속도는 아무래도 1번이 평균적으로 훨씬 빠릅니다.  
1. 오름차순으로 sorting한 다음에 뒤에서 부터 거꾸로 넣어준다.
2. 모든 문자를 탐색하면서 뒤의 값이 더 크다면 바꿔준다. (모두 탐색)
<br><br>

# <span style="color: red; font-size:15pt">1번 풀이<span>
문자를 char 배열 형태로 바꾸어 이를 바로 내림차순으로 정렬할 수도 있고 오름차순으로 정렬하고 뒤에 부터 넣어줄 수 있습니다.  
예를들어 abcdef가 있다면 이를 오름차순 하면 abcdef입니다.  
내림 차순은 반대이므로 뒤에부터 쓰면 fedcba로 내림차순이 됩니다.  
<br><br>

# <span style="color: red; font-size:15pt">2번 풀이<span>
이는 버블 정렬을 통해 그때 그때 뒤의 값이 크다면 자리를 바꿔줍니다.  
i번 인덱스와 i+1 부터 문자열끝 문자까지 모두 비교해 나갑니다.  
예를 들어 "Zbcdefg"가 있다면 처음에 Z와 b를 비교해 b가 더 크기 때문에 자리를 바꿔줍니다. bZcdefg  
다음 b와 c를 비교해서 cZbdefg. c와 d를 비교해서 dZbcefg... 이렇게 자리를 바꿔나갑니다.  
그러면 문자는 i전까지의 문자들, i문자, i~j사이의 문자, j문자, j~문자열 끝 으로 나뉘게 되므로 이를 '+'연산을 통해 concat 해주면 됩니다.