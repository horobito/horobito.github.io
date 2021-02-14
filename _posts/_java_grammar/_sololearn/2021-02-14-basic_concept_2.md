

## 03. java commnets



### 1.Comments[주석]

- 목적
  : 그 코드가 무엇을 하는지 설명해주기 위해 작성
- 주석 내 모든 글자들은 자바 컴파일러에 의해 무시된다.
- 한 줄의 주석은 // 로 시작한다.



ex)

```
﻿x=10; // 이렇게 한줄짜리 주석은 주석을 붙이고 싶은 코드 옆에 //를 작성후 적으면 됨
```



### 2. Multi-Line Comments

- 여러줄의 주석을 적고 싶다면
  /* ~~~~*/ 방식으로 적으면 됨

```
x= 10;
/* 나는 여러줄의
주석을 적을겁니다.
*/
```



## 04. Variable[변수]



### 1. 변수

- 변수

- 변 : 변할 변

- 수 : 여기서는 숫자가 아닌 모든 데이터를 의미

=> 변수는 [변할 수 있는 데이터] 를 의미

- 처리할 데이터를 저장, 저장된 데이터는 다른 데이터로 바뀔 수 있다.

- 변수는 이름( 또는 **식별자(identifier) )**을 가진다

- 모든 변수들은 타입을 가진다.



- 변수의 선언

  \* 선언
  : 그것이 있다는 것을 컴퓨터에게 알려줌,
  즉 어떤것을 생성하는 것

  *처음 선언 시 값이 정해지지 않은 상태

  *형태 : '변수의 타입' + ' 변수의 이름' + ';'

  -> 변수의 타입 : 정확히는 **변수에 저장될 데이터의 타입**을 의미

ex)

```
﻿int a; // int 타입의 a라는 이름을 같는 변수를 선언한 것, 즉 변수를 만든 것
```

- 변수의 타입
  : 선언된 변수에 담길 수 있는 데이터의 타입을 의미,
  이 예제에서는 이 변수에는 정수 타입의 데이터만 담길 수 있다는 것을 의미



- 할당
  : 선언된 것에 대입연산자(=)를 통해 데이터를 할당 한 것

ex)

```
int a = 10; // a라는 변수에 10이라는 데이터를 할당
```

- 초기화
  : 선언 후 값을 '최초'로 '할당' 하는것,
   즉 선언된 것에 최초로 값을 넣어주는 것



- 할당과 선언을 동시에 할 수 있다.

ex)

```
String name = "홍길동"
 // name이라 불리는 String 타입의 변수에 "홍길동" 이라는 값을 할당한 것
```

- 데이터 타입
  \- bit : 0과 1 => 2개 표현 가능
  \- byte : 8비트 => 2^8개 표현 가능



1) Primitive Type[원시자료형, 기본자료형, 자료형]

(1) 정수형 : 소수부가 존재하지 않는 모든 수

◈ byte : 1byte, => 2^8개 표현 가능, -2^7 ~ 2^7 -1

◈ short : 2 byte, => 2^16개 표현 가능, -2^15 ~ 2^15 -1

◈ int : 4byte => 2^32개 표현 가능, -2^31 ~ 2^31 -1

◈ long : 8 byte => 2^8=64개 표현 가능, -2^63 ~ 2^63 -1

(2) 실수형 : 소수부가 존재하는 모든 수

◈ float :4 byte

◈ double : 8byte

(3) 논리형

◈ boolean : true or false

ex) boolean a = true;

(4) 문자형

- char : 한 '글자'



2)Reference Type[참조 자료형]

- 원시 자료형을 제외한 모든 경우

- 참조 자료형으로 저장소(ex. 변수) 를 만들었을 경우,
  이때 생성된 것을 객체(object)라고 하며, 사용된 클래스를 객체의 타입이라 한다.

- 참조형 변수 선언
  ex)클래스 형의 변수 선언
  -> '클래스 이름' + '식별자(이름)' + ';'
  DataTime today;

- 참조형 변수 초기화
  ex)클래스 형의 변수 초기화
  DataTime today = new DataTime(); // 클래스를 이용해서 객체를 만든 것

  ex2) String class
  => Strina a = "aaa"









- 요약
  \- 변수는 타입과 관련되어있으며,
  변수에는 오직 변수 타입에 해당되는 값만 저장할 수 있다.
  ex) int 형 변수는 오직 정수값만 저장할 수 있다.

  \- , 를 사용해 **하나 이상의 변수를 선언** 할 수 있다.

ex)

```
int a = 42, b = 11;
```

## 05. Primitive Operators

 

### 1. The Math Operator[ 수학연산자]



- 자바는 다양한 변수들을 다루기 위한
  많은 연산자(operator)들을 제공



ex)

- operand

: 연산자들의 앞, 뒤에 있는 것들

