# 👕Laundrygo Project
> ### '우리집 모바일 세탁소, 런드리고'의 웹사이트 버전
> SpringMVC, MyBatis를 기반으로 제작한 세탁 서비스 웹사이트<br>
> 어플 사용이 어려울 때, 웹사이트로도 이용가능 하도록 하여 사용자의 불편함을 해소하는 프로젝트

<br><br>

# 👕제작기간 및 참여인원
### FrontEnd
> 2022-08-07 ~ 2022-08-21
### BackEnd
> 2022-09-18 ~ 2022-10-04
### 참여인원
> 팀 프로젝트 (총 4명)

<br><br>

# 👕사용기술
### FrontEnd
<img src="https://img.shields.io/badge/HTML5-black?style=for-the-badge&logo=HTML5&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/CSS3-black?style=for-the-badge&logo=CSS#&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/JavaScript-black?style=for-the-badge&logo=JavaScript&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/JQuery-black?style=for-the-badge&logo=JQuery&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/Ajax-black?style=for-the-badge&logo=Ajax&logoColor=white">
<br>

### BackEnd
<img src="https://img.shields.io/badge/Java11-black?style=for-the-badge&logo=Java11&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/Spring MVC-black?style=for-the-badge&logo=Spring&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/ApacheTomcat 9.0-black?style=for-the-badge&logo=Apache Tomcat&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/JSTL-black?style=for-the-badge&logo=JSTL&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/MyBatis-black?style=for-the-badge&logo=MyBatis&logoColor=white">

<br><br>

# 👕개발환경
### Tools
<img src="https://img.shields.io/badge/IntelliJ IDEA-black?style=for-the-badge&logo=IntelliJ IDEA&logoColor=white">&nbsp;
<img src="https://img.shields.io/badge/MySQL-black?style=for-the-badge&logo=MySQL#&logoColor=white">
<br>

### DBMS
<img src="https://img.shields.io/badge/MySQL-black?style=for-the-badge&logo=MySQL#&logoColor=white">&nbsp;
<br>

### Languages
<img src="https://img.shields.io/badge/Java11-black?style=for-the-badge&logo=Java11&logoColor=white">&nbsp;<img 
src="https://img.shields.io/badge/JavaScript-black?style=for-the-badge&logo=JavaScript&logoColor=white">
<br>

### 협업 툴
<img src="https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=GitHub&logoColor=white">

## 7. 트러블 슈팅

### 1:1 문의 이미지 등록 시 이미지 저장 및 받아오는 기능
![image](https://user-images.githubusercontent.com/101616249/193774595-11da1b69-d7bd-4c22-be8a-80b56fbaac45.png)
![image](https://user-images.githubusercontent.com/101616249/193775107-ab35c01a-7752-44ef-9149-232e9984b9b3.png)

- 이미지를 임의의 컴퓨터 경로에 저장
- 랜덤한 uuid와 이미지 저장 경로를 cs, cs_img 테이블에 저장
- 게시판에서는 각 문의가 고유한 uuid로 저장되고, 해당 문의의 uuid와 일치하는 이미지 경로를 테이블에서 받아와 이미지를 띄운다. </br></br>

### 특정 기능 수행 후 페이지 URL 변경으로 인해 타 기능들이 수행되지 않는 문제
![image](https://user-images.githubusercontent.com/101616249/193775314-ced872dd-7faf-409d-9861-fd3f06178541.png)

- id 찾기 기능을 예시로, id 찾기 수행시 메인페이지에서 Request url인 "/findId" 로 url이 변경된다.
- 이때, 기본적인 로그인 및 여러 페이지로의 이동이 불가능하게 됨
- 따라서 메서드의 return문을 "redirect:" + uri 로 설정하여 이전페이지의 url로 기능을 수행하여 값을 받아온다. </br></br>

### 프로젝트 진행과정의 분업과 효율성에 대한 고민
- 네 명의 인원이 각각의 파트를 맡아 개발을 진행하였을 때, 서로의 개발 코드에 대한 이해도가 떨어질 수 있다는 문제점이 있다.
- 반대로 네 명의 인원이 함께 모든 파트를 구현하기에는 시간적으로 효율성이 떨어진다는 판단을 하였다.
- 따라서 프로젝트 파트를 두개로 나눠 함께 구현함으로써 효율성과 원활한 개발코드 공유를 도모하였다. </br></br>

### 지속적인 DB의 수정 및 FK값 설정 문제
- 프로젝트를 진행함에 있어 추가되거나 삭제되는 DB가 존재하였다.
- 해당 DB와 관련된 controller 개발을 중심으로 이외의 기능들까지 고려하여 DB 추가 또는 삭제, 수정을 진행하였다.
- FK값에 따라 회원정보 삭제, 월정액 구매내역 삭제 등 기능이 수행되지 않는 현상이 발생하였다.
- 논의를 거쳐 불필요한 FK값을 삭제하거나, CASCADE 및 RESTRICT 옵션을 설정하여 원활한 기능 구현을 성공하였다. </br></br>

### ID 찾기 기능에서 한 명이 두 개의 이메일을 보유하고 있는 상황에 대한 처리
![image](https://user-images.githubusercontent.com/101616249/193777977-52f6442b-4fff-401a-a6ab-e0562c3c5361.png)
![image](https://user-images.githubusercontent.com/101616249/193778096-78e40b41-64c2-4afc-9a3b-cd959a4d6b55.png)

- 동일한 이름, 동일한 전화번호로 회원가입을 두 번 이상 진행하였을 때, UserDao 부분에서 "selectOne" 함수에 오류가 발생하였다.
- 해당 현상을 대처하기 위해 UserDao 부분에서 "selectList" 함수로 수정하였고, List로 받아온 값들의 email 부분만 StringBuilder로 설정하여 기능을 진행하였다. </br></br>

### HttpSession에 저장할 값에 대한 고민
- 기능 구현 초반, 로그인 시 User 객체 전체를 session에 저장하여 보다 편리하게 개발을 진행하려고 하였다.
- 이 때, 회원정보가 수정되었을 때 User 객체의 특정 값들을 변경하였을 때, session을 수정해야하는 문제점과
- session 객체에 여러 데이터들이 담겨 무거워지는 문제점이 발생하였다.
- 따라서, session에는 변하지 않는 값인 email만 담아 세션의 무게를 최소화 하였으며, Controller에서 필요로 하는 데이터들을 DB에서 받아와 개발을 진행하였다. </br></br>

### 월정액 기간이 만료되었을 때 처리되는 로직 구현
![image](https://user-images.githubusercontent.com/101616249/193779038-ab1a0ceb-3b04-4f31-88c0-6d2404cb9dab.png)

- 메인페이지가 로드될 때 일괄적으로 기간이 만료된 월정액을 파악한 후, 처리를 진행하였다.
- 월정액 기간이 종료되었을 때, 사용자가 설정한 월정액의 유지 또는 해지 상황을 기반으로 처리하였다.
- 월정액을 유지하였을 때, 동일한 월정액의 기간을 재설정하고, 추가 금액을 0으로 만든 후 결제내역에 기존 월정액 금액 + 추가금액 만큼을 insert 하였다.
- 마찬가지로 잔여 생활빨래, 개별클리닝, 무료수거의 갯수를 월정액 초기 횟수로 재설정 하였다.
- 월정액을 해지하였을 때, 해당 월정액을 DB에서 삭제하고, 추가금액 만큼을 결제내역에 insert 하였다.

---
