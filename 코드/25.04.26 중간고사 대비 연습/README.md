### 1. 사원이름을 모두 대문자로 변환해서 조회

**문제**: `EMP` 테이블에서 사원이름(ENAME)을 대문자로 변환하여 출력하세요.

**결과**:
```yaml
ENAME
----------
SMITH
ALLEN
WARD
...
```

---

### 2. 사원이름의 첫 글자와 세 번째 글자부터 세 글자 연결하여 조회

**문제**: 사원이름의 첫 글자 + ' O ' + 세 번째 글자부터 세 글자를 연결하여 표시하세요.

**결과**:
```yaml
NAME
-----
S O ITH
A O LEN
W O RD
...
```

---

### 3. 급여(SAL) 금액을 천 단위 구분기호와 함께 조회

**문제**: `SAL`을 `1,600` 형식처럼 천 단위 구분기호를 넣어서 출력하세요.

**결과**:
```yaml
SAL
-----
1,600
1,250
...
```

---

### 4. 사원이름에서 'S'가 몇 번째에 나오는지 조회

**문제**: 사원이름(ENAME) 중 'S' 문자가 몇 번째에 나오는지 조회하세요.

**결과**:
```yaml
POSITION
---------
2
1
0
...
```

---

### 5. 급여를 10자리 폭에 `$`로 채워서 왼쪽 정렬하여 조회

**문제**: 급여(SAL)을 10자리로 `$`로 채워서 표시하세요.

**결과**:
```yaml
SALARY
----------
$$$$$1,600
$$$$$1,250
...
```

---

### 6. 사원이름 양쪽 공백 제거 후 조회

**문제**: 사원이름(ENAME) 양쪽 공백을 제거해서 출력하세요.

**결과**:
```yaml
ENAME
------
SMITH
ALLEN
WARD
...
```

---

### 7. 사원이름 중 'A'를 '★'로 바꿔서 조회

**문제**: 사원이름(ENAME) 중 'A'를 '★'로 바꿔 출력하세요.

**결과**:
```yaml
ENAME
------
SMITH
★LLEN
W★RD
...
```

---

### 8. 사원이름과 직업을 연결해서 조회

**문제**: 사원이름(ENAME)과 직업(JOB)을 이어붙여서 출력하세요.

**결과**:
```yaml
DETAIL
---------------
SMITHCLERK
ALLENSALESMAN
WARDSALESMAN
...
```

---

### 9. 급여를 소수 둘째자리까지 반올림하여 조회

**문제**: 급여(SAL)를 소수점 둘째 자리까지 반올림하여 출력하세요.

**결과**:
```yaml
SAL
-----
1600.00
1250.00
...
```

---

### 10. 급여를 소수 첫째자리까지 버림하여 조회

**문제**: 급여(SAL)를 소수 첫째 자리까지만 남기고 버림(TRUNC)하세요.

**결과**:
```yaml
SAL
-----
1600.0
1250.0
...
```

---

### 11. 급여의 올림값 조회

**문제**: 급여(SAL)를 올림하여 출력하세요.

**결과**:
```yaml
SAL
-----
1601
1250
...
```

---

### 12. 급여의 내림값 조회

**문제**: 급여(SAL)를 내림하여 출력하세요.

**결과**:
```yaml
SAL
-----
1600
1249
...
```

---

### 13. 급여를 3으로 나눈 나머지 조회

**문제**: 급여(SAL)를 3으로 나눈 나머지를 구해 출력하세요.

**결과**:
```yaml
MOD_SAL
---------
1
2
0
...
```

---

### 14. 현재 날짜와 시간을 'YYYY-MM-DD' 형식으로 조회

**문제**: `SYSDATE`를 `YYYY-MM-DD` 형식의 문자열로 변환해 출력하세요.

**결과**:
```yaml
TODAY
------------
2025-04-26
```

---

### 15. 현재 날짜에서 2개월 뒤 날짜 조회

**문제**: 현재 날짜에서 2개월을 더한 날짜를 출력하세요.