```
int x = 6 + 3; // 6 과 3 : plus operator의 operands
```

- arithmetic operator[산술연산자]

1 ) + : 더하기

2 ) - : 빼기

3 ) * : 곱하기

4) / : 나누기 - 몫만 받음

5) % : modulo -나머지만 받음



- 수학과 같이 한 줄의 코드에서 여러개의 연산자를 사용 가능

ex)

```
int val = 10 + 5 - 2;
```



## 06. Increment & Decrement operator



### 1. Increment operator(++) & Decrement operator(--)

- 변수의 값을 1씩 늘리거나 줄이는 효과적인 방법

ex)

```
int test = 5;
++test; // test is now 6

int test = 5;
--test; // test is now 4
```

\2. Prefix & Postfix

- 둘 다 Increment & Decrement operator 와 함께 쓰인다.

- prefix
  \- **operand 앞**에 연산자를 붙이는 것
  \- 그 변수의 값을 증가시키고, 새로운 값을 표현에서 사용

ex)

```
int a =  4;
int b = ++a; // a = b = 35
```

- 첫번째로 x의 값을 증가시키고, 이 값을 y에 배정,
  따라서 x 와 y 모두 35







- postfix
  \- **operand 뒤**에 연산자를 붙이는 것
  \- 그 변수의 **값을 먼저 표현에 사용**하고, 이후 그 값을 증가시키는 것

ex)

```
int a =  4;
int b = a++; // a=5, b=4
```

- 첫번째로 x의 값을 y에 배정하고, 이후 그 값을 증가시킨다.



- 같은 연산을
  **decrement** operator 에도 적용 가능



### 3. 대입 연산자(=)

- 변수에 값을 **대입**하는 역할

ex)

```
int value = 5;
```

- 자바는 코드를 좀 더 쉽게 짜기 위해

여러가지 대입연산자를 제공한다

- 더하고 대입하기(+=)

```
public class NHN11 {
    public static  void main(String[] args){
       int a =  4;
       int b = 10;
       System.out.println(b+=a); // b = b+a = 14
       System.out.println(a); // a = 4
       System.out.println(b); // b =14;
    }
}
```

- 빼고 대입(-=)

```
public class NHN11 {
    public static  void main(String[] args){
       int a =  4;
       int b = 10;
       System.out.println(b-=a); // b = b-a = 16
       System.out.println(a); // a = 4
       System.out.println(b); // b =16;
    }
```

- 위와 비슷하기 *=(곱하고 배정), /=(나누고 배정), %= 도 가능





### 07. String[문자열]

### 1. String

- 일련의 글자들을 나타내는 객체(object)

ex)

```
String a = "Hi" // 2글자로 이루어진 문자열
```

- **빈 문자열**을 선언할 수 있다.

```
String str = "";
```

### 2. String Concatenation[ 문자열 붙이기]



- 문자열들 사이의 +(plus) 연산자는 그 문자열들을 서로 결합하여
  하나의 새로운 문자열로 만들 수 있다.
  이러한 과정을 **Concatenation** 이라고 한다.
- 나오는 String 은 첫번째 String에 두번째 String이 붙어서 나온다.

ex)

```
public class NHN11 {
    public static  void main(String[] args){
        String a = "java는";
        String b = "재밌다.";
        System.out.println(a+" "+b);
    }
}
// 자바는 재밌다.
```





## 08. Getting User Input



### 1. Getting User Input[사용자 입력 받기]



- 자바는 수많은 Getting User Input을 위한 메소드들을 제공한다.



- 그 중 **Scanner class**는 가장 흔하고, 쉽게 행할 수 있는 객체이다.



- Scanner 클래스를 가져와서 Scanner 객체를 사용하기

```
import java.util.Scanner;
```

- Scanner 클래스를 사용하기 위해,
  다음 구문을 이용하여 Class 의 instance를 만든다.

```
Scanner sc = new Scanner(System.in);
```

- 이렇게 하면 사용자가 입력한 여러 종류의 입력 데이터를
  읽을 수 있다.
- Scanner class를 통하여 사용가능한 메소드들의 종류

1 )Read a byte - nextByte()

2 )Read a short - nextShort()

3 )Read an int- nextInt()

ex)

```
import java.util.Scanner;

class Nyahahaha{
   public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    int a = sc.nextInt();
   }
}
```

4 )Read a long - nextLong()

5 )Read afloat- nextFloat()

6 )Read a double - nextDouble()

7 )Read a boolean- nextBoolean()

8 )Read a **complete line** - nextLine()

ex)

```
import java.util.Scanner;

class MyClass{
    public static void main(String[] agrs){
    Scanner sc = new Scanner(System.in);
    System.out.println(sc.nextLine)
    String wow = sc.nextLine();

    }
}
```

9 )Read a **word** - next()







﻿