# java-calculator-precourse: 문자열 덧셈 계산기

## 구현할 기능 목록
1. 쉼표(,) 콜론(:)으로 문자열 분리해서 숫자 추출해서 숫자 합 반환
2. 빈 문자열일시 0 반환
3. "//" "\n" 사이에 있는 값 커스텀 구분자로 이용, 기준으로 문자열 구분에서 합 반환
4. 구분자 사이에 양수 이외의 값 입력시(음수, 0, 문자 등) IllegalArgumentException 발생
5. 구분자 잘못 입력시 IllegalArgumentException 발생

---

## 기능 요구 사항
입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.

* 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환한다.
  * 예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6
* 앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
  * 예를 들어 "//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
* 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

## 입출력 요구 사항
### 입력
* 구분자와 양수로 구성된 문자열
### 출력
* 덧셈 결과


    결과 : 6
  

#### 실행 결과 예시

    
    덧셈할 문자열을 입력해 주세요.
    1,2:3
    결과 : 6

    
## 프로그래밍 요구 사항
* JDK 21 버전에서 실행 가능해야 한다.
* 프로그램 실행의 시작점은 Application의 main()이다.
* build.gradle 파일은 변경할 수 없으며, 제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.
* 프로그램 종료 시 System.exit()를 호출하지 않는다.
* 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다.
* 자바 코드 컨벤션을 지키면서 프로그래밍한다.
  * 기본적으로 Java Style Guide를 원칙으로 한다.

## 라이브러리
* camp.nextstep.edu.missionutils에서 제공하는 Console API를 사용하여 구현해야 한다.
* 사용자가 입력하는 값은 camp.nextstep.edu.missionutils.Console의 readLine()을 활용한다.