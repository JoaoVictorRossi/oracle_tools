# Queries uteis

### Data in Full Form
````
TO_CHAR(SYSDATE, 'DD MONTH YYYY HH:MM','NLS_DATE_LANGUAGE=AMERICAN')
````
### Lookups
````
SELECT MSLT.LOOKUP_CODE FOB_CODE, MSLT.MEANING FROM fusion.MSC_SR_LOOKUP_VALUES_B mslb, fusion.MSC_SR_LOOKUP_VALUES_tl mslt WHERE mslb.lookup_code = mslt.lookup_code AND mslb.lookup_type = 'FOB' AND mslt.language = userenv('LANG')
````