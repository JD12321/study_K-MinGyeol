### 1. JSP 스크립트 태그의 종류를 기술하시오.
| 내장 객체   | 설명                                                                                                       |
|-------------|------------------------------------------------------------------------------------------------------------|
| request     | 클라이언트가 서버에게 전송하는 관련 정보를 처리하기 위한 객체이다.                                         |
| response    | 서버가 클라이언트에게 요청에 대한 응답을 보내기 위한 객체이다.                                             |
| session     | 클라이언트마다 세션 정보를 저장 및 유지 관리하기 위한 객체이다.                                            |
| out         | JSP 페이지의 출력을 위한 객체이다.                                                                         |
| pageContext | JSP 페이지에 관한 정보와 다른 페이지로 제어권을 넘겨줄 때 사용되는 객체이다.                               |
| config      | 서블릿이 초기화 되는 동안 JSP 컨테이너가 환경 정보를 서블릿으로 전달할 때 사용하는 객체이다.               |
| application | 웹 애플리케이션에서 유지 관리되는 여러 환경 정보를 관리하는 객체이다.                                      |
| page        | JSP 페이지 자체를 나타내는 객체이다.                                                                       |
| exception   | 페이지 지시자에서 isErrorPage를 true로 한 경우에만 사용이 가능하며, 적절한 예외 처리 구현을 위한 객체이다. |
<br>

### 2. JSP 표현식을 이용하여 다음과 같이 본인의 이름과 학번을 출력하는 JSP 프로그램을 작성하시오.
```jsp
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>JSP 예제</title>
</head>
<body>
    이름: <%= "홍길동" %><br>
    학번: <%= 20103056 %>
</body>
</html>
```
<br>

### 3. 다음 프로그램의 실행 결과를 쓰시오.
```html
s1 = 지역변수
this.s1 = 소속변수
```
<br>

### 4. 다음 소스에서 오류를 수정하여 실행하시오.
```jsp
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>JSP 예제 ex04.jsp</title>
</head>
<body>
    원주율은 <%= Math.PI %> 이다.
</body>
</html>
```
<br>

### 5. 다음 프로그램의 실행 결과를 쓰시오.
```html
[2*1 = 2] [2*2 = 4] [2*3 = 6] [2*4 = 8] [2*5 = 10] [2*6 = 12] [2*7 = 14] [2*8 = 16] [2*9 = 18]
[3*1 = 3] [3*2 = 6] [3*3 = 9] [3*4 = 12] [3*5 = 15] [3*6 = 18] [3*7 = 21] [3*8 = 24] [3*9 = 27]
[4*1 = 4] [4*2 = 8] [4*3 = 12] [4*4 = 16] [4*5 = 20] [4*6 = 24] [4*7 = 28] [4*8 = 32] [4*9 = 36]
[5*1 = 5] [5*2 = 10] [5*3 = 15] [5*4 = 20] [5*5 = 25] [5*6 = 30] [5*7 = 35] [5*8 = 40] [5*9 = 45]
[6*1 = 6] [6*2 = 12] [6*3 = 18] [6*4 = 24] [6*5 = 30] [6*6 = 36] [6*7 = 42] [6*8 = 48] [6*9 = 54]
[7*1 = 7] [7*2 = 14] [7*3 = 21] [7*4 = 28] [7*5 = 35] [7*6 = 42] [7*7 = 49] [7*8 = 56] [7*9 = 63]
[8*1 = 8] [8*2 = 16] [8*3 = 24] [8*4 = 32] [8*5 = 40] [8*6 = 48] [8*7 = 56] [8*8 = 64] [8*9 = 72]
[9*1 = 9] [9*2 = 18] [9*3 = 27] [9*4 = 36] [9*5 = 45] [9*6 = 54] [9*7 = 63] [9*8 = 72] [9*9 = 81]
```
<br>

### 6. for 문장을 이용하여 다음과 같이 1부터 100까지의 합이 출력되도록 JSP 프로그램을 작성하시오.
```jsp
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>JSP 예제 ex06.jsp</title>
</head>
<body>
    <%
        int sum = 0;

        for (int i = 1; i < 101; i++) {
            sum += i;
        }
    %>

    1부터 100까지의 합은  <%= sum %>이다.
</body>
</html>
```