# Importação de Dados
### Carregando dados de amostra
Para importar dados de amostra para o desenvolvimento do template, é necessário exportar os dados em **formato XML**.
**Exemplo:**
````
<?xml version="1.0" encoding="WINDOWS-1252" ?>
   <VENDOR_REPORT>
    <LIST_G_VENDOR_NAME>
     <G_VENDOR_NAME>
     <VENDOR_NAME>COMPANY A</VENDOR_NAME>
      <LIST_G_INVOICE_NUM>
       <G_INVOICE_NUM>
       <SET_OF_BOOKS_ID>124</SET_OF_BOOKS_ID>
       <GL_DATE>10-NOV-03</GL_DATE>
       <INV_TYPE>Standard</INV_TYPE>
       <INVOICE_NUM>031110</INVOICE_NUM>
       <INVOICE_DATE>10-NOV-03</INVOICE_DATE>
       <INVOICE_CURRENCY_CODE>EUR</INVOICE_CURRENCY_CODE>
       <ENT_AMT>122</ENT_AMT>
       <ACCTD_AMT>122</ACCTD_AMT>
       <VAT_CODE>VAT22%</VAT_CODE>
      </G_INVOICE_NUM>
     </LIST_G_INVOICE_NUM>
     <ENT_SUM_VENDOR>1000.00</ENT_SUM_VENDOR>
     <ACCTD_SUM_VENDOR>1000.00</ACCTD_SUM_VENDOR>  
    </G_VENDOR_NAME>
   </LIST_G_VENDOR_NAME>
  <ACCTD_SUM_REP>108763.68</ACCTD_SUM_REP>
  <ENT_SUM_REP>122039</ENT_SUM_REP>
 </VENDOR_REPORT>
````

1. Acessa a aba da extensão Oracle para MS Word: "Publisher"
2. Clique em Sample XML![Importação de Dados XML BIP](ImportacaoDadosXML.png)
3. Busque e selecione o arquivo .xml contendo os dados de amostra.