# Queries para contabilidade

### Period Name until now
````
SELECT PERIOD_NAME FROM (
    SELECT DISTINCT PERIOD_NAME, START_DATE FROM GL_PERIODS
        WHERE EXTRACT(MONTH FROM SYSDATE) >=  EXTRACT(MONTH FROM END_DATE)
            AND  EXTRACT(YEAR FROM SYSDATE) >=  EXTRACT(YEAR FROM END_DATE)
    ORDER BY START_DATE DESC
)
````