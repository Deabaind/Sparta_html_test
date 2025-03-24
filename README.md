# test 
sparta_foodfighter.html = 5주차 과제
ff.html = 과제를 보고 처음부터 만들어보는 파일
sparta_food_fighter.png = 목표(과제) 사진
[Calendar API 명세서, ERD 1c0f7369191680129ec6e609669300b4.md](https://github.com/user-attachments/files/19429406/Calendar.API.ERD.1c0f7369191680129ec6e609669300b4.md)

# Calendar API 명세서, ERD

| 기능 | Method | URL | request | response | 상태코드 |
| --- | --- | --- | --- | --- | --- |
| 일정 등록 | POST | /schedules | 요청 body
{
  “user” : {
    “name” : ”작성자”
  },
  “schedule” : {
    “title” : “일정명”,
    “contents” : “일정 내용”,
    “start_date” : “일정 시작일”,
    “last_date” : 일정 종료일”
  }
} | 등록 정보
{
  “schedule” : {
    “schedule_Id” : “일정 번호”
  }
} | 200: 정상 등록 |
| 일정 목록 조회 | GET | /schedules | 요청 param | 다건 응답 정보 | 200: 정상 조회 |
| 일정 조회 | GET | /schedules/{schedulesid} | 요청 param | 단건 응답 정보
{
  “schedule” : {
    “title” : “일정명”,
    “contents” : “일정 내용”,
    “start_date” : “일정 시작일”,
    “last_date” : 일정 종료일”
  }
} | 200: 정상 조회 |
| 일정 수정 | PUT | /schedules/{schedulesid} | 요청 body
{
  “user” : {
    “name” : ”작성자”,
    “password” : “비밀번호”
  },
  “schedule” : {
    “title” : “일정명”,
    “contents” : “일정 내용”,
    “start_date” : “일정 시작일”,
    “last_date” : 일정 종료일”
  }
} | 수정 정보
{
  “schedule” : {
    “title” : “일정명”,
    “contents” : “일정 내용”,
    “start_date” : “일정 시작일”,
    “last_date” : 일정 종료일”
  }
} | 200: 정상 수정 |
| 일정 삭제 | DELETE | /schedules/{schedulesid} | 요청 param | - | 200: 정상 삭제 |

![Blank diagram (3).png](Blank_diagram_(3).png)
