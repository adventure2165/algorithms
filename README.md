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


## Coding Tips
- 정규식 공부 URL
https://programmers.co.kr/learn/courses/11

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


## 코딩시 고려해야할 점
  * 여태까지 그런적은 없었으나, 최근 2개의 코딩테스트 시험 시간이 1시간차이로 겹치는 상황이 발생하였다. 처음 있는 일이여서 전략을 짰으나, 난이도가 생각보다 쉽게 느껴진 나머지 두개 다 동시에 하는 멍청한 짓을 하였다. 명심하자. 하나만 집중하자. 2개 동시에는 절대 못한다.

## Commit message 에 대한 팁

- 참조할만한 좋은 링크 https://meetup.toast.com/posts/106

## Unit Test 
- Mocha : Javascript를 사용하는 Unit test 지원 프레임워크. 코딩테스트 사이트의 결과 보는거랑 같은 기능임.
  * Python에도 있는거 같은데 찾아보는중.
---------

## Reference Repo
- https://github.com/eagle705/algorithms : (eagle705) Thankyou!
