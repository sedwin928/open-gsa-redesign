---
title: GUI Services
banner-heading: GUI Services
---

<link rel="stylesheet" type="text/css" href="../../assets/swaggerui-dist/swagger-ui.css" >


## Overview
GUI Services (combination of both Web Services and UI) to the Public Users for them to receive Referential data. 

* Public Users are the type of users that are not associated with a Federal Government agency and that do not post data to FPDS-NG.
* Public Users must send User ID, Password and Service Originator ID in their Web Service requests sent to legacy FPDS-NG.

## Getting Started
FPDS-NG offers the following Referential Data GUI Services to the Public Users:

1. Department: getExistingDepartmentURL
2. Agency: getExistingAgencyURL
3. Contracting Office: getExistingContractingOfficeURL
4. Government Office: getExistingGovernmentOfficeURL
5. Country: getExistingCountryURL
6. Place: getExistingPlaceURL
7. NAICS: getExistingNAICSURL
8. PSC: getExistingPSCURL

* GUI service consumers should create new system accounts in beta.SAM.gov and procuring an API_KEY. 
* Once they set up a new system account they can use the API_KEY to call Business web services. 
* Below is the link to system account information:
  https://cm.usa.gov/confluence/display/ALL/System+Account+Documentation
* Initially, authentication will be based on the API_KEY. Eventually this will be enhanced to accept authentication credentials.
* The service can reject if incoming request doesn’t have enough privileges.   
* A place holder in beta.SAM.gov UI will be created to place WSDL files and other FAQ related documents for business service

Web Services can be accessed from Beta via the following sample end points:

Award, IDV, Other Transaction Award, Other Transaction IDV
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/Award 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/IDV 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/OtherTransactionAward 
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/contracts/1.5/OtherTransactionIDV

Referential Data
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Department
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Agency
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/ContractingOffice
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/GovernmentOffice
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.2/GovernmentOffice
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Country
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Place
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/PSC
*	https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/NAICS
*	https://www.api.sam.gov/prod/FPDS/GUIServices/SystemAdministration/1.0/User
*	https://www.api.sam.gov/prod/FPDS/GUIServices/SystemAdministration/1.2/User

 

## API Description

**Endpoint:** https://www.api.sam.gov/prod/ FPDS/GUIServices/DataCollection/contracts/1.5/Award 
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
            &lt;fpds:userID /&gt;
            &lt;fpds:password /&gt;
            &lt;fpds:serviceOriginatorID /&gt;
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


**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Department 
<details>
<summary><b>Department getExistingDepartmentURL Request</b></summary>
<p>
<code><pre>
&lt;urn:getExistingDepartmentURL&gt;
    &lt;authenticationKey&gt;
      &lt;fpds:userID&gt;XXXXXX&lt;/fpds:userID&gt;
      &lt;fpds:password&gt;XXXXXXX&lt;/fpds:password&gt;
      &lt;fpds:serviceOriginatorID&gt;XXXXX&lt;/fpds:serviceOriginatorID&gt;
    &lt;/authenticationKey&gt;
    &lt;departmentID&gt;9700&lt;/departmentID&gt;
&lt;/urn:getExistingDepartmentURL&gt;
</pre></code></p>
</details>

<details>
<summary><b>Department getExistingDepartmentURL Response</b></summary>
<p>
<code><pre>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;ns1:getExistingDepartmentURLResponse xmlns:ns1="https://www.fpds.gov/FPDS"&gt;
   &lt;ns1:requestNumber&gt;1434306305&lt;/ns1:requestNumber&gt;
   &lt;ns1:confirmationNumber&gt;385744666&lt;/ns1:confirmationNumber&gt;
   &lt;ns1:outputMessages&gt;
      &lt;ns1:listOfErrors /&gt;
      &lt;ns1:listOfWarnings /&gt;
      &lt;ns1:listOfInfoMessages /&gt;
   &lt;/ns1:outputMessages&gt;
   &lt;ns1:departmentURL&gt;https://www.fpds.gov/common/jsp/LaunchWebPage.jsp?command=execute&amp;requestid=92847204&lt;/ns1:departmentURL&gt;
&lt;/ns1:getExistingDepartmentURLResponse&gt;
</pre></code></p>
</details>


<!--**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Agency
<details>
<summary><b>Agency getExistingAgencyURL  Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>Agency getExistingAgencyURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>



