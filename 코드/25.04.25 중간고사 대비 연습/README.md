### 1. EMP 테이블의 모든 정보 조회

**문제**: EMP 테이블의 모든 행과 열을 조회하는 쿼리를 작성하세요.

**결과**:
```yaml
EMPNO ENAME   JOB       MGR   HIREDATE   SAL   COMM  DEPTNO
----- ------- --------- ----- ---------- ----- ----- ------
7369  SMITH   CLERK     7902  17-DEC-80   800         20
7499  ALLEN   SALESMAN  7698  20-FEB-81  1600   300    30
7521  WARD    SALESMAN  7698  22-FEB-81  1250   500    30
7566  JONES   MANAGER   7839  02-APR-81  2975         20
7654  MARTIN  SALESMAN  7698  28-SEP-81  1250  1400    30
7698  BLAKE   MANAGER   7839  01-MAY-81  2850         30
7782  CLARK   MANAGER   7839  09-JUN-81  2450         10
7788  SCOTT   ANALYST   7566  19-APR-87  3000         20
7839  KING    PRESIDENT       17-NOV-81  5000         10
7844  TURNER  SALESMAN  7698  08-SEP-81  1500     0    30
7876  ADAMS   CLERK     7788  23-MAY-87  1100         20
7900  JAMES   CLERK     7698  03-DEC-81   950         30
7902  FORD    ANALYST   7566  03-DEC-81  3300         20
7934  MILLER  CLERK     7782  23-JAN-82  1300         10
```

---

### 2. 급여가 1000 초과인 직원 조회

**문제**: 급여(SAL)가 1000보다 많은 직원들의 모든 정보를 조회하세요.

**결과**:
```yaml
EMPNO ENAME   JOB       MGR   HIREDATE   SAL   COMM  DEPTNO
----- ------- --------- ----- ---------- ----- ----- ------
7499  ALLEN   SALESMAN  7698  20-FEB-81  1600   300    30
7521  WARD    SALESMAN  7698  22-FEB-81  1250   500    30
7566  JONES   MANAGER   7839  02-APR-81  2975         20
7654  MARTIN  SALESMAN  7698  28-SEP-81  1250  1400    30
7698  BLAKE   MANAGER   7839  01-MAY-81  2850         30
7782  CLARK   MANAGER   7839  09-JUN-81  2450         10
7788  SCOTT   ANALYST   7566  19-APR-87  3000         20
7839  KING    PRESIDENT       17-NOV-81  5000         10
7844  TURNER  SALESMAN  7698  08-SEP-81  1500     0    30
7876  ADAMS   CLERK     7788  23-MAY-87  1100         20
7902  FORD    ANALYST   7566  03-DEC-81  3300         20
7934  MILLER  CLERK     7782  23-JAN-82  1300         10
```

---

### 3. 직무가 SALESMAN 또는 CLERK인 직원 조회

**문제**: 직무(JOB)가 'SALESMAN' 또는 'CLERK'인 직원의 모든 정보를 조회하세요.

**결과**:
```yaml
EMPNO ENAME   JOB       MGR   HIREDATE   SAL   COMM  DEPTNO
----- ------- --------- ----- ---------- ----- ----- ------
7369  SMITH   CLERK     7902  17-DEC-80   800         20
7499  ALLEN   SALESMAN  7698  20-FEB-81  1600   300    30
7521  WARD    SALESMAN  7698  22-FEB-81  1250   500    30
7654  MARTIN  SALESMAN  7698  28-SEP-81  1250  1400    30
7844  TURNER  SALESMAN  7698  08-SEP-81  1500     0    30
7876  ADAMS   CLERK     7788  23-MAY-87  1100         20
7900  JAMES   CLERK     7698  03-DEC-81   950         30
7934  MILLER  CLERK     7782  23-JAN-82  1300         10
```

---

### 4. 부서번호 오름차순, 이름 오름차순 정렬

**문제**: EMP 테이블의 모든 데이터를 부서번호(DEPTNO) 오름차순, 이름(ENAME) 오름차순으로 정렬해서 조회하세요.

**결과**:
```yaml
EMPNO ENAME   JOB       MGR   HIREDATE   SAL   COMM  DEPTNO
----- ------- --------- ----- ---------- ----- ----- ------
7782  CLARK   MANAGER   7839  09-JUN-81  2450         10
7839  KING    PRESIDENT       17-NOV-81  5000         10
7934  MILLER  CLERK     7782  23-JAN-82  1300         10
7566  JONES   MANAGER   7839  02-APR-81  2975         20
7788  SCOTT   ANALYST   7566  19-APR-87  3000         20
7876  ADAMS   CLERK     7788  23-MAY-87  1100         20
7902  FORD    ANALYST   7566  03-DEC-81  3300         20
7369  SMITH   CLERK     7902  17-DEC-80   800         20
7499  ALLEN   SALESMAN  7698  20-FEB-81  1600   300    30
7698  BLAKE   MANAGER   7839  01-MAY-81  2850         30
7654  MARTIN  SALESMAN  7698  28-SEP-81  1250  1400    30
7900  JAMES   CLERK     7698  03-DEC-81   950         30
7844  TURNER  SALESMAN  7698  08-SEP-81  1500     0    30
7521  WARD    SALESMAN  7698  22-FEB-81  1250   500    30
```

