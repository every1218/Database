### 1. 모든 직원의 이름, 부서 번호, 부서 이름을 보여주세요.

**문제**: EMP 테이블과 DEPT 테이블을 조인하여 모든 직원의 이름(ENAME), 부서 번호(DEPTNO), 부서 이름(DNAME)을 조회하세요.

**결과**:
```yaml
ENAME      DEPTNO DNAME
---------- ------ --------------
CLARK      10     ACCOUNTING
KING       10     ACCOUNTING
MILLER     10     ACCOUNTING
SMITH      20     RESEARCH
ADAMS      20     RESEARCH
FORD       20     RESEARCH
SCOTT      20     RESEARCH
JONES      20     RESEARCH
ALLEN      30     SALES
BLAKE      30     SALES
MARTIN     30     SALES
JAMES      30     SALES
TURNER     30     SALES
WARD       30     SALES
```

---

### 2. 30번 부서의 모든 직책을 중복 없이 나열하세요.

**문제**: 30번 부서(DEPTNO=30)에 있는 직원들의 직책(JOB)을 중복 없이 조회하세요. 각 직책에 해당하는 근무지(LOC)도 함께 보여주세요.

**결과**:
```yaml
JOB        LOC
---------- --------
CLERK      CHICAGO
MANAGER    CHICAGO
SALESMAN   CHICAGO
```

---

### 3. 커미션을 받는 직원의 이름, 부서 이름, 근무지를 보여주세요.

**문제**: 커미션(COMM)이 NULL이 아닌 직원들의 이름(ENAME), 부서 이름(DNAME), 근무지(LOC)를 조회하세요.

**결과**:
```yaml
ENAME      DNAME          LOC
---------- -------------- --------
ALLEN      SALES          CHICAGO
WARD       SALES          CHICAGO
MARTIN     SALES          CHICAGO
TURNER     SALES          CHICAGO
```

---

### 4. 이름에 'A'가 포함된 모든 직원의 이름과 부서 이름을 보여주세요.

**문제**: 이름(ENAME)에 'A'가 포함된 직원들의 이름과 부서 이름을 조회하세요.

**결과**:
```yaml
ENAME      DNAME
---------- --------------
CLARK      ACCOUNTING
ADAMS      RESEARCH
ALLEN      SALES
WARD       SALES
JAMES      SALES
MARTIN     SALES
BLAKE      SALES
```

---

### 5. DALLAS에서 근무하는 모든 직원의 이름, 직책, 부서 번호, 부서 이름을 보여주세요.

**문제**: 근무지(LOC)가 DALLAS인 직원의 이름, 직책, 부서 번호, 부서 이름을 조회하세요.

**결과**:
```yaml
ENAME      JOB        DEPTNO DNAME
---------- ---------- ------ --------------
SMITH      CLERK      20     RESEARCH
ADAMS      CLERK      20     RESEARCH
FORD       ANALYST    20     RESEARCH
SCOTT      ANALYST    20     RESEARCH
JONES      MANAGER    20     RESEARCH
```

---

### 6. 직원과 그들의 매니저 정보를 보여주세요.

**문제**: 직원의 이름과 번호, 그리고 해당 직원의 매니저 이름과 매니저 번호를 함께 보여주세요. 열 이름은 Employee, Emp#, Manager, Mgr#로 표시하세요.

**결과**:
```yaml
Employee   Emp# Manager    Mgr#
---------- ---- ---------- ----
SCOTT      7788 JONES      7566
FORD       7902 JONES      7566
ALLEN      7499 BLAKE      7698
WARD       7521 BLAKE      7698
JAMES      7900 BLAKE      7698
TURNER     7844 BLAKE      7698
MARTIN     7654 BLAKE      7698
MILLER     7934 CLARK      7782
ADAMS      7876 SCOTT      7788
JONES      7566 KING       7839
CLARK      7782 KING       7839
BLAKE      7698 KING       7839
SMITH      7369 FORD       7902
```

---

### 7. 매니저가 없는 직원(KING 포함)까지 모두 보여주세요.

**문제**: 위 문제에서 매니저가 없는 직원(KING)도 포함하여 직원과 매니저 정보를 모두 보여주세요.

**결과**:
```yaml
Employee   Emp# Manager    Mgr#
---------- ---- ---------- ----
SCOTT      7788 JONES      7566
FORD       7902 JONES      7566
ALLEN      7499 BLAKE      7698
WARD       7521 BLAKE      7698
JAMES      7900 BLAKE      7698
TURNER     7844 BLAKE      7698
MARTIN     7654 BLAKE      7698
MILLER     7934 CLARK      7782
ADAMS      7876 SCOTT      7788
JONES      7566 KING       7839
CLARK      7782 KING       7839
BLAKE      7698 KING       7839
SMITH      7369 FORD       7902
KING       7839
```

