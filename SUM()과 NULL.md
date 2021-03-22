SELECT SUM(AA) + SUM(BB) + SUM(CC) + SUM(DD) + SUM(EE) + SUM(FF) SUM1,
       SUM(AA+BB+CC+DD+EE+FF) SUM2
  FROM TESTTABLE.A
 WHERE TESTDATE = '20181026' // 서로 다른 SUM 값이 나옴



ORACLE SUM 함수는 단일 행을 계산할 때는 NULL 값을 제외해주지만
<b>두 컬럼 이상일 때</b>는 NULL 이 있는 로우를 제외시키고 계산하여 값이 다르게 나오게 된다.


따라서 같은 값이 나오게 하려면 NVL 처리를 해주어야만 한다.



SELECT SUM(NVL(AA, 0) + NVL(BB, 0) + NVL(CC, 0) + NVL(DD, 0) + NVL(EE, 0) + NVL(FF, 0) ) SUM2 

 FROM TESTTABLE.A
 
 
 
 
