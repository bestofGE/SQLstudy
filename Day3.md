### 학습목표
- 실습 전 알아두어야 할 SQL 개념

### SELECT,FROM,WHERE 구문
- 쓰는 순서는 아래와 같음
- SELECT SHOP_CODE, SHOP_NAME 조회할 칼럼
- FROM STORE 조회할 테이블명
- WHERE COUNTRY ='JAPAN'조건

- 읽는 순서는 FROM절 > WHERE절 > SELECT절
- ex) STORE라는 테이블에서 COUNTRY가 JAPAN인 항목들만 가져와서 SHOP_CODE와 SHOP_NAME만 보여주세요

### JOIN : 테이블과 테이블 붙인다
- #### LEFT JOIN는 왼쪽 테이블을 기준으로 붙임(RIGHT JOIN도 마찬가지)
- #### OUTER은 포괄적으로 붙임
- (합집합! A테이블과 B테이블 둘 다 온전한 상태로 붙여짐)
- 공통적인 값은 그대로 있지만 공통적이지 않은 부분은 한쪽만 데이터 있음, 나머지한쪽은 NULL값 표
- #### INNER는 교집합만 붙임
* ON에는 조건을 써줌

### CASE WHEN : CASE 조건문
- CASE WHEN 조건1 THEN 값1 (조건1 만족 시, 값1)
- WHEN 조건2 THEN 값2 (조건2 만족 시, 값2)
- ELSE 값3 END (그 외 값3) (END 뒤에 별칭이 붙기도 하는데 무시해도 됨 (원하는 목적에 따라 값 분류할 때 씀))

### 비교연산자
- 각 부등호
- BETWEEN a AND b : a와 b값 사이에 있으면 된다(a,b 둘다포함)/ 값이 연속형일 때 사용
- IN (list) : 리스트에 있는 값 중에서 어느 하나라도 일치 / 값이 비연속형일 때 사용
- LIKE '비교문자열' : 비교문자열과 형태가 일치(%:여러문자, _:한문자)
- 예시) WHERE NAME LIKE '홍%', WHERE PRODUCT_CODE LIKE '2_'
- IS NULL : NULL값인 경우 체크

  ### 논리연산자
  - AND : 앞 뒤 조건 동시만족
  - OR : 둘 중 하나만 만족해도 됨
 
  ### 부정 SQL 연산자 (NOT)
  - NOT IN(list) : List 값과 일치하지 않음
  - IS NOT NULL : NULL 값을 갖지 않음
 
  ### 연산자 우선순위
  - 1. 괄호
    2. NOT 연산자
    3. 비교 연산자, SQL 비교 연산자
    4. AND
    5. OR