---

### 5. 커미션(COMM)이 NULL인 직원 조회

**문제**: COMM이 NULL인 직원의 이름(ENAME), 급여(SAL), 커미션(COMM)을 조회하세요.

**결과**:
```yaml
ENAME   SAL   COMM
------- ----- ------
SMITH    800
JONES   2975
BLAKE   2850
CLARK   2450
SCOTT   3000
KING    5000
ADAMS   1100
JAMES    950
FORD    3300
MILLER  1300
```

---

### 6. 이름이 'S'로 시작하는 직원 조회

**문제**: 이름(ENAME)이 'S'로 시작하는 직원의 모든 정보를 조회하세요.

**결과**:
```yaml
EMPNO ENAME   JOB    MGR   HIREDATE   SAL  COMM  DEPTNO
----- ------- ------ ----- ---------- ---- ----- ------
7369  SMITH   CLERK  7902  17-DEC-80   800        20
7788  SCOTT   ANALYST 7566 19-APR-87  3000        20
```

---

### 7. MGR 번호가 7902, 7566, 7788 중 하나인 직원 조회

**문제**: MGR이 7902, 7566, 또는 7788 중 하나인 직원의 모든 정보를 조회하세요.

**결과**:
```yaml
EMPNO ENAME   JOB      MGR   HIREDATE   SAL   COMM  DEPTNO
----- ------- -------- ----- ---------- ----- ----- ------
7369  SMITH   CLERK    7902  17-DEC-80   800         20
7788  SCOTT   ANALYST  7566  19-APR-87  3000         20
7876  ADAMS   CLERK    7788  23-MAY-87  1100         20
7900  JAMES   CLERK    7698  03-DEC-81   950         30
```

---

### 8. 직책이 'CLERK'이고 급여가 1000 이상인 직원 조회

**문제**: JOB이 'CLERK'이고 SAL이 1000 이상인 직원의 이름, 직책, 급여를 조회하세요.

**결과**:
```yaml
ENAME   JOB     SAL
------- ------- -----
ADAMS   CLERK   1100
MILLER  CLERK   1300
```

---

### 9. COMM이 0이 아닌 직원만 조회

**문제**: COMM(커미션)이 NULL이 아니고 0이 아닌 직원의 이름, 급여, 커미션을 조회하세요.

**결과**:
```yaml
ENAME   SAL   COMM
------- ----- ------
ALLEN   1600   300
WARD    1250   500
MARTIN  1250  1400
```

---

### 10. 직책(job) 목록을 중복 없이 조회

**문제**: EMP 테이블의 직책(JOB) 목록을 중복 없이 조회하세요.

**결과**:
```yaml
JOB
---------
CLERK
SALESMAN
MANAGER
ANALYST
PRESIDENT
```

---

### 📘 SQL 실습 문제 채점 결과

| 번호 | 쿼리 | 결과 | 피드백 |
|------|------|------|--------|
| 1️⃣ | `SELECT * FROM emp;` | ✅ **정답** | 전체 조회 쿼리 정확해요! |
| 2️⃣ | `SELECT * FROM emp WHERE sal >= 1000;` | ✅ **정답** | 비교 연산자 정확히 사용했어요! |
| 3️⃣ | `SELECT * FROM emp WHERE job IN ('SALESMAN', 'CLERK');` | ✅ **정답** | `IN` 연산자 사용 잘했어요! |
| 4️⃣ | `SELECT * FROM emp ORDER BY deptno, ename;` | ✅ **정답** | 두 컬럼 기준 정렬 정확해요! |
| 5️⃣ | `SELECT ename, sal, comm FROM emp WHERE comm IS NULL;` | ✅ **정답** | NULL 조건문 정확해요! |
| 6️⃣ | `SELECT * FROM emp WHERE ename LIKE 'S%';` | ✅ **정답** | LIKE 패턴 매칭 잘했어요! |
| 7️⃣ | `SELECT * FROM emp WHERE mgr IN (7902, 7566, 7788);` | ✅ **정답** | `IN` 조건문 문제없어요! |
| 8️⃣ | `SELECT ename, job, sal FROM emp WHERE job = 'CLERK' AND sal > 1000;` | ✅ **정답** | 논리 연산자까지 완벽! |
| 9️⃣ | `SELECT ename, sal, comm FROM emp WHERE comm IS NOT NULL AND comm != 0;` | ✅ **정답** | `IS NOT NULL`과 비교 연산자 조합 좋았어요! |
| 🔟 | `SELECT DISTINCT job FROM emp;` | ✅ **정답** | 중복 제거 정확히 잘 했어요! |

---

### ✅ 총점: **10 / 10**

