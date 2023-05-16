# 230516
## 회사 웹 서버 구축
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
