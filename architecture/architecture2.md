#Architecture
####Architecture에서 중요한 것은 무엇인가?
사용자의 니즈
####객체지향에서 중요한 것은 무엇인가?
변화(확장)에 대한 용이성을 포함한 재사용성의 재고    
Readable은 모든 프로그래밍에서 추구해야 하는 부분이고
####Ojbect-Oriented Architecture는
사용자의 니즈를 객체지향적으로 시스템에 반영해야
##Use case
사용자의 니즈를 **사용자의 행동과 시스템의 니즈로 구체화** 한 것
####A Use Case Driven Approach
Use case를 중심(기반)으로 architect    
####Use case와 delivery가 분리되어야 하는 이유
Delivery는 변할 수 있는 부분    
사용자가 웹으로 요청하든, 콘솔로 요청하든 동일한 니즈에 동일한 아키텍처를 적용    
좋은 아키텍처의 조건이라기 보단 좋은 **객체지향 아키텍처**의 조건
>분리는 use case와 delivery 사이에서만 필요한 것이 아니다. use case와 entity, entyty와 db사이에도 필요하다.

###Use case 정의
>**주문 생성**
>Data:
>`<customer-id>`, `<customer-contact-info>`, `<shipment-destination>`
>Primary Course:
>1. 수주 담당자가 주문 데이터를 입력
>2. 시스템이 데이터를 검증
>3. 시스템이 주문을 생성하고 주문 아이디를 결정
>Alternative Course:
>예외 상황 등에 대한 flow 정의

반드시 위 예제의 형식을 따라야 하는 것은 아님    
특정 환경(delivery 등)에 비종속적인 사용자의 액션과, 시스템의 처리 그리고 시스템의 응답을 정의

>비종속성을 유지하기 위해서는 use case를 중심으로 추상화가 필요

###Use case algorithm과 Use case object
Use case algorithm을 객체 지향적으로 설계하면 use case가 의존하는 객체들을 다루는 로직(객체들을 생성하고 객체의 메소드들을 호출 하는 등)의 관리 책임을 가질 객체가 필요하며 이 책임을 갖는 객체가 use case objects
##Partitioning
Use case를 central organizing principle이 되게 하면서 객체 지향적으로 시스템을 나누기
###아키텍처를 구성하는 3개의 fundamental objects
- Entities
- Boundaries
- Interactors

####Entities
Application 독립적인(당연히 use case 독립적인) 비지니스 로직    
다른 Application 에서도 entity는 사용할 수 있어야(객체지향적이어야)    
Application 종속 메소드는 use case object가 갖어야

####Interactors
Use case objects에 해당    
Application 종속적 비지니스 로직    

####Boundaries
Use case와 delivery와의 의존성을 없애기 위한 objects    
Interface 등의 abstract objects로 use case와 delivery가 의존성을 가짐    

####UML
![architecture](https://raw.githubusercontent.com/unitimes/study-clean-coders/master/architecture/architecture.png)
>사실 완벽하게 Dependency inversion principle을 지켰다고 보긴 힘들다    
>Use case와 entity, entity와 database 사이의 의존성도 Interface를 통해 이루어져야 DIP를 지켰다고 할 수 있음

