algorithms
=========
improving algorithm skills!
========

# Coding Test를 준비하기 위한 개인 저장소
- 1일 1문제 목표
- 기본 난이도 부터 시작하여 영어, 고난도까지 포괄
- 최대한 빠른 시간에 푸는 것을 목표로 진행
- 백준(한글)
- Codility(영문)
- 프로그래머스(한글)
-----------

## 대표 취약 유형 대비

- BFS
- DFS
- DP
- 정규식
- 공부하면서 향후 추가 예정


## Coding Test Mind 
- 난이도 있는 문제는 언어영역처럼 잘 읽어서 이해부터 해야한다.
- 문자열은 정규식을 사용하면 매우 강력하고 편하게 사용할 수 있다. 정규식을 잘 사용하자.
- Collection 라이브러리는 Python에서 기본 제공하면서도 매우 유용하게 사용할 수 있다.
  * Deque : 양쪽 Queue
  * Counter : 리스트,딕셔너리,문자열 등의 안의 문자나 원소 갯수를 세어서 원소 : 갯수 이렇게 해서 딕셔너리 형으로 반환
- Itertools 라이브러리 또한 Python에서 기본 제공하면서도 매우 유용하다.
  * 곱집합 사용 가능 (Product 사용)
  * 순열과 조합 사용 가능(Permutation, Combination)
  * 이외 다양한 기능 존재. 필요 취합하면 좋음.
- Copy 라이브러리또한 사용하면 좋음 Python은 할당을 할때 주소할당을 하기 때문에 똑같은걸 할당한뒤 하나를 변경하면 다른것도 변경되기 때문에 Deepcopy를 통해서 아예 다른 존재로 만들어 줘야 서로 연동이 안됨.
- Python의 Dictionary는 key와 Value를 동시에 저장하는 기능이 있어서 마치 Node처럼 사용 가능하다. Node의 값 : key의 값, Value : 다음 노드를 나타냄 이렇게 사용가능 하므로 그래프 문제에서 매우 잘 사용할 수 있음.
- 쉬운 함수 - ord()는 해당 문자의 ASCII값을 반환함. C처럼 바로 int화하면 해당값이 반환되는 것이 아님. 숫자를 ASCII값으로 문자 변환을 원하면 chr()을 쓰면 됨.
- 처음부터 완벽한 풀이가 있으면 바로 그것으로 풀면 문제 없을텐데, 풀었을 때 예상치 못하게 부분점수가 나올 경우가 있다. 이때 어떻게 해야하는지는 상황에 따라 다르긴 하겠지만... 확실하게 이렇게 하는게 좋겠다
	1. 반례가 확실히 보이는데 해당 반례가 조금만 수정하면 되는 것이 확실한 경우 : 기존 코드 수정
	2. 반례가 확실히 보이고, 해당 반례가 조금만 수정하면 되는 것이 불확실한 경우 : 다시 새로 푸는게 낫다.
	3. 반례가 불확실해서 어떻게 될지 모르겠다 : 시간이 부족하다면 그냥 제출부터 해놓고... 아니면 다시 새로풀자.
- Numpy와 Pandas를 사용하는 코딩테스트도 존재한다. Numpy는 성능을 중요시하며, For문을 대신하여 Where(For + if)기능을 사용하는것이 좋다.
- Python의 Time Complexity에 관련되어서 매우 유용한 사이트 - https://choisblog.tistory.com/26
	1. 여기에 따르면 큐는 collections.queue를 사용하라 한다. 시간성능이 엄청차이난다 한다. queue.Queue도 안된다 함. 이건 멀티스레딩을 위해 만들어진 큐이고 매우 느리다 함.
	2. 파이썬의 재귀 깊이는 기본적으로 최대 1,000. sys.setrecursionlimit으로 조절 가능하다.
	3. int / int == float. int화(몫)은 // 사용
	


## Coding Tips
- 정규식 공부 URL
https://programmers.co.kr/learn/courses/11

- 정규식 테스트 사이트 : 매우 유용! 정규식을 치면 바로 즉각즉각 결과를 알려준다. 정규식의 결과를 눈으로 즉각 보면서 할 수 있으므로 정말 좋음!!!
https://regexr.com/


