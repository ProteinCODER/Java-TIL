# 상속



 ###  부모 클래스

       ``` java
public class A {
 int field1;
 void method1() {...}
 }
       ```

###  

### 자식 클래스

```java
public class B extends A {
 String field2;
 void method2(){...}
}
```



---

* 다중 상속 허용하지 않는다



 ## 부모 생성자 호출

```java
DmbCellPhone dmbCellPhone = new DmbCellPhone();
```

---

```java
public DmbCellPhone () {
 super();
}
```

* 부모 생성자는 `자식 생성자의 맨 첫 줄`에서 호출된다.



##  메소드 재정의

> @override
>
> 메소드 오버라이딩은 상속된 메소드의 내용이 자식 클래스에 맞지 않을 경우, 자식 클래스에서 동일한 메소드를 재정의 하는 것을 말한다.

* 부모의 메소드와 `동일한 시그너처`를 가져야 한다.
* 접근 제한을 더 강하게 오버라이딩 할 수 없다.
* 새로운 예외를 `throws` 할 수 없다.



<h6>부모 클래스</h6>

```java
public class Carculator
 double areaCircle(double r) {
  system.out.println("Calculator 객체의 areaCircle() 실행");
  return 3.14159 *r *r;
  }
}
```



<h6>자식 클래스</h6>

```java
public class Computer extends Calculator {
 @Override
 double(areaCircle(double r)) {
  System.out.println("Computer 객체의 areaCirlcle() 실행");
  return Math PI *r r;
 }
}
```



<h6>오버라이딩</h6>

```java
public class ComputerExample
public static void main(Stirng[] argu) {
 int r= 10;
 
 Carculator carculator = new Calculator;
 system.out.println("원면적: " + computer.areaCircle(r));
 system.out.println();
 
 Computer computer = new Computer();
 System.out.println("원면적: "+computer.areaCircle(r));
}
```



# 부모 메소드 호출(super)

```java
super.부모 메소드();
```

* 자식 클래스 내부에서 오버라이딩된 부모 클래스 메소드를 호출해야하는 상황이 발생하며 명시적으로 super 키워드를 붙여서 호출





# final 클래스 와 final 메소드

  ### 상속할 수 없는 final 클래스

* 클래스 선언시 앞에 final을 붙이면 최종 클래스가 되어 상속할 수 없는 클래스가 되어버린다.

### 오버라이딩 할 수 없는 final 메소드

* 부모클래스를 상속해서 자식클래스를 선언할 때 부모 클래스에 선언된 final 메소드는 자식클래스에서 재정의 할 수 없다.