**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/ContractingOffice 
<details>
<summary><b>Contracting Office getExistingContractingOfficeURL Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>Contracting Office getExistingContractingOfficeURL Response</b></summary>
<p>
<code><pre>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;

</pre></code></p>
</details>



**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/GovernmentOffice
<details>
<summary><b>Government Office getExistingGovernmentOfficeURL  Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>Government Office getExistingGovernmentOfficeURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>



**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.2/GovernmentOffice
<details>
<summary><b>Government Office getExistingGovernmentOfficeURL  Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>Government Office getExistingGovernmentOfficeURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>



**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Country
<details>
<summary><b>Country getExistingCountryURL Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>
 
<details>
<summary><b>Country getExistingCountryURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>



**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Place
<details>
<summary><b>Place getExistingPlaceURL Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>Place getExistingPlaceURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/PSC
<details>
<summary><b>PSC getExistingPSCURL Request</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>

<details>
<summary><b>PSC getExistingPSCURL Response</b></summary>
<p>
<code><pre>

</pre></code></p>
</details>-->

**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/NAICS
<details>
<summary><b>NAICS getExistingNAICSURL Request</b></summary>
<p>
<code><pre>
&lt;urn:getExistingNAICSURL&gt;
    &lt;authenticationKey&gt;
     &lt;fpds:userID&gt;XXXXXXX&lt;/fpds:userID&gt;
     &lt;fpds:password&gt;XXXXXX&lt;/fpds:password&gt;
     &lt;fpds:serviceOriginatorID&gt;XXXXX&lt;/fpds:serviceOriginatorID&gt;
    &lt;/authenticationKey&gt;
    &lt;NAICSCode&gt;111110&lt;/NAICSCode&gt;
&lt;/urn:getExistingNAICSURL&gt; 
</pre></code></p>
</details>

<details>
<summary><b>NAICS getExistingNAICSURL Response</b></summary>
<p>
<code><pre>
&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;ns1:getExistingNAICSURLResponse xmlns:ns1="https://www.fpds.gov/FPDS"&gt;
   &lt;ns1:requestNumber&gt;1434304093&lt;/ns1:requestNumber&gt;
   &lt;ns1:confirmationNumber&gt;385742977&lt;/ns1:confirmationNumber&gt;
   &lt;ns1:outputMessages&gt;
      &lt;ns1:listOfErrors /&gt;
      &lt;ns1:listOfWarnings /&gt;
      &lt;ns1:listOfInfoMessages /&gt;
   &lt;/ns1:outputMessages&gt;
   &lt;ns1:NAICSURL&gt;https://www.fpds.gov/common/jsp/LaunchWebPage.jsp?command=execute&amp;requestid=92846459&lt;/ns1:NAICSURL&gt;
&lt;/ns1:getExistingNAICSURLResponse&gt;
</pre></code></p>
</details>

## OpenAPI Specification File 
You can view the full details of this API in the OpenAPI Specification file available here: 


Award, IDV, Other Transaction Award, Other Transaction IDV
* <a href="v1/Award.wsdl">WSDL file for the Award</a>
* <a href="v1/IDV.wsdl">WSDL file for the IDV</a>
* <a href="v1/OtherTransactionAward.wsdl">WSDL file for the Other Transaction Award</a>
* <a href="v1/OtherTransactionIDV.wsdl">WSDL file for the Other Transaction IDV</a>


Referential Data
* <a href="v1/Department.wsdl">WSDL file for the Department</a>
* <a href="v1/Agency.wsdl">WSDL file for the Other Transaction Agency</a>
* <a href="v1/ContractingOffice.wsdl">WSDL file for the Contracting Office</a>
* <a href="v1/GovernmentOffice.wsdl">WSDL file for the Government Office version 1.0</a>
* <a href="v1/GovernmentOffice-V1.2.wsdl">WSDL file for the Government Office version 1.2</a>
* <a href="v1/Country.wsdl">WSDL file for the Country</a>
* <a href="v1/Place.wsdl">WSDL file for the Place</a>
* <a href="v1/PSC.wsdl">WSDL file for the PSC</a>
* <a href="v1/NAICS.wsdl">WSDL file for the NAICS</a>
* <a href="v1/User.wsdl">WSDL file for the User version 1.0</a>
* <a href="v1/User.wsdl">WSDL file for the User version 1.2</a>


## HTTP Response Codes

| HTTP Response Code | Description |
| ---- | ----------- |
| 200 | Successful. |
| 403 | API key is not correct or was not provided. |


## Contact Us