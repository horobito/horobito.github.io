---
title: "잘 되는건가"
category: "java_grammar"
tags: "ggg"

---

# 제목

내용
---

## 01. Exception Handling

### 1 . Exception

- 정의
  \- 프로그램 동작 과정 중 일어나는 문제

- 예외는 프로그램의 비정상적인 종료를 야기한다.

- Exceptioin Handling 
  \- runtime error을 조정하여
    기존 애플리케이션의 flow를 유지시키는
     강력한 기구

- 에러가 발생하는 몇 가지 이유들
  \1. 유저가 유효하지 않는 데이터에 접근
  \2. 필요한 파일을 찾을 수 없을때
  \3. 네트워크 연결이
    통신 과정 중 끊길때,
  \4. 부족한 메모리 &
     기타 하드웨어적 요소로 인한 문제
  => 에러는 유저, 프로그래머,  하드웨어적 요소 등
       다양한 원인들로 인해 일어남

- 예외를 잡을 수 있는 키워드
  **- try & catch**

- try & catch 블럭은
  **예외를 일으킬 수 있는 코드 주변에**
  **배치**된다. 
  ex)

  ```
  try{
    // some code;
  }catch(Exception e){
     // some code to handle errors
  }
  ```

  - catch 문
    : 잡아내려 하는 exception의 타입의 선언을
      포함한다.
      ex) Exception e

- 동작 원리
  \- 만약 try 블럭 내에서
    예외가 일어날 경우,
    try 다음에 오는 catch 블럭이
    이를 잡아낸다. 

  \- 발생한 Exception의 타입이
     catch 블럭 내에 list 되어 있다면,
     exception은 마치
     인자가 멤소드의 파라미터로 이동하는 것과 같이
     catch 블럭 내로 이동한다.

  \- **Exception 타입**은 모든 가능한  exception들을
     잡아낼 수 있다. 



- 존재하지 않는 배열 index에 접근을 시도 할 때,
  발생하는  exception의 handling을 보여주는 예제

  ```
  public class MyClass{
    public static void main(String[] args){
      try{
        int a[] = new int [2];
        System.out.println(a[5]);
      }catch(Exception e){
        System.out.println("An error occurred");
      }
    }
  }
  ```



- try/catch 블럭이 없을 경우,
  찾고자 하는 index가 존재하지 않기 때문에
  프로그램은 crash 가 발생한다.
- 주목할 점
  catch 블럭 내의 (Exception e) 구문
  -> 모든 가능한 예외들을 잡아낼 때 사용된다. 







## 02 . Mutiple Exception

### 1 . throw 

- 기능
  \- 메소드로부터 exception들을 
    수동으로 생성하는 것을 가능하게 할 때 사용

  \- 사용가능한 많은 exception 타입은
   [IndexOutOfBoundException],
   [IllegalArgumentException],
   [ ArithmeticException ]   을 포함한다.

  

- 파라미터가 0일때 
  ArithmeticException을 throw 하는 예제

  ```
  int div(int a, int b) throw ArithmeticException{
    if(b==0){
      throw new ArithmeticException("Division by Zero");
    }else{
      return aa/b;
    }
  }
  ```

  

- 메소드정의 에서의 throw 구문은 
  메소드가 throw 할 수 있는 exception(s)의
  타입을 정의한다.

- throw 키워드는
  custom 메세지와 함께 대응하는 exception을 throw 한다.
  ex)
  위 예제에서
  div 메소드를 호출 할 때,
  두 번째 파라미터 b 가 0이면,
  이 메소드는 “Division by Zero” 와 함께
  ArithmeticException 을 throw 한다. 

- Multiple Exception은 
  ,로 구분되는 list를 사용하여
  throw 구문 안에서 정의된다. 



## 2. Exception Handling 

- 하나의 try 블럭은
  다수의 catch 블럭을 가지며,
  이를 통해 서로 다른 예외들을 처리할 수 있다.
  ex)

  ```
  try{
    // 실행하고자 하는 코드
  }catch(ExceptionType1 e1){
    // ExceptionType1 e1 일 때의 코드 
  }catch(ExceptionType2 e2){
    // ExceptionType2 e2 일 때의 코드 
  }catch(ExceptionType3 e3){
    // ExceptionType3 e3 일 때의 코드 
  }catch(ExceptionType4 e4){
    // ExceptionType4 e4 일 때의 코드 
  }
  ```



- 규칙
  \- 모든 catch블럭은 반드시
    구체적인 범위에서 일반적인 범위 순서대로 
    위치되어야 한다.

  \- Exception 타입을 사용하여
  마지막 catch에서  앞에서 catch되지 않은
  모든  exception들을 catch 할 수 있다. 





## 03. HashMap

### 1 . HashMap

- 배열과 List는 정렬된 원소들의 집합을 가지며,
  각각의 원소들은 **정수형 index**를 가진다. 
