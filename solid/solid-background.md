#SOLID Foundation
- The Source code is the design
- Engineers makes source code

###집 짓는 것과 소프트웨어를 만드는 것은 달라야
건설은 결과물의 수정이 설계보다 훨씬 어렵다    
소프트웨어는 결과물의 수정이 설계보다 훨씬 쉽다    

>설계 : 소스 코드 = 결과 : 바이너리 코드    

**`#Evolutionary architecture and emergent design, #Agile, #TDD`**    

###Bad Design Smells
####**Rigidity**    
변경하기 어려운 디자인    
####**Fragility**    
부분(한 모듈)의 변경이 다른 부분에 영향을 미치는 디자인    
####**Immobility**    
모듈이 쉽게 추출 되지 않고 재사용 되지 않는 디자인    

객체가, 계층이, 모듈이 서로 밀접하게 연관(coupling)되어 있는 디자인    

Dependency(runtime level)는 유지한채로 Decoupling(source code level)

###Needless Complexity
앞으로의 확장(변화)를 고려하다바면 불필요하게 시스템이 복잡해 짐    
현재 요구 사항에 집중하고 OOD로 앞으로의 확장에 유연함을 확보    

**`#agile, #OOP, #TDD`**    

###OOP    
**High level don't depend on low level**    
Inversion of Control(IoC)를 실현    
>Client(high level)는 used object에 대한 레퍼런스를 가진다. 이를 역전시키는 것이 IoC이며, 이는 인터페이스를 사용하으로써 실현    

###OO    
**Dynamic polymorphism**    
어떻게 동작하는지는 모르고 무엇을 원하는 지를 전달    
>**Static polymorphism**    
>Compile 시점에 어떤 메소드가 호출 될 지 결정    
>ex. method overloading    

> **Dynamic polymorphism**
> Runtime 시점에 어떤 메소드가 호출 될 지 결정    
> ex. method overloading    

```
class Animal {    
   public void move(){
      System.out.println("Animals can move");
   }
}

class Dog extends Animal {
   public void move() {
      System.out.println("Dogs can walk and run");
   }
}

public class TestDog {

   public static void main(String args[]) {
      Animal a = new Animal(); // Animal reference and object
      Animal b = new Dog(); // Animal reference but Dog object

      a.move();//output: Animals can move
      b.move();//output:Dogs can walk and run
   }
}
```    

때문에 **Dependency Inversion**이 OO의 정수    
IoC를 통해 **상위 레벨의 모듈을 하위 레벨의 모듈로 부터 보호**하는 것이 OO의 핵심    

###OOD    
**Dependency Management**    

####**SOLID**    
의존성 관리 원칙    
- Single Responsibility Principle
- Open Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependency Inversion Principle    

