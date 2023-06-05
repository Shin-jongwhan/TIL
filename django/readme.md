# 230516
## 회사 웹 서버 구축 중
1. 웹 서버 생성
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/3343d6ed-59d1-4cf5-91dc-326264fa90a0)
2. app 생성 및 관리
3. mysql DB 여러 개 관리 방법(dbrouter)
- settings.py
  - app 추가
  - dbrouter
  - DATABASE 여러 개(mysql) 등록
4. admin - db 등록(여러 개일 경우)
5. db - html 출력 연결
### 간략한 스크린샷
- db 데이터를 html 에 출력한 결과
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/07bbbb83-b0ed-4983-903c-4250b5936be2)
- db 데이터 여러 개 연결하여 html 에 출력하기(첫 번째 행은 1 번 db 에서, 두 번째 행은 2 번 db 에서 값을 가져온 것)
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/544eee84-b3b5-4e64-8e58-fc51da26aaf3)
- db 가 여러 개일 경우, admin 페이지에 등록하는 방법 : dbrouter 구성, db 관리 app 생성
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/ef151e24-4721-4fb1-b205-075b4c1f7e53)
### <br/><br/><br/>

# 230520
## 로그인 / 회원가입 구현
### 구현한 것
1. 회원가입 / 로그인 페이지 틀 짜기
2. session 확인, session expiry time 구현 -> 끝나면 자동 로그아웃
3. 로그인되어 있는지, 안 되어 있는지 확인 -> 되어 있으면 로그인 페이지로 다시 가려고 하면 자동으로 홈으로 리다이렉션
### db 에 저장되어 있는 session 정보(django_session 테이블)와 웹에 저장되어 있는(F12 - network, application 에서 확인) session 정보가 일치하는지 확인함
### 회원가입(틀만 짜놓음)
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/1b9767cc-046d-4337-bbff-2390de4ed18d)
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/b008b432-31cc-4544-8484-1906f6dc5757)
### 회원가입 시 필요사항 알림창 출력
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/3f29afb7-e128-499b-a0e6-1dabb60f2af6)
### 로그인
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/3fba2316-2f02-4e8f-9f15-d5eec19a5800)
### 로그인 성공 시 리다이렉션
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/237dc4db-d9d2-4303-9921-123d1f87c5f3)
### <br/><br/><br/>

# 230522
## 로그인
### 로그인 안 되어 있을 때는 항상 login 페이지로 이동
- middleware 로 구현
### <br/><br/><br/>

# 230605
## 그 동안 한 것
1. 로그인 / 회원가입
- 에러메세지 출력
- 세션 유지 및 만료
- 로그인 중인지 체크
- 로그아웃
2. db 쿼리 및 데이터 파싱
- 특정 id 입력하면 그 id 에 맞는 쿼리를 제출하고 데이터를 파싱해서 가져오도록 함
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/ace5ca0e-61dc-486a-8cd3-1b3ed2bd4bf4)
3. middleware 구현
### <br/><br/><br/>
