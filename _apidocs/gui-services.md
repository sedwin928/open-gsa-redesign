---
title: Contract Data GUI Services
banner-heading: Contract Data GUI Services
---

<link rel="stylesheet" type="text/css" href="../../assets/swaggerui-dist/swagger-ui.css" >

## Overview
Federal Government Agencies report their Procurement Data to legacy FPDS-NG via their certified COTS/GOTS Contract Writing Systems (CWS).
To facilitate the Agencies report the entire lifecycle of their Procurement Data,legacy FPDS-NG offers a wide variety of Web Services. 

* Public Users are the type of users that are not associated with a Federal Government agency and that do not post data to FPDS-NG.
* Public Users must send User ID, Password and Service Originator ID in their Web Service requests sent to legacy FPDS-NG.

## Getting Started
**Authentication/Authorization in Beta SAM**
* Contract Data GUI service consumers should create new system accounts in beta.SAM.gov and procuring an API_KEY. 
* Once they set up a new system account they can use the API_KEY to call Contract Data GUI services. 
* Below is the link to system account information:
  https://cm.usa.gov/confluence/display/ALL/System+Account+Documentation
* Initially, authentication will be based on the API_KEY. Eventually this will be enhanced to accept authentication credentials.
* The service can reject if incoming request doesn’t have enough privileges.   
* A place holder in beta.SAM.gov UI will be created to place WSDL files and other FAQ related documents for Contract Data GUI service.

**Generating the API Key**
* Registered users can request for a public API on ‘Account Details’ page.
* Users must enter their password on ‘Account Details’ page to view the API Key information. If an incorrect password is entered, an error will be returned.
* After the API Key is generated on ‘Account Details’ page, the API Key can be viewed on the Account Details page immediately.
  The API Key is visible until users navigate to a different page.
* If an error is encountered during the API Key generation/retrieval, then users will receive an error message and they can try again.

**Types of Procurement Data**
* Award – Delivery/Task Order, Purchase Order, Definitive Contract, BPA Call, Intragovernmental, Grant for Research, Funded Space Act Agreement, Training Grant and Cooperative Agreement.
* IDV – FSS, GWAC, BOA, BPA and IDC.
* Other Transaction Award – Other Transaction Agreement and Other Transaction Order.
* Other Transaction IDV – Other Transaction IDV.

**Sub-types of Procurement Data**
* Base – The initial record that is represented as Modification Number = 0.
* Modification – The modification/amendment record to the initial record that is represented as Modification Number <> 0.

**Contract Data GUI Services**
* Award: getNewAwardURL, getNewAwardURLFromTemplate, getExistingAwardURL
* IDV: getNewIDVURL, getNewIDVURLFromTemplate, getExistingIDVURL
* Other Transaction Award: getNewOtherTransactionAwardURL, getExistingOtherTransactionAwardURL
* Other Transaction IDV: getNewOtherTransactionIDVURL, getExistingOtherTransactionIDVURL

**Endpoint Information:**
Web Services can be accessed from Beta via the following sample end points:
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/Award 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/IDV 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/OtherTransactionAward 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/OtherTransactionIDV

 

## API Description

**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/Award 
<details>
<summary><b>getNewAwardURL Request</b></summary>
<p>
<code><pre>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:fpds="https://www.fpds.gov/FPDS" xmlns:urn="urn:FPDS.GUIServices.DataCollection.contracts.Award"&gt;
   &lt;soapenv:Header /&gt;
   &lt;soapenv:Body&gt;
      &lt;urn:getNewAwardURL&gt;
         &lt;authenticationKey&gt;
            &lt;fpds:apiKey/&gt;
         &lt;/authenticationKey&gt;
         &lt;award version="?"&gt;
            &lt;fpds:awardID&gt;
               &lt;fpds:awardContractID&gt;
                  &lt;fpds:agencyID name="?" departmentID="?" departmentName="?"&gt;9700&lt;/fpds:agencyID&gt;
                  &lt;fpds:PIID&gt;FA252119VJMJM&lt;/fpds:PIID&gt;
               &lt;/fpds:awardContractID&gt;
            &lt;/fpds:awardID&gt;
            &lt;fpds:relevantContractDates&gt;
               &lt;fpds:signedDate&gt;2018-10-11 00:00:00&lt;/fpds:signedDate&gt;
            &lt;/fpds:relevantContractDates&gt;
            &lt;fpds:purchaserInformation&gt;
               &lt;fpds:contractingOfficeAgencyID name="?" departmentID="?" departmentName="?"&gt;5700&lt;/fpds:contractingOfficeAgencyID&gt;
               &lt;fpds:contractingOfficeID name="?" regionCode="?"&gt;FA2521&lt;/fpds:contractingOfficeID&gt;
            &lt;/fpds:purchaserInformation&gt;
            &lt;fpds:contractData&gt;
               &lt;fpds:contractActionType description="?" part8OrPart13="?"&gt;B&lt;/fpds:contractActionType&gt;
            &lt;/fpds:contractData&gt;
         &lt;/award&gt;
      &lt;/urn:getNewAwardURL&gt;
   &lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;
</pre></code></p>
</details>

<details>
<summary><b>getNewAwardURL Response</b></summary>
<p>
<code><pre>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"&gt;
   &lt;soapenv:Body&gt;
      &lt;ns1:getNewAwardURLResponse xmlns:ns1="urn:FPDS.GUIServices.DataCollection.contracts.Award" soapenv:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"&gt;
         &lt;ns1:getNewAwardURLResponse xmlns:ns1="https://www.fpds.gov/FPDS"&gt;
            &lt;ns1:requestNumber&gt;2086954286&lt;/ns1:requestNumber&gt;
            &lt;ns1:confirmationNumber&gt;1023905113&lt;/ns1:confirmationNumber&gt;
            &lt;ns1:outputMessages&gt;
               &lt;ns1:listOfErrors /&gt;
               &lt;ns1:listOfWarnings /&gt;
               &lt;ns1:listOfInfoMessages /&gt;
            &lt;/ns1:outputMessages&gt;
            &lt;ns1:awardURL&gt;https://beta.fpds.gov/common/jsp/LaunchWebPage.jsp?command=execute&amp;requestid=85088361&amp;version=1.5&lt;/ns1:awardURL&gt;
         &lt;/ns1:getNewAwardURLResponse&gt;
      &lt;/ns1:getNewAwardURLResponse&gt;
   &lt;/soapenv:Body&gt;
&lt;/soapenv:Envelope&gt;
</pre></code></p>
</details>



## OpenAPI Specification File 
You can view the full details of this API in the WSDL file available here: 

Award, IDV, Other Transaction Award, Other Transaction IDV
* <a href="v1/Award.wsdl">WSDL file for the Award</a>
* <a href="v1/IDV.wsdl">WSDL file for the IDV</a>
* <a href="v1/OtherTransactionAward.wsdl">WSDL file for the Other Transaction Award</a>
* <a href="v1/OtherTransactionIDV.wsdl">WSDL file for the Other Transaction IDV</a>



## HTTP Response Codes

| HTTP Response Code | Description |
| ---- | ----------- |
| 200 | Successful. |
| 400 | <a href="v1/FPDS-NG_V1.5_Data_Validation_rules_document.doc"/>Application Level Error Messages</a>  |
| 403 | API key is not correct or was not provided. |


## Contact Us