**결과**:
```yaml
NEW_DATE
------------
2025-06-26
```

---

### 16. 현재 날짜와 입사일 차이를 주 단위로 조회

**문제**: 사원의 입사일(HIREDATE)과 현재 날짜(SYSDATE) 차이를 주(week) 단위로 출력하세요.

**결과**:
```yaml
ENAME   WEEKS
------  -----
SMITH    2285
ALLEN    2283
...
```

---

### 17. 현재 날짜 이후 첫 금요일 날짜 조회

**문제**: 현재 날짜 이후 가장 가까운 금요일 날짜를 출력하세요.

**결과**:
```yaml
NEXT_FRIDAY
------------
2025-05-02
```

---

### 18. 이번 달 마지막 날 조회

**문제**: 이번 달 마지막 날짜를 출력하세요.

**결과**:
```yaml
LAST_DAY
------------
2025-04-30
```

---

### 19. 입사일을 월 단위로 반올림하여 조회

**문제**: 사원의 입사일(HIREDATE)을 월 단위로 반올림하여 출력하세요.

**결과**:
```yaml
ENAME   NEW_HIREDATE
------  ------------
SMITH    1980-12-01
ALLEN    1981-02-01
...
```

---

### 20. 사원의 직업별 보너스 급여 계산

**문제**: 직업(JOB)에 따라 급여(SAL)을 다르게 계산하여 출력하세요.  
(ANALYST는 1.1배, CLERK는 1.15배, MANAGER는 1.2배, 그 외는 그대로)

**결과**:
```yaml
JOB       SAL    BONUS
--------  ----   -----
CLERK     800    920
SALESMAN  1600   1600
MANAGER   2975   3570
...
```

---

| 번호 | 문제 | 결과 | 비고 |
|:---:|:---|:---|:---|
| 1 | `select upper(ename) AS ENAME from emp;` | ✅ | 정확함 |
| 2 | `select substr(ename,1,1) \|\| 'O' \|\| substr(ename,3,1) AS NAME from emp;` | ✅ | 정확함 |
| 3 | `select to_char(sal, '9,999') AS SAL from emp;` | ✅ | 정확함 |
| 4 | `select length(ename) AS POSITION from emp;` | ❌ | 컬럼명이 POSITION인 이유가 애매함 (length는 글자수 의미) |
| 5 | 까먹음 | ❗ | 기억 안남 |
| 6 | 까먹음 | ❗ | 기억 안남 |
| 7 | `select replace(ename,'A','★') AS ENAME from emp;` | ✅ | 정확함 |
| 8 | `select ename\|\|job AS DETAIL from emp;` | ✅ | 정확함 |
| 9 | `select round(sal,2) AS SAL from emp;` | ✅ | 정확함 |
| 10 | `select trunc(sal,1) AS SAL from emp;` | ✅ | 정확함 |
| 11 | `select ceil(sal) AS SAL from emp;` | ✅ | 정확함 |
| 12 | `select floar(sal) AS SAL from emp;` | ❌ | `floor`로 수정 필요 (오타) |
| 13 | `select mod(sal,3) AS MOD_SAL from emp;` | ✅ | 정확함 |
| 14 | `select to_char(sysdate,'yyyy-mm-dd') AS TODAY from dual;` | ✅ | 정확함 |
| 15 | `select add_month(sysdate, 2) AS NEW_DATE from dual;` | ❌ | `add_months`로 수정 필요 (복수형) |
| 16 | `select ename, between_month(sysdate, hiredate)/7 AS WEEKS from emp;` | ❌ | `months_between`로 수정 필요 (함수 이름 오류) |
| 17 | `select next_day(sysdate,'금') AS NEXT_FRIDAY from dual;` | ✅ | 정확함 |
| 18 | `select last_day(sysdate) AS LAST_DAY from dual;` | ✅ | 정확함 |
| 19 | `select ename, round(hiredate, 'MONTH') AS NEW_HIREDATE from emp;` | ✅ | 정확함 |
| 20 | `select job, sal, <- 까먹음` | ❗ | 작성 불완전 |

