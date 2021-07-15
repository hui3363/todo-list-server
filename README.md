# todo-list-server
Todo List Server API  
  
- Framework : Spring Boot   
- IDE : IntelliJ  
  

## 필요 기능

**1. todo 리스트 목록에 아이템을 추가**  (**POST**)  
- endpoint : /  
- 기능 : todo 아이템 추가  
  
- request : 
{
"title": "자료구조 공부하기",
}  
  
- response : 
{
"id": 17,
"title": "자료구조 공부하기",
"order": 0,
"completed": false,
"url": "http://localhost:8080/17"
}  
  
---


**2. todo 리스트 목록 중 특정 아이템을 조회**  (**GET**)  
- endpoint : /  
- 기능 : 전체 todo 리스트 조회  
  
- response :   
[
{
"id": 1,
"title": "자바 기초 공부하기",
"order": 0,
"completed": false,
"url": "http://localhost:8080/1"
},
{
"id": 2,
"title": "알고리즘 공부하기",
"order": 0,
"completed": false,
"url": "http://localhost:8080/2"
}, ...
]  

---


**3. todo 리스트 전체 목록을 조회**  (**GET**)  
- endpoint : /{:id}  
- 기능 : todo 아이템 조회  
  
- response :   
{
"id": 17,
"title": "자료구조 공부하기",
"order": 0,
"completed": false,
"url": "http://localhost:8080/17"
}  

---


**4. todo 리스트 목록 중 특정 아이템을 수정**  (**PATCH**)  
- endpoint : /{:id}  
- 기능 : todo 아이템 수정  
  
- request :   
{
"title": "반복문 공부하기"
}
  
- response :   
{
"id": 1,
"title": "반복문 공부하기",
"order": 0,
"completed": false,
"url": "http://localhost:8080/1"
}  
  
---
  

**5. todo 리스트 목록 중 특정 아이템을 삭제**  (**DELETE**)  
- endpoint : /  
- 기능 : 전체 todo 리스트 삭제  
  
- response :  200  
  
---

**6. todo 리스트 전체 목록을 삭제**  (**DELETE**)  
- endpoint : /{:id}  
- 기능 : todo 아이템 삭제  
  
- response : 200  

---
