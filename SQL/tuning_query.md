# 쿼리 튜닝

### 🖤 DESC
 - SELECT문 앞에 DESC 예약어를 붙여 해당 쿼리 실행 계획 분석
 - select_type / table / partitions / possible_keys / key / key_len / ref / rows / filtered / extra
 - select_type : primary / derived 로 나뉘어지며, delrived의 경우 서브 쿼리나 UNION 등을 통해 생성한 임시 테이블을 의미함(임시 테이블의 경우, 인덱스가 없으므로 성능 저하 주의)
 - possible_keys : 사용할 수 있는 인덱스 또는 Primary key
 - rows : 테이블을 스캔하여 읽은 row 수, 데이터 rows. Join시 각 테이블마다 읽어낸 rows가 곱해짐
 - extra : Using index / Using temporary / Using filesoft 등 테이블을 읽는데 인덱스를 사용했는지, 임시 테이블을 사용했는지 아니면 테이블 풀 스캔을 했는지 확인
