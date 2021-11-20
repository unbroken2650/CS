# 자료구조

---

## 시스템 생명 주기(System Life Cycle)

요구사항 -> 분석 -> 설계 -> 정제와 코딩 -> 검증

### 요구사항(Requirement)

프로젝트들의 목적을 정의한 명세들의 집합
입력과 출력에 관한 정보를 기술

### 분석(Analysis)

문제들을 다룰 수 있는 작은 단위들로 나눔
상향식(Botton-up)/하향식(Top-down) 접근 방법

### 설계(Design)

추상 데이터 타입(Abstract Data Type, ADT) 생성
알고리즘 명세와 설계 기법 고려

### 정제와 코딩(Refinement and Coding)

데이터 객체에 대한 표현 선택
수행되는 연산에 대한 알고리즘 작성

### 검증(Verification)

-   정확성 증명(Correctness Proof)
    -   수학적 기법들을 이용해서 증명
-   테스트(Testing)
    -   프로그램의 정확한 수행을 검증하고 성능을 검사
-   오류 제거(Error Removal)
    -   독립적 단위로 테스트 후 전체 시스템으로 통합

---

## 객체 지향 프로그래밍(Object-oriented Programming)

: 객체를 기본적인 구성 단위(Building Block)으로 하는 프로그래밍[!](https://ko.wikipedia.org/wiki/%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D) 객체를 클래스와 상속(Inheritance)관계로 연관지음.

### 객체(Object)

: 계산을 수행하고 상태를 갖는 개체 + 데이터+ 절차적 요소

### 클래스(Class)

: 공통된 속성과 동작을 공유하는 객체들의 그룹

### 디자인 패턴(Design Pattern)

: 특정 상황에서 공통적으로 발생하는 문제에 대해 재사용 가능한 해결책들을 모은 것

---

## 데이터 추상화와 캡슐화

### 데이터 추상화(Data Abstraction)

: 객체의 명세(Specification)와 구현(Implementation)을 분리 / What과 How를 명확하게 구분

### 데이터 캡슐화(Data Encapsulation)

: 정보 은닉(Information Hiding) / 외부로부터 데이터 객체의 자세한 구현을 은닉

### 장점

-   소프트웨어 개발의 간소화
-   테스트와 디버깅
-   재사용성
-   데이터 타입의 표현에 대한 수정

<style type="text/css">
  @import url('https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css');
  *{
    font-family: 'Pretendard', sans-serif;
  }
  </style>
