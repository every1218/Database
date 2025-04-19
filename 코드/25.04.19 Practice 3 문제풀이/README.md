**1. 현재 날짜 표시 쿼리**

**문제:** 현재 날짜를 표시하는 쿼리를 작성하고, 열에 "Date" 레이블을 지정하세요.

**결과:**

```
Date
--------
28-OCT-97
```

```sql
select sysdate "Date" from dual;
```
---



**2. 직원 번호, 이름, 급여 및 15% 인상 급여 쿼리**

**문제:** 직원 번호, 이름, 급여 및 15% 인상된 급여를 정수로 표시하세요. 열에 "New Salary" 레이블을 지정하고, SQL 문을 p3q2.sql 파일에 저장하세요.

---

**3. p3q2.sql 실행 결과**

**결과:**
```
EMPNO ENAME  SAL New Salary
------ -------- ----- ----------
7839 KING   5000       5750
7698 BLAKE  2850       3278
7782 CLARK  2450       2818
7566 JONES  2975       3421
7654 MARTIN 1250       1438
7499 ALLEN  1600       1840
7844 TURNER 1500       1725
7900 JAMES  950        1093
7521 WARD   1250       1438
7902 FORD   3000       3450
7369 SMITH  800        920
7788 SCOTT  3000       3450
7876 ADAMS  1100       1265
7934 MILLER 1300       1495
14 rows selected.`
```
```sql
select empno, ename, sal, round(sal*1.15,0) "New Salary" from emp;
```
---

**4. 급여 인상액이 추가된 p3q2.sql 수정 쿼리**

**문제:** p3q2.sql 쿼리를 수정하여 이전 급여와 새 급여의 차이를 계산하는 열을 추가하고, 열에 "Increase" 레이블을 지정한 후 쿼리를 다시 실행하세요.

**결과:**

```
EMPNO ENAME  SAL New Salary Increase
------ -------- ----- ---------- --------
7839 KING   5000       5750       750
7698 BLAKE  2850       3278       428
7782 CLARK  2450       2818       368
7566 JONES  2975       3421       446`
```
```sql
select empno, ename, sal, round(sal*1.15,0) "New Salary", round(sal*1.15,0)-sal Increase from emp;
```

---

**5. 직원 급여 검토일 쿼리**

**문제:** 직원의 이름, 입사일 및 급여 검토일(입사 후 6개월 후의 첫 번째 월요일)을 표시하는 쿼리를 작성하세요. 열에 "REVIEW" 레이블을 지정하고, 날짜가 "Sunday, the Seventh of September, 1981"과 유사한 형식으로 나타나도록 날짜의 형식을 지정하세요.

**결과:**

```
ENAME      HIREDATE    REVIEW
---------- ----------- --------------------------------------
KING       17-NOV-81   Monday, the Twenty-Fourth of May, 1982
BLAKE      01-MAY-81   Monday, the Second of November, 1981
CLARK      09-JUN-81   Monday, the Fourteenth of December, 1981
JONES      02-APR-81   Monday, the Fifth of October, 1981
MARTIN     28-SEP-81   Monday, the Twenty-Ninth of March, 1982
ALLEN      20-FEB-81   Monday, the Twenty-Fourth of August, 1981
TURNER     08-SEP-81   Monday, the Fifteenth of March, 1982
JAMES      03-DEC-81   Monday, the Seventh of June, 1982
WARD       22-FEB-81   Monday, the Twenty-Fourth of August, 1981
FORD       03-DEC-81   Monday, the Seventh of June, 1982
SMITH      17-DEC-80   Monday, the Twenty-Second of June, 1981
SCOTT      09-DEC-82   Monday, the Thirteenth of June, 1983
ADAMS      12-JAN-83   Monday, the Eighteenth of July, 1983
MILLER     23-JAN-82   Monday, the Twenty-Sixth of July, 1982
14 rows selected.
```

---

**6. 오늘 날짜와 입사일 사이의 개월 수 쿼리**

**문제:** 각 직원에 대해 직원 이름과 오늘 날짜와 직원이 고용된 날짜 사이의 개월 수를 표시하는 쿼리를 작성하세요. 열에 MONTHS_WORKED 레이블을 지정하고, 결과를 고용된 개월 수로 정렬하며, 개월 수를 가장 가까운 정수로 반올림하세요.

**결과:**

```ENAME      MONTHS_WORKED
---------- -------------
ADAMS                177
SCOTT                178
MILLER               188
JAMES                190
FORD                 190
KING                 191
MARTIN               192
TURNER               193
CLARK                196
BLAKE                197
JONES                198
WARD                 199
ALLEN                199
SMITH                202
14 rows selected
```
```sql
select ename, round(months_between(sysdate, hiredate),0) AS MONTHS_WORKED from emp order by MONTHS_WORKED;
```


---

**7. 직원 급여 및 희망 급여 쿼리**

**문제:** 각 직원에 대해 다음을 생성하는 쿼리를 작성하세요: `<직원 이름>` earns `<급여>` monthly but wants `<3 times salary>`. 열에 "Dream Salaries" 레이블을 지정하세요.

**결과:**

