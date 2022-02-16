# 1강. Java와 객체지향 프로그래밍

# Java 언어의 특징

- C와 C++언어와 유사하나 단순함
- 플랫폼에 독립적
- 완전한 객체지향 언어
- 웹 또는 네트워크 프로그래밍이 용이
- 엄격한 자료형의 검사
- 예외 처리 기능 제공
- 멀티 스레딩 지원

# Java 프로그램의 실행

- 바이트 코드는 엄격하게는 기계어가 아니어서 일반적인 운영체제에서는 실행할 수 없다. 대신 Java VM에서 실행된다.

![img](https://user-images.githubusercontent.com/43905552/154262241-f8a72fef-f6bc-4b8f-beb6-1d07b23934ca.png)

- Java 소스 프로그램의 확장자는 .java
- 바이트 코드
    - Java 소스를 컴파일한 결과물
    - 확장자는 .class이며 클래스 파일이라고도 함.
    - 자바 플랫폼의 Java VM에서 실행 가능한 코드

# 애플리케이션과 애플릿

- 애플리케이션
    - Java 플랫폼에서 실행되는 프로그램
    - 실행을 위해 main() 함수가 필요함
- 애플릿
    - HTML 웹 페이지에 포함되어 웹 브라우저를 통해 실행(요즘에는 익스플로러에서만 실행 가능)
      ![img](https://user-images.githubusercontent.com/43905552/154264452-fca61914-f2a5-4f90-9417-4d1d6415f770.png)

# Java 플랫폼

- 플랫폼
    - 프로그램의 실행을 위한 하드웨어와 소프트웨어 환경
    - Java 플랫폼은 Java 프로그램의 개발과 실행을 위한 환경
    - 운영체제에 맞는 Java 플랫폼을 설치해야 함

![img2](https://user-images.githubusercontent.com/43905552/154264528-a21608c0-a8c4-429c-96a5-b021d7619709.png)

# Java 플랫폼의 구성

- Java VM
    - 자바 프로그램의 실행 환경을 제공하는 가상 기계
    - 자바 프로그램의 구동 엔진
    - 실행에 필요한 사항을 관리
    - 메모리 정리를 자동으로 수행

![img3](https://user-images.githubusercontent.com/43905552/154264594-e881fdec-4dca-43a0-bff2-e4c9cd8da520.png)

- Java API
    - 프로그램의 개발에 필요한 클래스 라이브러리
    - 패키지(클래스 묶음)들이 계층 구조로 분류되어 있음.

# JDK의 설치

- 자바 홈페이지에서 다운로드 받아 설치
- 환경변수 PATH를 수정
- 환경변수 JAVA_HOME을 생성

# Java 애플리케이션

- 대소문자를 구분한다.
- 주석, public class, main() 메소드, 출력문

![img](https://user-images.githubusercontent.com/43905552/154266452-71aa15b9-b3f8-4bcd-b3f9-2c407fa08ebf.png)