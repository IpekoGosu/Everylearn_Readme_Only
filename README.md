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
|-- java
|   `-- com
|       `-- example
|           `-- demo
|               |-- DemoApplication.java
|               |-- domain
|               |   |-- esimate
|               |   |   |-- controller
|               |   |   |   `-- EstimateController.java
|               |   |   |-- dto
|               |   |   |   |-- request
|               |   |   |   |   |-- CreateEstimateDto.java
|               |   |   |   |   `-- CreateEstimateRequestDto.java
|               |   |   |   `-- response
|               |   |   |       |-- EstimateInfoResponseDto.java
|               |   |   |       `-- EstimateResponseDto.java
|               |   |   |-- entity
|               |   |   |   |-- Estimate.java
|               |   |   |   |-- EstimateHakwon.java
|               |   |   |   |-- EstimateInfo.java
|               |   |   |   `-- enums
|               |   |   |       |-- DayOfWeek.java
|               |   |   |       |-- Status.java
|               |   |   |       `-- TimeZone.java
|               |   |   |-- repository
|               |   |   |   |-- EstimateHakwonRepository.java
|               |   |   |   |-- EstimateInfoRepository.java
|               |   |   |   `-- EstimateRepository.java
|               |   |   |-- service
|               |   |   |   |-- EstimateService.java
|               |   |   |   `-- impl
|               |   |   |       `-- EstimateServiceImpl.java
|               |   |   `-- utils
|               |   |       `-- EstimateMapper.java
|               |   |-- hakwon
|               |   |   |-- controller
|               |   |   |   `-- HakwonController.java
|               |   |   |-- dto
|               |   |   |   |-- HakwonInfoDto.java
|               |   |   |   |-- HakwonListDto.java
|               |   |   |   |-- HakwonRequestDto.java
|               |   |   |   `-- HakwonSearchResponseDto.java
|               |   |   |-- entity
|               |   |   |   |-- Hakwon.java
|               |   |   |   |-- HakwonTypeEnum.java
|               |   |   |   |-- Like.java
|               |   |   |   |-- Review.java
|               |   |   |   `-- Teacher.java
|               |   |   |-- repository
|               |   |   |   |-- HakwonRepository.java
|               |   |   |   |-- LikeRepository.java
|               |   |   |   |-- ReviewRepository.java
|               |   |   |   `-- impl
|               |   |   |       |-- HakwonRepositoryImpl.java
|               |   |   |       |-- HakwonRepositoryJpa.java
|               |   |   |       |-- LikeRepositoryImpl.java
|               |   |   |       |-- LikeRepositoryJpa.java
|               |   |   |       |-- ReviewRepositoryImpl.java
|               |   |   |       `-- ReviewRepositoryJpa.java
|               |   |   |-- service
|               |   |   |   |-- HakwonService.java
|               |   |   |   `-- impl
|               |   |   |       `-- HakwonServiceImpl.java
|               |   |   `-- utils
|               |   |       `-- HakwonMapper.java
|               |   `-- member
|               |       |-- controller
|               |       |   `-- MemberController.java
|               |       |-- dto
|               |       |   |-- request
|               |       |   |   |-- FindIdRequestDto.java
|               |       |   |   |-- LoginRequestDto.java
|               |       |   |   |-- ResetPwRequestDto.java
|               |       |   |   `-- SignUpRequestDto.java
|               |       |   `-- response
|               |       |       |-- LoginResponseDto.java
|               |       |       `-- SignUpResponseDto.java
|               |       |-- entity
|               |       |   |-- Member.java
|               |       |   `-- enums
|               |       |       `-- Gender.java
|               |       |-- repository
|               |       |   `-- MemberRepository.java
|               |       |-- service
|               |       |   |-- CustomUserDetailsService.java
|               |       |   |-- MemberService.java
|               |       |   `-- impl
|               |       |       `-- MemberServiceImpl.java
|               |       `-- utils
|               |           `-- MemberMapper.java
|               `-- global
|                   |-- base
|                   |   `-- BaseTimeEntity.java
|                   |-- config
|                   |   |-- SecurityConfig.java
|                   |   |-- SwaggerConfig.java
|                   |   |-- WebMVCConfig.java
|                   |   |-- jwt
|                   |   |   |-- JwtAuthenticationFilter.java
|                   |   |   `-- JwtToken.java
|                   |   `-- util
|                   |       `-- JwtTokenProvider.java
|                   |-- exception
|                   |   |-- CustomException.java
|                   |   |-- ErrorCode.java
|                   |   `-- GlobalExceptionHandler.java
|                   `-- response
|                       `-- ResponseDto.java
`-- resources
    `-- application.yml
```
