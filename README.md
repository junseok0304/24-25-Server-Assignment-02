# 23-24 Assignment template
# Description

- "QWER 헬스장"의 회원을 관리하는 컨셉의 서비스입니다.
- 헬스장 회원정보를 추가/조회/수정/삭제 할 수 있습니다. (CRUD)
- swagger를 적용하여 API명세에 대한 일부 자동화를 구현해보았습니다.

## API 명세
<img width="479" alt="스웨거_Api명세" src="https://github.com/user-attachments/assets/1fe1f221-da6d-49ca-8138-abc65deae57c">
<br>
<br>
<details> <summary>API 명세 자세히 보기 클릭 (글 버전)</summary>

### POST - /members : 새로운 회원을 생성하고, 저장합니다.

### RequestBody

```json
{
	  "id": 1,
    "name": "홍길동",
    "phoneNumber": "01012345678",
    "isEnrolled": true,
    "ptTeacherName": "김코치"
}
```

### Response

- **Status Code**: `201 Created`
- **Description**: -
- **Response Body**: 없음

---

## **GET - /members/{id} : 회원 정보를 ID로 조회합니다.**

### **Request**

- **Path Parameter**:
    - **id**: 회원의 고유 ID

### **Response**

- **Status Code**: `200 OK`
- **Description**: -

### **Response Body(JSON)**

```json
{
    "id": 1,
    "name": "홍길동",
    "phoneNumber": "01012345678",
    "isEnrolled": true,
    "ptTeacherName": "김코치"
}

```

---

## **DELETE - /members/{id} : 회원을 ID로 삭제합니다.**

### **Request**

- **Path Parameter**:
    - **id**: 회원의 고유 ID

### **Response**

- **Status Code**: `204 No Content`
- **Description**: -
- **Response Body**: 없음

---

## **PATCH - /members/{id} : 회원 정보를 수정합니다.**

### **Request**

- **Path Parameter**:
    - **id**: 회원의 고유 ID
- **Request Body(JSON)**:

```json
{
	  "id": 1,
    "name": "김완숙",
    "phoneNumber": "01012345678",
    "isEnrolled": true,
    "ptTeacherName": "백종원"
}
```

### **Response**

- **Status Code**: `200 OK`
- **Description**: -
- **Response Body**: 없음

---

## **GET - /members/list : 모든 회원 리스트를 조회합니다.**

### **Request**: 없음

### **Response**

- **Status Code**: `200 OK`
- **Description**: -

### **Response Body(JSON)**

```json
[
  {
    "id": 1,
    "name": "홍길동",
    "phoneNumber": "01012345678",
    "isEnrolled": true,
    "ptTeacherName": "김코치"
  },
  {
    "id": 2,
    "name": "쵸단",
    "phoneNumber": "01012345678",
    "isEnrolled": True,
    "ptTeacherName": "김계란"
  }
]

```

PUT -/members
GET - /members/{id}
DELETE - /members/{id}
PATCH - /members/{id}
GET(LIST) - /members/list

---
</details>
<br>

## Important content

- Swagger 의존성을 추가하여 postman이 없어도 자체적으로 테스트가 가능하도록 구성해봤습니다. (swagger 구현 사진)
- `MemoryMemberRepository` 코드에서, @Override를 사용해주지 않아도 동작하는데 그러면 오버라이드 구문을 삭제해도 될까요? 안된다면, 이유가 무엇인지 궁금합니다!
- API명세서 작성시에 코드상에서 구현한 설명이 없다면 -로 표기하는것이 일반적인가요?

## Question & Reference

- 질문은 important content에 같이 작성해두었습니다.!
<br>

참고문헌 : Swagger 커스터마이징, Swagger 사용법, Api 명세서 작성 가이드

[Swagger 커스터마이징](https://github.com/taehyeon3549/SwaggerCustomizing)  
[Swagger 사용법](https://velog.io/@nefertiri/Spring-Swagger-%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-API-%EB%AA%85%EC%84%B8%EC%84%9C-%EC%9E%91%EC%84%B1-%EC%9E%90%EB%8F%99%ED%99%94%ED%95%98%EA%B8%B0)  
[API 명세서 작성 가이드](https://velog.io/@nefertiri/API-%EB%AA%85%EC%84%B8%EC%84%9C-%EC%9E%91%EC%84%B1-%EA%B0%80%EC%9D%B4%EB%93%9C)
<br>
EOL
