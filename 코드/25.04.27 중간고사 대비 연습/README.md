### 1. 부서번호가 10 또는 20인 직원들의 이름과 부서번호 조회

**문제**: 부서번호가 10 또는 20인 직원들의 이름(ENAME)과 부서번호(DEPTNO)를 조회하세요.

**결과**:
```yaml
ENAME      DEPTNO
---------- ------
CLARK      10
KING       10
MILLER     10
SMITH      20
JONES      20
SCOTT      20
FORD       20
```

---

### 2. 이름이 S로 시작하는 직원 조회

**문제**: 이름이 'S'로 시작하는 직원들의 이름을 조회하세요.

**결과**:
```yaml
ENAME
-----
SMITH
SCOTT
```

---

### 3. 커미션(COMM)이 NULL인 직원 조회

**문제**: 커미션이 없는 직원들의 이름과 커미션을 조회하세요.

**결과**:
```yaml
ENAME      COMM
---------- -----
SMITH      NULL
ALLEN      NULL
WARD       NULL
...
```

---

### 4. 연봉(SAL * 12)을 조회하고 별칭을 ANNUAL로 지정

**문제**: 직원의 연봉(SAL * 12)을 계산하여 ANNUAL로 표시하세요.

**결과**:
```yaml
ENAME      ANNUAL
---------- -------
KING       60000
SCOTT      36000
WARD       15000
...
```

---

### 5. 급여가 높은 순으로 직원 조회

**문제**: 급여가 높은 순으로 이름, 급여를 조회하세요.

**결과**:
```yaml
ENAME      SAL
---------- -----
KING       5000
SCOTT      3000
FORD       3000
...
```

---

### 6. 입사일이 가장 빠른 직원 1명 조회

**문제**: 가장 먼저 입사한 직원의 이름과 입사일을 조회하세요.

**결과**:
```yaml
ENAME      HIREDATE
---------- --------
KING       17-NOV-81
```

---

### 7. 부서번호별로 직원 수 세기

**문제**: 부서번호(DEPTNO)별로 직원 수를 COUNT해서 조회하세요.

**결과**:
```yaml
DEPTNO     COUNT
------     -----
10         3
20         5
30         6
```

---

### 8. JOB이 'CLERK'인 직원들의 평균 급여 구하기

**문제**: 직책이 'CLERK'인 직원들의 평균 급여를 구하세요.

**결과**:
```yaml
AVG_SAL
-------
1037.5
```

---

### 9. 사번(EMPNO)이 짝수인 직원 조회

**문제**: 사번이 짝수인 직원들의 이름과 사번을 조회하세요.

**결과**:
```yaml
ENAME      EMPNO
---------- -----
ALLEN      7499
WARD       7521
...
```

---

### 10. 부서번호별 최고 급여 조회

**문제**: 부서번호별(MAX), 최고급여를 조회하세요.

**결과**:
```yaml
DEPTNO     MAX_SAL
------     -------
10         5000
20         3000
30         2850
```

---

### 11. 사원번호가 7900 이상인 직원 조회

**문제**: 사원번호가 7900 이상인 직원들의 이름과 사원번호를 조회하세요.

**결과**:
```yaml
ENAME      EMPNO
---------- -----
FORD       7902
MILLER     7934
```

---

### 12. 이름의 두 번째 글자가 'A'인 직원 조회

**문제**: 이름 두 번째 글자가 'A'인 직원을 조회하세요.

**결과**:
```yaml
ENAME
-----
MARTIN
BLAKE
WARD
```

---

### 13. 입사일이 1981년 이후인 직원 조회

**문제**: 1981년 이후 입사한 직원들의 이름과 입사일을 조회하세요.

**결과**:
```yaml
ENAME      HIREDATE
---------- --------
SCOTT      09-DEC-82
ADAMS      12-JAN-83
...
```

---

### 14. 직책이 'MANAGER'이면서 급여가 2800 이상인 직원 조회

**문제**: 직책이 'MANAGER'이고 급여가 2800 이상인 직원들을 조회하세요.

**결과**:
```yaml
ENAME      JOB       SAL
---------- --------- -----
BLAKE      MANAGER   2850
```

---

### 15. 급여를 1000 단위로 반올림해서 조회

**문제**: 급여를 1000 단위로 반올림하여 조회하세요.

**결과**:
```yaml
ENAME      ROUND_SAL
---------- ----------
KING       5000
SCOTT      3000
...
```

---

### 16. 모든 직원 이름을 소문자로 변환하여 조회

**문제**: 모든 직원 이름을 소문자로 표시하세요.

**결과**:
```yaml
ENAME
-----
smith
allen
jones
...
```

---

### 17. 급여가 1500 이상 3000 이하인 직원 조회

**문제**: 급여가 1500 이상 3000 이하인 직원들을 조회하세요.

**결과**:
```yaml
ENAME      SAL
---------- -----
JONES      2975
BLAKE      2850
CLARK      2450
...
```

---

### 18. 입사일이 오래된 순서대로 3명만 조회

