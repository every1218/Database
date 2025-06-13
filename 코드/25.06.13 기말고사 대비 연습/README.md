### 1. 근무지(LOC)가 DALLAS인 직원 조회

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

### 2. BLAKE보다 입사일이 늦은 직원 조회

**문제**: 직원 BLAKE보다 입사일이 늦은 직원들의 이름과 입사일을 출력하세요.

**결과**:

```yaml
ENAME      HIREDATE
---------- ---------
SMITH      17-DEC-80
ALLEN      20-FEB-81
WARD       22-FEB-81
JONES      02-APR-81
```

---

### 3. MGR이 NULL이 아니고 최저 연봉이 1000 이상인 그룹 조회

**문제**: MGR이 NULL이 아닌 경우만 포함하고, 최저 연봉이 1000 이상인 경우만 표시하세요. 연봉 내림차순 정렬.

**결과**:

```yaml
MGR   MIN(SAL)
------ --------
7566      3000
7839      2450
7782      1300
7788      1100
```

---

### 4. 부서별 직원 수 및 평균 연봉

**문제**: 모든 부서의 부서 이름, 위치, 직원 수, 평균 연봉을 표시하시오.

**결과**:

```yaml
DNAME       LOC        Number of People   Salary
----------- ---------- ----------------- ---------
ACCOUNTING  NEW YORK                  3     2916.67
RESEARCH    DALLAS                    5     2175.00
SALES       CHICAGO                   6     1566.67
```
