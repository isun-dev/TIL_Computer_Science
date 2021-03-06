# 배열

- 같은 자료형의 원소를 정해진 개수만큼 가지고 있는 객체
- 배열의 크기는 배열이 초기화 또는 생성될 때 정해짐
- 숫자 인덱스를 사용하여 특정 원소를 다룸

## 배열의 선언

- 선언할 때는 크기를 지정할 수 없음
- 형식은 자료형[] 변수이름; 또는 자료형 변수이름[];
- 아래의 방법을 모두 사용할 수는 있지만 보통 자료형에 붙이는 것을 추천함
    - int[] a; int b[];
    - int[][] a; int b[][]; int[] e[]
    - int f[10] // 오류가 난다.

## 배열의 초기화

- 선언과 동시에 중괄호를 이용하여 초기값을 지정
    - 자동으로 메모리 공간이 확보됨
    - 초기화 또는 생성 과정을 거쳐야 배열의 원소를 사용할 수 있음
    - int[] a= {2,3,4,5}; // 선언과 동시에 초기화
    - int[][] anArray = {{1,2,3},{4,5,6}}; // 초기화를 할 수 있음

## 배열의 생성

### 배열의 원소가 사용할 메모리 공간의 생성

- new 연산자를 이용
    - 배열의 크기를 정하고 메모리 공간을 확보
    - new 연산자는 메모리의 주소값을 리턴함.
    - 원소가 숫자인 경우 0, 참조형인 경우 null로 자동 초기화.
    - int a[] = new int[3];
    - int b[]; b=new int[10];
    - int anArray4[][] = new int[3][2];

## 배열이 크기

- 배열이름.length
- 2차원 배열일 때
    - 행: 배열이름.length
    - 열: 배열이름[].length
# 문자열

## String 클래스

- String 클래스는 문자열을 표현하고 처리하기 위한 참조형
- String 형의 변수는 참조형이거나 기본형 변수처럼 사용할 수 있음 ⇒ 원래라면 new로 생성해주어야 하는데.

### 문자열 리터럴

- 이중 따옴표를 사용함
    - String aaa = “Java”;
- 참조형 변수에는 null이라는 특별한 값을 지정할 수 있다.
    - if(s1 != null) {…}

## 문자열의 + 연산자

- 두 문자열을 연결하는 것
- (문자열 + 기본형) or (문자열 + 다른 참조형)도 가능

# Scanner 클래스

- 키보드나 파일로부터 다양한 자료를 입력받을 때 사용
    - 기본적으로 공백 문자로 구분되는 단어 단위로 입력됨
    - 문자열이나 기본형 값의 입력을 위해 next XXX() 메소드를 제공함
- 키보드에서 입력을 받는 Scanner 객체
    - System.in을 이용하여 Scanner 객체를 만들고 사용함
    - Scanner sc = new Scanner(System.in);
- Scanner 클래스의 입력용 메소드
    - boolean hasNext() → 다음 단어가 있으면 true를 반환
    - String next() → 단어를 읽어 String으로 반환
    - boolean hasNextInt(), int nextInt()
    - boolean hasNextDouble(), double nextDouble()
    - boolean hasNextLine(), String nextLine()
    
    ```java
    import java.util.Scanner;
    class HelloWorld {
        public static void main(String[] args) {
           Scanner sc = new Scanner(System.in);
           // 123 hello 입력하고 엔터를 누르게 되면,
           // 123은 int 니까 true를 출력하고
           // hello String이니까 false를 출력한다.
           while(sc.hasNextInt()){
               System.out.println(sc.nextInt());
           }
        }
    }
    ```
    

# 클래스 정의
- 데이터 필드와 메소드를 정의
    - 객체가 가지는 인스턴스 변수(반드시 객체가 생성되고 나서 만들어지는 것, 객체가 없다면 사용할 수 없다)와 인스턴스 메소드
    - 클래스가 가지는 클래스 변수와 클래스 메소드
- 객체의 상태는 데이터 필드로, 행위는 메소드로 구현됨.
- 메소드는 저장된 데이터를 이용해 기능을 수행.
- 클래스의 사용
    - 클래스형 변수를 선언할 때(클래스는 객체의 자료형)
    - 객체를 생성할 때
    - 상속받아 클래스를 정의할 때

## 클래스 접근제어자

- 클래스를 사용할수 있는 범위를 제한 하는 것
- private와 protected는 특별한 경우에만 사용함
- 접근제어자가 생략된 경우와 public class
    - 클래스 선언에서 접근 제어자가 생략된 class
        - 같은 패키지에 있는 다른 클래스에서 사용 가능(패키지 접근 수준)
    - public class로 선언된 경우
        - 모든 클래스에서 즉, 어디서나 사용가능 하다.

## `데이터 필드 접근 제어자`

- 클래스 정의에서 데이터 필드나 메소드를 정의할 때도 접근 제어자를 사용함
    - 데이터 필드를 사용할 수 있는 범위를 제한하는 것(정보 은닉)
    - 메소드의 접근 제어자도 의미가 같음
- 데이터 필드 접근 제어자의 의미
    - private 필드는 같은 클래스에서만 사용 가능
    - 접근 제어자가 생략된 필드는 같은 패키지에 있는 다른 클래스에서 사용 가능
    - protected 필드는 같은 패키지와 자식 클래스에서 사용 가능
    - public 필드는 모든 클래스에서 사용 가능
