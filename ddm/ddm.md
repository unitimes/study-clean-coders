#Developing Domain Model
##개발순서
**Static에서 Action으로**
##Static Model
클래스, 클래스의 속성, 클래스간 관계를 정의    
아직 메소드는 정의 하지 않음    
##Adding Actions
###책임과 상호작용을 식별하여 행위를 결정
####책임
**클래스의 책임**    
클래스가 무엇을 알고 무엇을 해야 하는 지
####상호작용
클래스가 책임 수행을 위해 어떤 클래스에 의존해야 하는 지
###책임과 상호작용을 식별하는 절차
어플리케이션이 처래해야 하는 **요구사항** 분석   
요구사항을 바탕으로 도메인 모델이 **노출해야 하는 인터페이스** 정의    
TDD 접근법으로 **인터페이스 구현**
###요구사항 식별
####요구 사항 구분
사용자 요구사항은 **사용자 행위**와 **어플레케이션 응답**으로 구성    
어플리케이션 응답은 곧 **책임**에 해당
####책임의 구분
책임은 **로직**과 **출력**으로 다시 구분    
로직은 **서비스 메소드**에 출력은 **리파지토리 메소드**에 해당
####결국 클라이언트는 도메인 티어를 2번 호출
서비스, 리파지토리 각 한번씩
##테스트와 mock
mock 객체를 이용하면 collaborator 구현이 필요 없기 때문에 타깃 테스트에 집중 가능