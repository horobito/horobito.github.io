---
title: "Basic Concept 1"
category: "sololearn"
tags: "java"

permalink: /sololearn/basic_conecept1
layout: single
---


# 01. Introduction of java 

- 컴파일
  \- 개발자가 작성한 보기 쉬운 코드를
    기계가 이해할 수 있도록 재해석하는 과정



- 컴파일의 필요성

  \- 기존 언어
   : 소스코드 -> 컴파일 -> IL(중간언어)
  ->'가상머신'에서 기계어(ex) 윈도우 기계어, 리눅스 기계어) 변환 후 실행

  \> 공통요소 : 소스코드 ...... 가상머신에서 읽을 수 있는 중간언어까지

  \> 기존 언어는 **"운영체제"**가 프로그램을 실행

  cf) 중간언어 : 가상머신에서 읽을 수 있는 언어
  cf2) 소스코드 : 프로그래머가 프로그래밍 언어로 작성한 코드, 설계도 역할

  \- 자바

  : 자바는 운영체제 앞에 하나의 가상머신**(JVM)**을 두어,
  그곳에서 컴파일된 코드를 실행시켜줌



- 자바의 특징
  \1. 한번 작성하면, 어디에서나 작동
  \2. 플랫폼에 구애받지 않는다
  \3. portable
  \4. 객체와 객체 사이에서 일어나는 관계들을 묘사하는 언어



# 02. A hello world Program



## 1. your firtst java program 

```
class MyClass{
  public static void main(String[] args){
     System.out.println("Hello World")
  }
}
```

- 자바에서 **실제로 작동**하는 코드들은
  **클래스** 내부에 존재해야 함
  -> 클래스의 이름은 항상 **대문자**부터 시작

ex) 위의 예시에서 코드들은 MyClass 내부에 존재



cf) 클래스
   : **객체**를 만들어 낼 설계도



- 자바에서는 프로그램 실행 시 **시작점**, 또는 **입구**가 존재,
  이를 main 이라는 이름의 method, 즉 **main method**라고 한다.



- 요약
  \1. 자바 내 모든 프로그램은 반드시 클래스를 가져야 한다.
  \2. 모든 자바 프로그램은 **main method**에서부터 시작이 된다.



**1.5. method**



- 메소드
  : 특정 **기능**을 제공하는 코드
- 메소드의 **정의** & **호출**

- **[정의, define]** : 메소드를 **만드는** 것
  ex)

```
public class Method{
   public static void numbering(){
     int i = 0;
     While(i<10){
        System.out.println(i);
         i++;
     }  
  }
}
```

- **[호출, call]** : 만들어진 메소드를 **실행**,

```
public class Method{
   public static void numbering(){
     int i = 0;
     While(i<10){
        System.out.println(i);
         i++;
     }  
   }
   public static void main(String[] args){
       numbering(); // 메소드의 호출
   }
}
```





## 2. main method



- main method은 반드시 이러한 시그니처로 인식된다.

```
public static void main(String[] args){}
```

\1. public

: **'누구나 접근이 가능'** 을 의미 - 접근제한자의 한 종류



\2. static

: 'main method를 포함하는 클래스의 **instance**를 만들지 않고, 실행할 수 있는다.' 라는 의미



\3. void : '어떤값도 return하지 않음' 을 의미



\4. main

: 그 method의 이름,

실행의 진입점, **코드 실행 시 jvm(자바 가상머신)이 제일 먼저 찾아 실행하게 되는 것**

따라서, 자바가 실행이 될 때**, main이라고 불리는 method를 가장 먼저 호출**

cf) **하나의 프로그램은 하나의 메인메소드를 가진다.**



cf) 메소드 시그니처

: 메소드 블록( {} ) 외의 메소드들의 반환형, 접근 제한자, 파라미터 등을 모아서 부르는 것



ex) test라는 메소드의 선언

```
void test();
```