```
Dream Salaries
--------------------------------------------------------------------------------
KING earns $5,000.00 monthly but wants $15,000.00.
BLAKE earns $2,850.00 monthly but wants $8,550.00.
CLARK earns $2,450.00 monthly but wants $7,350.00.
JONES earns $2,975.00 monthly but wants $8,925.00.
MARTIN earns $1,250.00 monthly but wants $3,750.00.
ALLEN earns $1,600.00 monthly but wants $4,800.00.
TURNER earns $1,500.00 monthly but wants $4,500.00.
JAMES earns $950.00 monthly but wants $2,850.00.
WARD earns $1,250.00 monthly but wants $3,750.00.
FORD earns $3,000.00 monthly but wants $9,000.00.
SMITH earns $800.00 monthly but wants $2,400.00.
SCOTT earns $3,000.00 monthly but wants $9,000.00.
ADAMS earns $1,100.00 monthly but wants $3,300.00.
MILLER earns $1,300.00 monthly but wants $3,900.00.
14 rows selected.
```
```sql
select ename||' earns '||to_char(sal, '$99,999.99')||' monthly but wants'|| to_char(sal*3, '$99,999.99') AS "Dream Salaries" from emp;
```
---

**8. 직원 이름 및 급여 표시 쿼리 (형식 지정)**

**문제:** 모든 직원의 이름과 급여를 표시하는 쿼리를 작성하세요. 급여의 형식을 15자 길이로 지정하고 왼쪽을 $로 채우세요. 열에 "SALARY" 레이블을 지정하세요.

**결과:**

```
ENAME      SALARY
---------- ---------------
SMITH      $$$$$$$$$$$$800
ALLEN      $$$$$$$$$$$1600
WARD       $$$$$$$$$$$1250
JONES      $$$$$$$$$$$2975
MARTIN     $$$$$$$$$$$1250
BLAKE      $$$$$$$$$$$2850
CLARK      $$$$$$$$$$$2450
SCOTT      $$$$$$$$$$$3000
KING       $$$$$$$$$$$5000
TURNER     $$$$$$$$$$$1500
ADAMS      $$$$$$$$$$$1100
JAMES      $$$$$$$$$$$$950
FORD       $$$$$$$$$$$3000
MILLER     $$$$$$$$$$$1300
14 rows selected.
```
```sql
select ename, lpad(to_char(sal), 15, '$') AS SALARY from emp;
```
---

**9. 직원 이름 (형식 지정) 및 길이 표시 쿼리**

**문제:** 각 직원에 대해 이름의 첫 글자는 대문자로, 다른 모든 글자는 소문자로 표시하고 이름의 길이를 표시하는 쿼리를 작성하세요. 이름이 J, A 또는 M으로 시작하는 모든 직원에 대해 수행하고, 각 열에 적절한 레이블을 지정하세요.

**결과:**

```
Name     Length
-------- ------
Jones         5
Martin        6
Allen         5
James         5
Adams         5
Miller        6
6 rows selected.
```
```sql
select initcap(ename) AS Name, length(ename) AS Length from emp where ename like 'A%' or ename like 'J%' or ename like 'M%';
```
---

**10. 직원 이름, 입사일 및 요일 표시 쿼리**

**문제:** 직원 이름, 입사일 및 직원이 시작한 요일을 표시하는 쿼리를 작성하세요. 열에 DAY 레이블을 지정하고, 결과를 월요일부터 시작하는 요일별로 정렬하세요.

**결과:**

```
ENAME      HIREDATE    DAY
---------- ----------- ---------
MARTIN     28-SEP-81   MONDAY
CLARK      09-JUN-81   TUESDAY
KING       17-NOV-81   TUESDAY
TURNER     08-SEP-81   TUESDAY
SMITH      17-DEC-80   WEDNESDAY
ADAMS      12-JAN-83   WEDNESDAY
JONES      02-APR-81   THURSDAY
FORD       03-DEC-81   THURSDAY
SCOTT      09-DEC-82   THURSDAY
JAMES      03-DEC-81   THURSDAY
ALLEN      20-FEB-81   FRIDAY
BLAKE      01-MAY-81   FRIDAY
MILLER     23-JAN-82   SATURDAY
WARD       22-FEB-81   SUNDAY
14 rows selected
```
```sql
select ename, hiredate, to_char(hiredate, 'DAY') AS "DAY" from emp order by to_char(hiredate, 'D');
```
---

**11. 직원 이름 및 커미션 표시 쿼리**

**문제:** 직원 이름과 커미션 금액을 표시하는 쿼리를 작성하세요. 직원이 커미션을 받지 않는 경우 "No Commission"을 넣고, 열에 COMM 레이블을 지정하세요.

**결과:**

```
ENAME      COMM
---------- -------------
SMITH      No Commission
ALLEN      300
WARD       500
JONES      No Commission
MARTIN     1400
BLAKE      No Commission
CLARK      No Commission
SCOTT      No Commission
KING       No Commission
TURNER     0
ADAMS      No Commission
JAMES      No Commission
FORD       No Commission
MILLER     No Commission
14 rows selected.
```

```sql
select ename, NVL(to_char(comm), 'NO Commission') AS COMM from emp;
```
