---
title: "04. Conditionals and Loops(2)"
category: "sololearn"
tags: 
- Java
- Sololearn
- Grammar
---

﻿

## 06. While Loops



### 1. while Loops



- loop문은 하나 또는 그 이상의 문들을
  반복적으로 실행하게 하는 기능을 한다.



- while loop문은 **주어진 조건이 참**일 경우
  목표 문을 **반복적으로 실행**한다.

ex)

```
import java.util.Scanner;

public class Sololearn {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int testCase = sc.nextInt();
        int c = 1;
        while(c<=testCase){
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println(a+b);
            c++
        }
    }
}
```

- while문은 **조건이 참**일 경우,
   그것의 body안에 있는 문을 실행한다.
  이후 조건문을 다시 확인하고, 반복한다.



- 조건문의 결과값이 false 일 때,
  loop body는 스킵되고, while문 이후의 첫번째 문이 실행된다.

ex)

```
import java.util.Scanner;

public class Sololearn {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int testCase = sc.nextInt();
        int c = 1;
        while(c<=testCase){
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println(a+b);
            c++;
        }
        System.out.println("While문 실행 완료");
    }
}
```

- 위의 마지막 출력 method가 while 문 바깥에 있는 것을 주목.



## 07. For Loops



### 1. for Loops



- for loop
  \- 또 다른 loop구조
  \- 특정 횟수만큼 실행하는 loop를 효율적으로 작성이 가능하다.
- for loop 구조

```
for(initialization; condition; increment/decrement){
  statement(s)
}
```

1) initialization
: 루프가 시작되는 동안 처음 한번만 실행됨

2) condition

- 루프가 반복될때마다 평가됨

- 조건이 false를 return할 때까지, for loop는 명령문을 반복적으로 실행한다.

3) Increment/Decrement

- 루프가 반복될때마다 실행



ex) for 구문의 예시- 구구단

```
import java.util.Scanner;

public class Sololearn {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i=1; i<=n; i++){
           System.out.println(n + "*"+ i + "=" + n*i);
        }
    }
}
```

- 주의
  : ';' 이 구문 내 initialization 과 condition 뒤에 붙는다.
- for loop에서,
  **모든 타입의 조건**과,  **모든 타입의 increment statements 문**을 가질 수 있다.

```
import java.util.Scanner;

public class Sololearn {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int x = sc.nextInt();
        int[] t = new int[n];
        for(int i=0; i<n; i++){
           t[i] = sc.nextInt();
           if(t[i]<x){
               System.out.print(t[i]+" ");
           }
        }
    }
}
```

- for loop문은 시작과 끝 숫자를 알 때 최고의 방법이다.





## 08. do while Loops



### 1. do.....while Loops



- do.. while loop는 while loop 와 비슷하지만,
  **최소 한번은 실행**한다는 점에서 차이가 있다.

ex)

```
public class Sololearn {
    public static void main(String[] args){
        int x = 1;
        do{
            System.out.println(x);
            x++;
        }while(x<0);
    }
}
```

ex2)

```
public class HelloWorld {
    public static void main(String[] args){
        int i =0;
        do{
            if(i==0){
                System.out.println("do-while문을 시작합니다.");
            }else{
                System.out.println(i);
            }
            i++;
            if(i==10){
                break;
            }
        }while (i>0);
    }
}
/*
시작합니다.
1
2
3
4
5
6
7
8
9

*/
```

ex3)

```
public class Sololearn {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a;
        int b;
        int c;
        do{
            a = sc.nextInt();
            b = sc.nextInt();
            c = sc.nextInt();
        }while(a>100||b>100||c>100);
        System.out.println("아무도 100점을 못넘었어");
    }
}
// 입력 90 60 30 
// 출력 "아무도 100점을 못넘었어"
```

- **루프 끝에 조건**이 나타나는 것을 주의,
  그렇기 때문에, loop문 안의 구문은 검증 전 최소 한번은 실행된다.
  -> 비록 조건이 falseㄹ도, 최소 한번은 실행된다.
- 주의할 점
  \- do...while 문에서, **while은 단지 조건일 뿐이고, 그것의 몸체 자체는 없다.**



### 2. Loop Control Statement

- break문과 continue 문은 loop의 실행 흐름을 변화시킨다.
- **break 문은 loop를 종료**하고,
  **루프 바로 다음에 있는 문으로 실행을 전송**

ex)

```
public class Sololearn {
    public static void main(String[] args){
        int x =1;
        while(x>0){
            if(x==4){
                break;
            }
            System.out.println(x);
            x++;
        }
        System.out.println("while문을 종료합니다.")
    }
}
```



```
public class Sololearn {
    public static void main(String[] args){
        int x =1;
        while(x>0){
            if(x>100){
                break;
            }
            System.out.println(x);
            x *= 2;
        }
        System.out.println("while문을 종료합니다.")
    }
}
```



- continue 문은 루프가 **continue 이후의 본문을 건너뛰고,**
  **즉시, 조건문의 조건을 다시 테스트**하게 함

ex)

```
public class Sololearn {
    public static void main(String[] args){
        int x =1;
        while(x<100){
            x++;
            if(x%2==0){
                continue;
            }
            System.out.println(x);
        }
    }
}
```



﻿