- What is Enum?
  * 열거형이라고도 부름. 고유한 상숫값에 연결된 기호 이름(멤버)의 집합. 열거형 내에서, 멤버를 아이덴티티로 비교할 수 있고, 열거형 자체는 이터레이트 될 수 있음.
  * 우선 import enum을 해주어야 함. 다른 언어랑 다름.
  * class Color(Enum): 이렇게 상속을 해서 사용가능
	RED = 1
	Blue = 2
	Green = 3

  * 뭐 Color.RED 이렇게 접근 가능.
  * for i in Color 사용가능.
  * 같은 이름의 멤버는 존재할 수 없음. (RED = 1, RED = 2 이건 안됨)
  * 다른 이름인데 값은 다른건 별칭 개념으로 생각하면 됨.(RED = 1, BBALGANG = 1 이건 됨.)

- Mutable 과 Immutable
  * 둘의 차이는 쉽게 예를 들어 설명하면 다음과 같다.

  ```X = abcde```
  ```Y = X```
  * 이렇게 하면 X랑 Y는 같은 값을 가진다. 
  * 근데 Mutable한 것은 
```Y = Y+"f"```
```X = abcdef```
```Y = abcedf(X랑 동일)```
  * 이렇게 되어버림.
  * Immutable은 위의 연산을 하면
```X = abcde```
```Y = abcdef```
  * 가 되는 것이다.
  * Call by reference에 의해 Y=X와 같이 똑같은것을 할당할 때 아예 새로 만들어 버리는건지, 아니면 주소를 똑같이 해서 가리키는것을 같이 하는건지 차이다.
  * 리스트, 딕셔너리, set - Mutable
  * 숫자, 문자열, 튜플 - immutable
  * immutable 한 것은 뭐 추가를 하던 수정을 하던 하면 수정을 하는게 아니라 아예 새롭게 수정된 결과를 반환해준다.

- try, else, except, finally
  * try : 일단 try 인덴트 안의 코드를 실행해 보아라.
  * except: try 인덴트 안의 코드에서 예외가 발생시 실행하여라. 반드시 try랑 같이 사용하여야 한다.
  * else : try 인덴트 안의 코드에서 예외가 한번이라도 발생 안하면 실행한다. for - else 이렇게 쓸수도 있는데, 이때에는 for에서 break가 발생 할 경우 else를 실행하지 않고 그냥 종료한다. 하지만 무사히 for가 다 돌았으면 else 안의 코드를 실행한다.(While도 동일하게 사용 가능하다.)
  * finally : else와 except가 다 끝나고 나면 마지막에 실행

## 코딩시 고려해야할 점
  * 여태까지 그런적은 없었으나, 최근 2개의 코딩테스트 시험 시간이 1시간차이로 겹치는 상황이 발생하였다. 처음 있는 일이여서 전략을 짰는데, 한개가 어려우면 바로 넘어가고, 아니면 그냥 계속 풀기로 했다. 그런데 처음본 한개가 난이도가 생각보다 쉽게 느껴진 나머지 두개 다 동시에 하는 멍청한 짓을 하였다. 명심하자. 하나만 집중하자. 2개 동시에는 절대 못한다.
  * 문제를 풀어야할 때 반드시 구현해야하는 것인 경우, 귀찮아하지 말고 제대로 구현할것. 진법변환이라던지 이런것이 해당됨. 꼼수쓰려하지말고 구현하는게 더 빠름.
  * 문제 푼게 실행시 자동으로 점수가 반영되는 경우도 있는데 프로그래머스같은 애들은 자동으로 반영 안되는 경우도 있다. 코드 채점 버튼으로(실행 말고) 기록을 남겨야만 점수가 주어질 수 있다. 이를 반드시 명심해야한다.

## Commit message 에 대한 팁

- 참조할만한 좋은 링크 https://meetup.toast.com/posts/106

## Unit Test 
- Mocha : Javascript를 사용하는 Unit test 지원 프레임워크. 코딩테스트 사이트의 결과 보는거랑 같은 기능임.
  * Python에도 있는거 같은데 찾아보는중.
---------

## Reference Repo
- https://github.com/eagle705/algorithms : (eagle705) Thankyou!
- https://awesomeopensource.com/project/graykode/nlp-roadmap?fbclid=IwAR1e_1K4ouiwVfgBx9UgVSwPLer6vc9Vbjwj0owMIWB8LnYl7UJCjChSzBk NLP Road Map
