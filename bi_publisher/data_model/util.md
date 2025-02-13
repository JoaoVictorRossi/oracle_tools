# SQL queries uteis para DM prompts
### Prompts com múltiplos valores
````
AND (LEAST(:p_inv_org) IS NULL
            OR IOP.ORGANIZATION_CODE IN (:p_inv_org))
AND (LEAST(:p_item) IS NULL
            OR ESIB.ITEM_NUMBER IN (:p_item))
AND (LEAST(:p_sample_number) IS NULL
            OR QS.SAMPLE_NUMBER IN (:p_sample_number))
````
### Prompts com valor único
````
AND HOUFT.NAME           = NVL(:p_plant_name, HOUFT.NAME)
````