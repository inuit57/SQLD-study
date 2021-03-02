> UNION 
- 단순하게 합친다고 보면된다. 
- 조건은 columm의 이름이 같아야만 한다는 것. 
- 중복된 값을 제외하고 합쳐준다. 

>UNION ALL
- UNOIN과 동일하다. 
- 차이는 중복을 제거하지 않고 그냥 깡으로 합쳐준다. 


>예시
```
SELECT DISTINCT <b>COL1</b>
FROM SQLD_1
UNION ALL
SELECT <b>COL1</b>
FROM SQLD_2 
```
