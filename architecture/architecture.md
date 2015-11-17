#Architecture
##Architecture란 무엇인가?
전체 시스텝 개발에 기반을 제공하는 **변경 불가**한 초기 결정사항의 집합	
>Tool, building material 등이 아니라 **사용법**에 대한 것

결국 use case에 대한 이야기를 담고 있어야
##Use Case란 무엇인가?
목적(Goal)을 달성하는 과정에서 이루워지는, 책임(사용자)과 시스템 간 상호작용을, 순차적으로 정의해 놓은 것	
Use case는 delivering 메커니즘, UI, DB, Frame work, tools 등에 대한 결정과 완전히 decouple 해야	
>Use case should stand alone

##Deferring Decisions
좋은 아키텍처는 Stuff(ie. framework, WAS, Ui 등)에 대한 결정이 연기될 수 있어야 하고, 연기되어야만 한다.	
Stuff에 대한 정보는 시간이 지날 수록 정보가 풍부해지고 얼마든지 변경될 수 있다.	
따라서 아키텍처는 stuff에 의존해서는 안 됨	

##Central Abstraction
무엇이 중요한 추상화 인지에 대한 고민 필요	
서비스의 핵심 기능에 관련된 추상화가 중요한 추상화