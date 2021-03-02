출처 : https://goddaehee.tistory.com/55

<H1> 1. DELETE </H1>
- 데이터만 삭제 되며 테이블 용량은 줄어 들지 않는다. 또한 삭제후 잘못 삭제한 것을 되돌릴 수 있다. <br>
- TABLE이나 CLUSTER에 행이 많으면 행이 삭제될 때마다 많은 SYSTEM 자원이 소모 된다.<br>
- Commit이전에는 Rollback이 가능하다.<br>
- 롤백정보를 기록 하므로 Truncate에 비해서 느리다.<br>
- 전체 또는 일부만 삭제 가능 하다.<br>
- 삭제 행수를 반환 한다.<br>
- 데이터를 모두 Delete해도 사용했던 Storage는 Release 처리 되지 않는다.<br>


<H1>2. TRUNCATE </H1>
- 테이블을 최초 생성된 초기상태로 만든다.<br>
- 용량이 줄어들고, 인덱스 등도 모두 삭제 된다.<br>
- <b>Rollback 불가능</b> 하다.<br>
- 무조건 전체 삭제만 가능 하다.<br>
- 삭제 행수를 반환 하지 않는다.<br>
- 테이블이 사용했던 Storage중 최초 테이블 생성시 할당된 Storage만 남기고 Release 처리 된다.<br>

<H1>Drop </H1>
- 기존 테이블의 존재를 삭제한다. (테이블의 정의 자체를 완전히 삭제한다)<br>
- <b>Rollback 불가능</b> 하다.<br>
- 테이블이 사용했던 Storage는 모두 Release 처리 된다.<br>

