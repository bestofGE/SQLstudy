## 학습목표
- 실습데이터 소개 및 업로드

### 실습데이터
1. 매출데이터(e-commerce)
2. 고객데이터
3. 채널데이터

### 매출데이터
- 각 열에 들어가는 데이터 형식을 지정할 수 있음
- 데이터형식 종류
  텍스트타입: varchar[길이] <br>
  날짜타입: date(연월일), datetime(연월일+시간) <br>
  숫자타입: int(정수타입), decimal(소수점) <br>
- 데이터 살펴보기
- InvoiceNo(거래넘버) / StockCode(제품고유번호)/ Description(상품명) / <br>
Quantity(수량) / InvoiceDate(거래 일자) / UnitPrice(상품단위 당 가격) / CustomerID(고객아이디) / Country(고객의 지역)

### 고객데이터
- 한 사람당 한 줄로 쌓임

### 채널데이터
- channel_code / shop_category
- 고객데이터의 sign_up_ch(가입경로)과 함께 활용

### MSSQL Express 무료버전 설치 <br>
https://www.microsoft.com/ko-kr/sql-server/sql-server-downloads
- 데이터 가져오는 방법
1. 서버 안에 데이터베이스 만들기 (이름은 간단한 영어로)
2. 그 안에 테이블에 올려줄건데
3. 테스크 > 데이터 가져오기 > 마법사 시작 > 데이터 원본선택 > Flat File Source(csv, text파일) > 찾아보기 > 데이터세트 선택 > 
 제대로 미리보기 완료됐으면 sql 서버 선택 후 적재 > 서버는 로컬서버로 윈도우 인증으로 기본으로 두기 > 데이터베이스 선택 잘 돼 있는지 확인 > 파일명 변경 가능 > 매핑편집 > 항목들과 데이터형식 편집 > 확인 누르고 전송완료
4. 테이블을 누른 상태에서 새로고침누르기

- 이러한 순서로 매출데이터, 고객데이터, 채널데이터를 불러와준다.
- (*고객데이터는 엑셀 형태라 데이터원본에서 excel눌러주기 > 시트가 여러개일 경우 어떤걸 고를지 경로 추가됨!
