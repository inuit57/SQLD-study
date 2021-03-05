자료 참고 : https://gent.tistory.com/326<br>



테이블의 정보를 변경하는 SQL 명령어<br>


1) 컬럼 데이터 타입 정보 변경 <br>
ALTER TABLE [테이블명] MODIFY [컬럼명] [새로운 데이터타입(길이)] <br>

2)컬럼 명 변경 <br>
ALTER TABLE [테이블명] RENAME COLUMN [이전 컬럼명] TO [새로운 컬럼명] <br>


3)주의사항 <br>
3-1) 데이터 타입 변경 <br>
컬럼의 데이터 타입을 변경하기 위해서는 해당 컬럼의 값을 모두 지워야 변경이 가능하다.<br>

그렇지 않으면 아래의 오류가 발생한다.<br>
ORA-01439: column to be modified must be empty to change datatype <br>

3-2) 데이터 길이 변경<br>
컬럼의 길이를 줄일 경우 해당 컬럼의 값 중 변경할 길이보다 큰 값이 있으면 오류가 발생한다.<br>
ORA-01441: cannot decrease column length because some value is too big <br>

```
SELECT *
  FROM emp
 WHERE length(edit_id) > 4
 ```
 길이를 확인하고 처리하는 것이 좋다. <br>
