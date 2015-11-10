#TDD
##The Three Laws of TDD
1. Write NO production code except to pass a failing test.
>production code가 없는 상태에서는 모든 test가 failing test,
>**test code 부터 작성**하라는 뜻

2. Write only ENOUGH of a test to demonstrate a failure.
3. Write only ENOUGH production code to pass the test.

##TDD 절차
![Image of Flow]
(https://github.com/unitimes/study-clean-coders/blob/master/tdd/flow.png?raw=true)
한 사이클을 완전히 완수하고 다음 사이클로 넘어가야 한다
즉 하나의 failing test에 대한 일련의 절차를 마무리 하고 다음 failing test를 작성
##원칙&팁
작은 기능, 간단한 기능 부터 테스트
>**생성자**부터, 즉 오브젝트가 만들어지는지부터 확인

최소한의 코드로 production code 작성
##TDD의 잇점
TDD의 법칙을 잘 따르면 설계 문서를 얻게된다

>Test code를 보면 코드를 어떻게 사용하는 지, 어떻게 구현했는 지를 알 수 있다

낮은 결합성을 갖게 됨
시스템의 정상 작동 여부를 쉽게 확인