---

### 8. 특정 직원과 같은 부서에서 일하는 모든 직원을 보여주세요.

**문제**: 직원 이름, 부서 번호, 그리고 같은 부서에 있는 동료 이름을 보여주세요.  
단, 자기 자신은 제외하고, 각 열에는 `DEPARTMENT`, `EMPLOYEE`, `COLLEAGUE` 라벨을 붙이세요.

**결과 예시**:
```yaml
DEPARTMENT EMPLOYEE   COLLEAGUE
---------- ---------- ----------
10         CLARK      KING
10         CLARK      MILLER
10         KING       CLARK
10         KING       MILLER
10         MILLER     CLARK
10         MILLER     KING
20         ADAMS      FORD
20         ADAMS      JONES
20         ADAMS      SCOTT
20         ADAMS      SMITH
20         FORD       ADAMS
20         FORD       JONES
20         FORD       SCOTT
...
56 rows selected.
```

---

### 9. SALGRADE 구조 확인 및 직원 정보와 등급 함께 출력하기

**문제 1**: SALGRADE 테이블의 구조를 보여주세요.

```yaml
Name       Null?    Type
---------- -------- ------
GRADE               NUMBER
LOSAL               NUMBER
HISAL               NUMBER
```

**문제 2**: EMP 테이블, DEPT 테이블, SALGRADE 테이블을 조인하여 직원 이름, 직책, 부서 이름, 급여, 등급을 보여주세요.

**결과 예시**:
```yaml
ENAME      JOB        DNAME          SAL    GRADE
---------- ---------- -------------- ------ -----
MILLER     CLERK      ACCOUNTING     1300   2
CLARK      MANAGER    ACCOUNTING     2450   4
KING       PRESIDENT  ACCOUNTING     5000   5
SMITH      CLERK      RESEARCH       800    1
SCOTT      ANALYST    RESEARCH       3000   4
FORD       ANALYST    RESEARCH       3000   4
ADAMS      CLERK      RESEARCH       1100   1
JONES      MANAGER    RESEARCH       2975   4
JAMES      CLERK      SALES          950    1
BLAKE      MANAGER    SALES          2850   4
TURNER     SALESMAN   SALES          1500   3
ALLEN      SALESMAN   SALES          1600   3
WARD       SALESMAN   SALES          1250   2
MARTIN     SALESMAN   SALES          1250   2
14 rows selected.
```

---

### 10. BLAKE보다 나중에 입사한 직원들 조회

**문제**: 직원 BLAKE보다 입사일이 늦은 직원들의 이름과 입사일을 출력하세요.

**결과 예시**:
```yaml
ENAME      HIREDATE
---------- ---------
SMITH      17-DEC-80
ALLEN      20-FEB-81
WARD       22-FEB-81
JONES      02-APR-81
```

---

### 11. 매니저보다 먼저 입사한 직원 조회

**문제**: 직원 이름과 입사일, 매니저 이름과 매니저 입사일을 보여주세요.  
단, 직원이 매니저보다 먼저 입사한 경우만 포함되며, 라벨은 각각 `Employee`, `Emp Hiredate`, `Manager`, `Mgr Hiredate`로 하세요.

**결과 예시**:
```yaml
Employee Emp Hiredate Manager Mgr Hiredate
-------- ------------- ------- -------------
ALLEN    20-FEB-81     BLAKE   01-MAY-81
WARD     22-FEB-81     BLAKE   01-MAY-81
JONES    02-APR-81     KING    17-NOV-81
CLARK    09-JUN-81     KING    17-NOV-81
BLAKE    01-MAY-81     KING    17-NOV-81
SMITH    17-DEC-80     FORD    03-DEC-81
6 rows selected.
```

---

### 12. 직원 급여를 별표로 표시하고 급여 내림차순 정렬

**문제**: 직원 이름과 급여를 별표(*)로 표현해서 보여주세요.  
각 별은 100달러를 의미하며, `EMPLOYEE_AND_THEIR_SALARIES` 라벨을 사용하고, 급여 내림차순으로 정렬하세요.

**결과 예시**:
```yaml
EMPLOYEE_AND_THEIR_SALARIES
----------------------------
KING     *************************
FORD     ************************
SCOTT    ***********************
JONES    *********************
BLAKE    ********************
CLARK    *******************
ALLEN    ******************
TURNER   ***************
MILLER   ************
MARTIN   ***********
WARD     **********
ADAMS    ********
JAMES    ******
SMITH    *****
14 rows selected.
```
