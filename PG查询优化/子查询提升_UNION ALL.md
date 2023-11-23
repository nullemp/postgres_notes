# 子查询提升
```
SELECT * 
FROM score sc, 
LATERAL(SELECT * FROM student WHERE sno = 1 
UNION ALL 
SELECT * FROM student WHERE sno = sc.sno) st 
WHERE st.sno > 0; 

```
