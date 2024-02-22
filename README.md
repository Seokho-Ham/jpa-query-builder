## SQL 쿼리 빌더 구현

### Step1: Reflection
#### 기능 요구사항
- [x] 클래스 정보 출력
- [x] test로 시작하는 메서드 실행
- [x] @PrintView 어노테이션 메서드 실행
- [x] private field에 값 할당
- [x] 인자를 가진 생성자의 인스턴스 생성


### Step2: QueryBuilder DDL
#### 기능 요구사항
- [x] 1.create 쿼리 만들기
  - 엔티티를 바탕으로 테이블을 생성한다.

- [x] 2.추가된 정보를 통해 create 쿼리 만들어보기
  - pk인 id값은 DB의 AutoIncrement에 의해 생성된다.
  - @Column 어노테이션에 전달된 이름을 컬럼명으로 사용한다.
  - @Column 어노테이션에 전달된 옵션이 적용된다.

- [x] 3.추가된 정보를 통해 create 쿼리 만들어보기2
  - @Table 어노테이션에 전달된 이름을 테이블명으로 사용한다.
  - @Transient 어노테이션이 적용된 필드는 컬럼으로 사용하지 않는다.

- [x] 4.정보를 바탕으로 drop 쿼리 만들어보기
  - 전달된 엔티티를 바탕으로 테이블을 제거한다.