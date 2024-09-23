# Everylearn_Readme_only
Everylearn 프로젝트 1차 개발을 위해 임시로 설치한 서버

# backend
Temporary REST API Backend Server

| Developers|||
| :------------: | :------------: | :------------: |
| 배현철  | 김시우  | 백진욱 |
| DevOps  | 학원, MyPage | Member, 견적

#### Dev Schedule
2024.09.04. ~ 2024.09.20.

#### Dev Environemnts
Server: Spring Boot (Gradle, Java) -> AWS EC2   
Database: MySQL -> AWS RDS   

------------
#### Features
1. Member : 회원가입, 로그인, 회원탈퇴, 아이디/비밀번호 찾기
2. MyPage : 찜 목록, 리뷰 목록, 최근 본 학원 목록
3. 학원 : 학원 검색, 정렬, 단일 조회, 찜하기 지정/해제, 학원 분류 조회
4. 견적 : 목록/상세 조회

#### Directory Tree
```bash
├─main
│  ├─java
│  │  └─com
│  │      └─example
│  │          └─demo
│  │              ├─domain
│  │              │  ├─esimate
│  │              │  │  ├─controller
│  │              │  │  ├─dto
│  │              │  │  │  ├─request
│  │              │  │  │  └─response
│  │              │  │  ├─entity
│  │              │  │  │  └─enums
│  │              │  │  ├─repository
│  │              │  │  ├─service
│  │              │  │  │  └─impl
│  │              │  │  └─utils
│  │              │  ├─hakwon
│  │              │  │  ├─controller
│  │              │  │  ├─dto
│  │              │  │  │  ├─request
│  │              │  │  │  └─response
│  │              │  │  ├─entity
│  │              │  │  │  ├─category
│  │              │  │  │  └─enums
│  │              │  │  ├─repository
│  │              │  │  │  └─impl
│  │              │  │  ├─service
│  │              │  │  │  └─impl
│  │              │  │  └─utils
│  │              │  └─member
│  │              │      ├─controller
│  │              │      ├─dto
│  │              │      │  ├─request
│  │              │      │  └─response
│  │              │      ├─entity
│  │              │      │  └─enums
│  │              │      ├─repository
│  │              │      ├─service
│  │              │      │  └─impl
│  │              │      └─utils
│  │              └─global
│  │                  ├─base
│  │                  ├─config
│  │                  │  ├─jwt
│  │                  │  └─util
│  │                  ├─exception
│  │                  └─response
│  └─resources
└─test
    └─java
        └─com
            └─example
                └─demo
```
