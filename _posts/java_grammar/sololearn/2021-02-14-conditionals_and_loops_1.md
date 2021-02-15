---
title: "Conditionanls and Loops(1)"
category: "sololearn"
tags: 
- Java
- Sololearn
- Grammar
---

﻿

## 01. Conditional Statements



### 1. Decision Making[의사결정]



- Conditional statements[조건문]
  : 서로 다른 조건을 기반으로 서로 다른 행동들을 수행할 때 사용



- if statement[if 문]
  \- 가장 흔히 사용되는 조건문

  \- if 문의 조건이 참으로 평가될 경우,
    if 문 안의 블록에 있는 문은 실행된다.

  \- if 문의 조건이 거짓으로 밝혀질 경우,
    if문 바로 바깥(if문의 중괄호 바깥)의 첫번째 코드가 실행된다.

```
if(condition){
  // 조건이 참일 경우 실행
}
```

- 다음 비교 연산자들을 이용하여 조건문을 구성할 수 있다.

1) < : 미만

2) > :  초과

3) != :  같지 않음

4) == :  같음

5) <= :  이하

6) >= :  이상



ex)



```
class ConditionStatement{
   public static void main(String[] args){
       int x = 7;
       if(x<8){ //조건문 :  x<8 일 경우 참
            System.out.println("Hi") // 조건문이 참일 경우 실행
       }
   }
}
```

- 주의
  \* == : 두 값이 같은지 확인하는 표시
  \* = : 배정연산자를 의미





### 2. if ....else Statements[if...else 구문]



- **if문**은 뒤에 선택적으로**else 문**이 뒤따를 수 있다.
- else : 조건이 false일 때 실행

ex)

```
int a = 30;

if(a<30){
   System.out.println("Too Young");
}else{
   System.out.println("Welcome!");
}
```

- if 문의 조건이 거짓이라 판명되어 else문이 실행됨





### 2. Nested if Statements 



- if-else 문 안에 다른 if-else 문을 넣을 수 있다.

ex)

```
if(age>=0){
   if(age>16){
      System.out.println("welcome");
   }else{
      System.out.println("Too young");
   }
}else{
   System.out.println("0이상의 값을 넣으시오")
}
```

- 요약
  : if-else 문을 원하는 많큼 엮을 수 있다.







### 3. else if Statements



- if -else문을 엮는 대신,

**else if** 문을 사용해 다양한 조건을 검토 가능

ex)

```
int age = 25;

if(age<=0){
    System.out.println("Error");
}else if(age<=15){
    System.out.println("Too Young");
}else if(age<100){
    System.out.println("Welcome")
}else{
    System.out.println("Really?")
}
```

- 필요한 만큼 else if 문을 사용할 수 있다.







## 04. Logical Statements



### 1. Logical Operators[논리연산자]



- 논리연산자
  : 다양한 조건들을 묶을 때 사용



- AND 논리 연산자
  : **여러 조건을 만족할 경우에만** 출력하고 싶을 경우 사용

ex) 나이 18세 이상, 돈 500이상 조건일 경우에만 출력하고 싶을 경우

방법1. if 문을 엮어서 사용

```
if(age>18){
   if(money>500){
      System.out.println("Welcome")
   }
}
```



방법2. AND 논리 연산자(&&) 사용할 경우 더 좋은 방법이다.

```
if(age>18&& money>500){
   System.out.println("Welcome!")
}
```

- 두 operand 모두 참일 경우, 조건문은 참이 된다.



### 2. The OR Operator



- OR Operator(||) 는
  조건 중 한가지가 참일 때 참이다.



ex)

```
int age = 25;
int money = 100;

if(age>18 || money 500){
   System.out.println("Welcome!");
}
```

- 조건문에서 둘 중 하나라도 참이면 조건은 참 값을 나타낸다.



- Not(!) 논리 연산자
  \- 조건문을 뒤집을 때 사용
  \- 조건이 True일 경우,
     NOT 논리 연산자는 그것을 False로 만듬

```
int money = 25;
if(!(age>18)){ // 조건문 의미 : 나이가 18살보다 많지 않을 경우
  System.out.println("미성년 출입금지")
}else{
  System.out.println("어서오세요!!!!!")
}
```

- 논리 연산자 사용 시 팁
  \- &, | : 두 피연산자를 모두 평가해서 true,false를 산출
  \- &&: 두 피연산자 중 하나라도 false 면 비교를 멈추고 false 값을 산출
  \- | |: 두 피연산자 중 하나라도 true 라면 비교를 멈추고 true 값을 산출



## 05. The switch Statement



### 1. The switch Statement



- switch statement
  \- 변수들의 목록에 대하여 **어떠한 변수가 같은 값을 갖는지** 테스트를 한다.
  \- 각각의 값들은 **case**라고 불린다.
- switch 된 값들은 각각의 case마다 검사가 된다.

```
import java.util.Scanner;

public class NHN11 {ㄴ
    public static  void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();
        switch(score){
            case 30 : // case 30 과 score가 일치하는지 확인
                System.out.println("시험을 발로 봤구나?");
              // case와 변수가 일치할 경우 실행
                break;
            case 60 :
                System.out.println("전액 등록금 축하한단다!");
                break;
            case 80 :
                System.out.println("출석점수가 굉장하구나!");
                break;
            case 90 :
                System.out.println("A를 받았구나!!");
                break;
            case 100 :
                System.out.println("등록금이 아깝지 않구나");
        }
    }
}
```

- switch 된 변수가 case와 같을 경우
  이 다음 **명령문은 break문에 도달할 때까지 실행**된다.
- \> 만약 break문이 없다면???

```
public class NHN11 {
    public static  void main(String[] args){
        int score = 30;
        switch(score){
            case 30 : // case 30 과 score가 일치하는지 확인
                System.out.println("시험을 발로 봤구나?"); // case와 변수가 일치할 경우
            case 60 :
                System.out.println("전액 등록금 축하한단다!");
                break;
        }
    }
}
/*
시험을 발로 봤구나?
전액 등록금 축하한단다
*/
```



- break문에 도달한 경우,
  switch는 끝나고 제어 흐름은 switch 문 다음의 줄로 이동함



- 모든 case에 break가 필요한 것은 아니다.
  만약 break 가 없다면, 제어 흐름은 break에 도달할 때까지
  후속 case로 넘어간다.



### 2. The default Statement



- switch 문은 선택적으로 default 값을 가진다.



- **default case**는 변수가 case에 일치하지 않는 경우 작업을 수행한다.

```
import java.util.Scanner;

public class NHN11 {
    public static  void main(String[] args){
        int score = 50;
        switch(score){
            case 30 : // case 30 과 score가 일치하는지 확인
                System.out.println("시험을 발로 봤구나?"); // case와 변수가 일치할 경우
            case 60 :
                System.out.println("전액 등록금 축하한단다!");
                break;
            default:
                System.out.println("무슨 점수를 받았는지 참으로 궁금하구나");
        }
    }
}
```

- **default case 는은 항상 switch의 마지막 문**이므로, **break가 필요하지 않다.**





﻿