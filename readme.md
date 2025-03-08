# 테이블 설계
![table](https://github-production-user-asset-6210df.s3.amazonaws.com/29498316/419897083-ee882b49-062d-4027-a793-e68be8d1808f.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250306%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250306T115702Z&X-Amz-Expires=300&X-Amz-Signature=20d2cf501fa1fd7abdb71ccbb28ca0410f5b5d7ffcce7584d1defdf19b58fce6&X-Amz-SignedHeaders=host)

# API 설계
## 1) 가계부 작성
### 요청
- 타입 : POST
- URL : /account
- body
```json
{
  "user_idx": 1,
  "detail": "맥도날드",
  "type": "지출",
  "price": 3000,
  "date": "2025-03-09 21:43:12"
}
```
### 응답
- 상태코드 : 200
```json
{
  "status": "OK"
}
```

## 2) 가계부 목록
### 요청
- 타입 : GET
- URL : /account?page=10
- body : 없음
### 응답
``` json
{
    data: [
        {
            "id": 1,
            "detail": "맥도날드",
            "type": "지출",
            "price": 3000,
        },
        {
            "id": 2,
            "detail": "무신사",
            "type": "지출",
            "price": 10000,
        },
        {
            "id": 3,
            "detail": "아르바이트",
            "type": "수입",
            "price": 10000,
        },
    ]
}
```
