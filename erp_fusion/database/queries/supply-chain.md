# Queries para Supply Chain 
### BPA e PO
````
SELECT 
        PO_HEADERS.SEGMENT1 PO_NUMBER,
        BPA_HEADERS.SEGMENT1 BPA_NUMBER,
        RSH.RECEIPT_NUM,

        PO_HEADERS.PO_HEADER_ID,
	
        RT.TRANSACTION_ID,
        RSL.TO_ORGANIZATION_ID,
        PLA.ITEM_ID
    FROM PO_LINES_ALL PLA
        JOIN PO_HEADERS_ALL PO_HEADERS ON PLA.PO_HEADER_ID = PO_HEADERS.PO_HEADER_ID
        JOIN PO_HEADERS_ALL BPA_HEADERS ON PLA.FROM_HEADER_ID = BPA_HEADERS.PO_HEADER_ID
        JOIN RCV_TRANSACTIONS RT ON RT.PO_LINE_ID = PLA.PO_LINE_ID
        JOIN RCV_SHIPMENT_LINES RSL ON RSL.PO_HEADER_ID = PO_HEADERS.PO_HEADER_ID
        JOIN RCV_SHIPMENT_HEADERS RSH ON RSH.SHIPMENT_HEADER_ID = RSL.SHIPMENT_HEADER_ID
                                            AND RSH.SHIPMENT_HEADER_ID = RT.SHIPMENT_HEADER_ID
````
### POs da BPA
````
SELECT DISTINCT PO_HEADER_ID FROM PO_LINES_ALL WHERE FROM_HEADER_ID IN (SELECT PO_HEADER_ID FROM PO_HEADERS_ALL WHERE SEGMENT1 = :p_bpa_contract)
````