- 요약
  \1. 메소드 파라미터는 메소드이름 뒤에 오는 괄호() 안에 선언된다.
  \2. main 문에서의 파라미터는 String type의 args라는 이름을 가지는 배열이다.



cf) 객체와 인스턴스

- 객체(Object) : 소프트웨어 세계에 구현할 대상, 

- 클래스(Class)

: 위의 객체를 구현하기 위한 설계도, **변수(상태)**와 **메소드(행동)**을 가짐

- 인스턴스(Instance) : 이 설계도에 따라 소프트웨어 세계에 구현된 실제



- 객체(Object)는 현실의 대상(Object)와 비슷하지만,
  소프트웨어 관점에서는 그저 컨셉(concept), 즉 **사유의 결과**
- 소프트웨어에서 객체를 구현하기 위해서는
  컨셉 이상으로 많은 것들을 사고하고 구현해야 하므로,
  이를 위한 설계도로 클래스를 작성
- **설계도를 바탕으로 객체를 소프트웨어에 실체화** 하면 그것이 바로 instance
  -> 이 과정을 **‘인스턴스화(instantiation)’**이라 하며,
  **실제화된 인스턴스는 메모리에 할당된다.**



참고

https://cerulean85.tistory.com/149

[cerulean85.tistory.com](http://cerulean85.tistory.com)



cf) 파라미터

-  메소드 안에서 선언된 변수, 바깥의 값을 **복사**해 넣는 것
- 함수를 호출하기 위해 필요한 파라미터
  : 호출을 위한 관심사
-  함수를 호출하기 위해 필요한 중간 매개체를 만들기 위해 필요한 파라미터
  : 생성을 위한 관심사



### 2.5 입력과 출력



- 입력
  \- 메소드의 입력 : **매개변수**와 **인자**라는 것을 통해
  \- 인자 : 어떤 **함수를 호출**시에 **전달**되는 **값**
- 매개변수 : 그 전달된 **인자를 받아들이는 변수**

ex)

```
public class InputOutput{
   public static void numbering(int limit){
  // 매개변수 int limit
    : 이것은 인자를 통해 들어온 정수값을 받아 메소드 내에 보냄
     int i =0;
       while(i<limit){
          System.out.println(i);
         i++
       }
   }
   public static void main(Sting[] args){
    numbering(5); /*
   여기서의 5 : 인자
   컴퓨터가 numbering을 만나면,
   numbering이라는 method를 호출하기 위해서
   그 메소드의 정의로 이동,
   이때 괄호한의 limit에 호출 시 기입한 5라는 숫자를
   전달하게 된다.
  ]
}
```

- 인자와 매개변수는 여러개가 가능

```
public class InputOutput{
   public static void numbering(int inin, int limit){
     int i = inin;
       while(i<limit){
       System.out.println(i);
        i++;
      }
  }
  public static void main(String[] args){
     numbering(3,5);
```



### 3. system.out.println() 

- method의 **body**는 **중괄호 안**에 존재한다.

ex)

```
public class{
  public static void main(String[] args){
    System.out.println("Hello World");
  }
}
```

- println 메소드 : 한 줄의 문장을 화면에 표시
- **System**클래스와, 이것의 **‘out’** stream
  -> println method에 접근하기 위해 사용됨.



- 요약
  \- 클래스 내에서
  메소드, 기타 다른 flow-control structures 들은
  항상 중괄호( { } ) 내에 존재한다.



### 4. semicolons in java

- println method에 매개변수로 다른 텍스트를 전달해서
  출력할 수 있다.

ex)

```
class MyClass{
   public static void main(String[] args){
     System.out.println("I am learning java");
   }
}
```

- 자바에서, 각 코드문은 반드시 **;** 로 끝나야 한다.



- 요약
  -뒤에 중괄호를 사용하여 정의된 **body가 뒤따르는**
    method 및 class의 선언 시,
    ; 를 사용하지 말아야 한다.





﻿