**문제**: 입사일이 가장 오래된 직원 3명을 조회하세요.

**결과**:
```yaml
ENAME      HIREDATE
---------- --------
SMITH      17-DEC-80
ALLEN      20-FEB-81
WARD       22-FEB-81
```

---

### 19. 급여 대비 커미션 비율(COMM/SAL)을 소수 둘째 자리까지 표시

**문제**: 커미션을 급여 대비 비율로 계산하고 소수점 둘째 자리까지 표시하세요.

**결과**:
```yaml
ENAME      COMM_RATE
---------- ----------
ALLEN      0.2
MARTIN     0.15
```

---

### 20. 부서번호가 30이 아닌 직원 조회

**문제**: 부서번호가 30이 아닌 직원들의 이름과 부서번호를 조회하세요.

**결과**:
```yaml
ENAME      DEPTNO
---------- ------
SMITH      20
JONES      20
...
```

---

# 📋 채점 결과

---

### 1. ✅ 정답
```sql
SELECT ename, deptno FROM emp WHERE deptno = 10;
```

---

### 2. ✅ 정답
```sql
SELECT ename FROM emp WHERE ename LIKE '%S';
```

---

### 3. ✅ 정답
```sql
SELECT ename, comm FROM emp WHERE comm IS NULL;
```

---

### 4. ✅ 정답
```sql
SELECT ename, sal * 12 AS "ANNUAL" FROM emp;
```

---

### 5. ✅ 정답
```sql
SELECT ename, sal FROM emp ORDER BY sal DESC;
```

---

### 6. ✅ 정답
```sql
SELECT ename, hiredate FROM emp ORDER BY hiredate;
```

---

### 7. ❌ 오답
- **오류**: `depno distinct` 문법 틀림, `DISTINCT`는 칼럼 앞이 아니라 `SELECT DISTINCT`처럼 써야 함
- **모범답안**:
```sql
SELECT DISTINCT deptno, COUNT(deptno) FROM emp GROUP BY deptno;
```

---

### 8. ❌ 오답
- **오류**: `mean` 함수는 없음. 오라클은 `AVG` 써야 함
- **모범답안**:
```sql
SELECT AVG(sal) AS AVG_SAL FROM emp WHERE job = 'CLERK';
```

---

### 9. ❌ 오답
- **오류**: `empno%2=0`처럼 직접 연산 쓰면 안 되고 `MOD` 함수 써야 함
- **모범답안**:
```sql
SELECT ename, empno FROM emp WHERE MOD(empno,2) = 0;
```

---

### 10. ❌ 오답
- **오류**: `deptno distinct` 문법 틀림, `GROUP BY` 없이 `DISTINCT`는 의미 없음
- **모범답안**:
```sql
SELECT deptno, MAX(sal) AS MAX_SAL FROM emp GROUP BY deptno;
```

---

### 11. ✅ 정답
```sql
SELECT ename, empno FROM emp WHERE empno >= 7900;
```

---

### 12. ✅ 정답
```sql
SELECT ename FROM emp WHERE ename LIKE '%A';
```

---

### 13. ❌ 오답
- **오류**: 날짜 비교인데 1981을 문자로 안 묶었음 `'1981-01-01'`처럼 해야 함
- **모범답안**:
```sql
SELECT ename, hiredate FROM emp WHERE TO_CHAR(hiredate, 'YYYY-MM-DD') >= '1981-01-01';
```

---

### 14. ✅ 정답
```sql
SELECT ename, job, sal FROM emp WHERE job = 'MANAGER' AND sal >= 2800;
```

---

### 15. ✅ 정답
```sql
SELECT ename, ROUND(sal, -3) AS ROUND_SAL FROM emp;
```

---

### 16. ✅ 정답
```sql
SELECT LOWER(ename) AS ename FROM emp;
```

---

### 17. ✅ 정답
```sql
SELECT ename, sal FROM emp WHERE sal >= 1500 AND sal <= 3000;
```

---

### 18. ✅ 정답
```sql
SELECT ename, hiredate FROM emp ORDER BY hiredate DESC;
```

---

### 19. ❌ 오답
- **오류**: `comm/sal`인데 커미션이 NULL일 수 있으니까 NVL로 감싸줘야 안전해
- **모범답안**:
```sql
SELECT ename, TRUNC(NVL(comm,0)/sal, 2) AS COMM_RATE FROM emp;
```

---

### 20. ✅ 정답
```sql
SELECT ename, deptno FROM emp WHERE deptno != 30;
```

---

# 📈 총평

| 번호 | 결과 |
|:---:|:---:|
| 맞은 문제 | 14개 ✅ |
| 틀린 문제 | 6개 ❌ |

---

# 📚 총정리
- `DISTINCT` → **SELECT DISTINCT 컬럼** 또는 `GROUP BY`
- `AVG` 함수 사용 (`mean` ❌)
- `MOD` 함수 사용 (짝수/홀수 판단)
- 날짜는 `'YYYY-MM-DD'` 형태로 따옴표 필수
- `NVL` 사용해서 NULL 처리 조심

---
