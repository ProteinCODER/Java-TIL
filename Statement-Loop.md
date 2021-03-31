# 조건문

##  1. 중첩IF문

> 임의의 정수 뽑기
>
> `int num = (int) (Math.random() * 제한점 ) + 더할 숫자 ;`
>
> <b>더할 숫자<= 임의의 정수 < 제한점</b>

``` java
if(~~) {
  if(**) {
   grade = "A+" ;
  } else {
------
```

##  2. SWITCH 문

- 변수 값에 따라서 실행문이 결정되기 때문에 같은 기능의 IF 문보다 코드가 간결하다.

``` java
임의의 정수 뽑기 후
    타입 변수 = (타입) (Math.random()*n) + N ;
    switch(변수) {
            case N     // 이후 ``` 이어나가기
                break ; 
    }
```

##  

# 반복문

##  1. FOR 문

1) 초기화식이 제일 먼저 실행

2) 조건식을 평가해서 TRUE 면, 실행문을 실행. FALSE 면 FOR문 종결.

3) 블록 내부 실행문 모두 실행되면, 증감식 실행 후 다시 조건식 평가

``` java
for(int i= 1; i<= 10; i++) {
    //for(초기화식, 조건식, 증감식)
}
```

- 구구단

``` java
for(int i= 2; i<=9; i++) {    //2단부터 9단까지 ~
    System.out.println("*** "+ i + "단 ***");
    for(int j=1; j<=9; j++) {   // 1부터 9 곱하는 ~
        System.out.println(i+" X "+J+"= "+i*j);
    }
}
```

##  2. WHILE 문

- 시작할 때 부터 조건식을 검사하여 블록 내부를 실행할지 결정
- FOR문은 정해진 횟수만큼 반복한다면, WHILE 문은 조건식이 TRUE 일 경우에 계속해서 반복

```
변수 선언
while(조건식) {
 실행문
  i ++;
}
```

##  3. DO-WHILE 문

- 블록 내부의 실행문을 우선 실행시키고 , 실행 결과에 따라서 반복 실행할지 결정하는 경우 사용

``` java
do {
    실행문;
} while { 조건식} ;
```

- DoWhile 문 예제

```java
Scanner scanner = new Scanner(System.in); // scanner 객체 생성
String inputString ;

System.out.println("메시지를 입력하세요");
System.out.println("q를 입력하면 종료됩니다");

do{
  System.out.println(">");
  inputString = scanner.nextLine();      // 키보드로 입력한 문자열을 얻음
  System.out.println(inputString);
  } while( ! inputString.equals("q"));   // ! 논리 부정 연산자

System.out.println();
System.out.println("프로그램 종료");
    
 }
}
```

