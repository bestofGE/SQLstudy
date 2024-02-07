#### Day5_ 학습목표
- CASE WHEN과 비교연산자를 활용하여 고객들의 연령대 입력해보기


### ⭐실습1 [고객ID, 나이, 연령대를 추출해보자]
- SELECT MEM_NO, YEAR(GETDATE()) - YEAR(BIRTH_DT)+1 AS AGE
지난 강의에서는 위와 같이 나이를 추출했었다.
연령대를 구분하기 위해서 CASE WHEN을 사용해줄 것이다.

CASE WHEN YEAR(GETDATE()) - YEAR(BIRTH_DT)+1 < 10 '10대 미만' //나이가 10보다 적을 경우
''(실제로는 위와 같이 적어줘야함) BETWEEN '10' AND '19' THEN '10대'
'' BETWEEN '20' AND '29' THEN '20대'
'' BETWEEN '30' AND '39 THEN '30대'
'' BETWEEN '40' AND '49' THEN '40대'
'' BETWEEN '50' AND '100' THEN '50대이상'
ELSE 'XX'
END AS AGEBAND
FROM MEM
-> 각각의 고객별로 AGEBAND라는 항목으로 연령대를 확인할 수 있다.
-> 주의사항은 CASE WHEN구문은 위에서부터 순차적으로 검증되기 때문에 윗줄에서 해당이 되면
아랫줄에는 해당이 되더라도 속하지 않는다. 이 점을 고려해서 CASE WHEN 구문을 더 간단하게 써줄 수 있다.
BETWEEN 대신 <20, <30 이런식으로만 해도 ok!
-> 내가 임의로 데이터를 분류하는 구문인 만큼 예외의 상황도 신중히 고려하여 ELSE를 사용해야한다.

### ⭐실무에서는?
- 우리 브랜드의 고객 연령대를 알면, 이벤트를 기획할 때 경품에 참고할 수 있음
