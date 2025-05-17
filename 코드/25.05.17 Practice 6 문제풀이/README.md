### 1. Blake 부서 직원 조회

**문제**: 'BLAKE'와 같은 부서에 근무하는 직원들의 이름과 입사일을 조회하세요. 단, 결과에는 'BLAKE' 자신은 제외되어야 합니다.

**결과**:
```yaml
ENAME      HIREDATE
---------- -----------
MARTIN     28-SEP-81
ALLEN      20-FEB-81
TURNER     08-SEP-81
JAMES      03-DEC-81
WARD       22-FEB-81
```

---

### 2. 평균 급여를 초과하는 직원 조회

**문제**: 평균 급여보다 더 많은 급여를 받는 직원들의 사번과 이름을 급여 내림차순으로 조회하세요.

**결과**:
```yaml
EMPNO ENAME
----- ----------
7839  KING
7902  FORD
7788  SCOTT
7566  JONES
7698  BLAKE
7782  CLARK
```

---

### 3. 이름에 'T'가 포함된 부서 직원 조회 및 SQL 파일 저장

**문제**: 이름에 'T'라는 문자가 포함된 직원이 속한 부서의 모든 직원들의 사번과 이름을 조회하세요. 이 SQL문은 'p6q3.sql' 파일로 저장해야 합니다.

**결과**:
```yaml
EMPNO ENAME
----- ----------
7566  JONES
7788  SCOTT
7876  ADAMS
7369  SMITH
7902  FORD
7698  BLAKE
7654  MARTIN
7499  ALLEN
7844  TURNER
7900  JAMES
7521  WARD
```

---

### 4. Dallas에 위치한 부서 직원 조회

**문제**: Dallas에 위치한 부서에서 근무하는 직원들의 이름, 부서 번호, 직무를 조회하세요.

**결과**:
```yaml
ENAME      DEPTNO JOB
---------- ------ ---------
JONES      20     MANAGER
FORD       20     ANALYST
SMITH      20     CLERK
SCOTT      20     ANALYST
ADAMS      20     CLERK
```

---

### 5. King에게 보고하는 직원들의 급여 조회

**문제**: 'KING'에게 보고하는 모든 직원들의 이름과 급여를 조회하세요.

**결과**:
```yaml
ENAME      SAL
---------- ------
BLAKE      2850
CLARK      2450
JONES      2975
```

---

### 6. Sales 부서 직원 정보 조회

**문제**: Sales 부서에 근무하는 모든 직원들의 부서 번호, 이름, 직업을 조회하세요.

**결과**:
```yaml
DEPTNO ENAME      JOB
------ ---------- ---------
30     BLAKE      MANAGER
30     MARTIN     SALESMAN
30     ALLEN      SALESMAN
30     TURNER     SALESMAN
30     JAMES      CLERK
30     WARD       SALESMAN
```

---

### 7. p6q3.sql 쿼리 수정 및 재실행

**문제**: 기존 p6q3.sql 쿼리를 수정하여, 평균 급여보다 높은 급여를 받고 이름에 'T'가 포함된 직원이 속한 부서에 근무하는 직원들의 사번, 이름, 급여를 조회하세요. 수정된 쿼리는 'p6q7.sql'로 저장하고 실행하세요.

**결과**:
```yaml
EMPNO ENAME      SAL
----- ---------- ------
7566  JONES      2975
7788  SCOTT      3000
7902  FORD       3000
7698  BLAKE      2850
```
