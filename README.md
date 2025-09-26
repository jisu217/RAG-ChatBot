# Spring AI Tutorial

Spring AI를 활용하여 LLM 호출부터 RAG 파이프라인 구축, Storm OpenAPI 연동까지 단계별로 학습할 수 있는 실습 프로젝트입니다.


**언어**: Kotlin  
**프레임워크**: Spring Boot 3.4.4        
**Spring AI 버전**: `1.0.0-M6` (`1.0.0` 기반 코드도 업로드 예정)

## 강의 구성

### Chapter 1. Spring AI와 LLM 호출
- **이론**: Spring AI를 왜 배워야할까?
- **실습**: Spring AI를 활용해서 LLM 호출하기
- **브랜치**: `chapter1_exercise` (실습용), `chapter1_completed` (완성 코드)

### Chapter 2. 나만의 RAG 챗봇 만들기
- **이론**: 나만의 RAG 챗봇 설계하기
- **실습 1**: RAG 파이프라인 구축하기 - Data Indexing
- **실습 2**: RAG 파이프라인 구축하기 - Data Retrieval & Generation
- **브랜치**: `chapter2` (현재 브랜치)

### Chapter 3. Storm OpenAPI 연동
- **이론**: Storm이란?
- **실습**: Storm OpenAPI를 사용해 초간단 챗봇 만들기
- **브랜치**: `chapter3`

## 참고 사항

### 브랜치 관리
각 Chapter 별로 실습할 때는 해당 브랜치로 전환해주세요.

```bash
# Chapter 1 실습
git switch chapter1_exercise

# Chapter 1 실습 후 완성 코드 확인
git switch chapter1_completed

# Chapter 2 실습
git switch chapter2

# Chapter 3 실습
git switch chapter3
```

## 프로젝트 설정

### 필요한 환경
- **Java**: 17 이상
- **Kotlin**: 1.9.25
- **API Keys**:
    - **Chapter 1-2**: OpenAI API Key (LLM 모델 및 임베딩 모델 사용)
    - **Chapter 3**: Storm API Key (Storm OpenAPI 사용)

### 1. API Key 설정

`application.properties` 파일에 직접 추가
```properties
# Chapter 1-2
spring.ai.openai.api-key=your-openai-api-key-here

# Chapter 3
storm.api.key=your-storm-api-key-here
```

### 2. 프로젝트 빌드 및 실행

```bash
# 프로젝트 빌드
./gradlew build

# 애플리케이션 실행
./gradlew bootRun
```

애플리케이션이 성공적으로 시작되면 다음 주소에서 접근 가능합니다.
- **메인 서버**: http://localhost:8080
- **Swagger UI**: http://localhost:8080/swagger-ui.html

