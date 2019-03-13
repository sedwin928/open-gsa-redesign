---
title: GUI Services
banner-heading: GUI Services
---

<link rel="stylesheet" type="text/css" href="../../assets/swaggerui-dist/swagger-ui.css" >


## Overview
Legacy FPDS-NG offers GUI Services (combination of both Web Services and UI) to the Public Users for them to receive Referential data. 

* Public Users are the type of users that are not associated with a Federal Government agency and that do not post data to FPDS-NG.
* Legacy FPDS-NG allows Public User accounts (User Type = P) to be created with the default “General Public” role that will help them to 
  access the “Referential Data”. 
* Public Users must send User ID, Password and Service Originator ID in their Web Service requests sent to legacy FPDS-NG.
* Legacy FPDS-NG performs User Authentication to check if the Public User ID exists with an associated Password. 
* Legacy FPDS-NG performs the Mandatory and Format checks and returns the appropriate error messages.


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

For the existing GUI Services users to be able to continue to send and receive data from legacy FPDS-NG, but via the beta.sam.gov space 
and with the least impact, the following recommendations have been made:

* Legacy FPDS-NG Public Users shall be created in beta.sam.gov.
* They shall submit their requests via beta.sam.gov with the new end points.
* They shall not submit their requests to legacy FPDS-NG with the old end points

Web Services can be accessed from Beta via the following sample end points: 
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Department
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Agency
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/ContractingOffice
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/GovernmentOffice
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.2/GovernmentOffice
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Country
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/locations/1.0/Place
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/PSC
https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/ServiceClassifications/1.0/NAICS
 


## API Description

**Endpoint:** https://www.api.sam.gov/prod/FPDS/GUIServices/DataCollection/organizations/1.0/Department 
<details>
<summary><b>Department getExistingDepartmentURL Request</b></summary>
<p>
<code><pre>
&lt;urn:getExistingDepartmentURL&gt;
    &lt;authenticationKey&gt;
      &lt;fpds:userID&gt;JYOTHI-PUBLIC&lt;/fpds:userID&gt;
      &lt;fpds:password&gt;$Cleopatra12345&lt;/fpds:password&gt;
      &lt;fpds:serviceOriginatorID&gt;JYOTHI-PUBLIC&lt;/fpds:serviceOriginatorID&gt;
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
     &lt;fpds:userID&gt;jyothi-public&lt;/fpds:userID&gt;
     &lt;fpds:password&gt;$Cleopatra12345&lt;/fpds:password&gt;
     &lt;fpds:serviceOriginatorID&gt;jyothi-public&lt;/fpds:serviceOriginatorID&gt;
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

Referential Data GUI Services:

* <a href="v1/gui/department.yaml">Open API specification file for the IDV</a>
* <a href="v1/gui/agency.yaml">Open API specification file for the Other Transaction Award</a>
* <a href="v1/gui/contractingOffice.yaml">Open API specification file for the Other Transaction IDV</a>
* <a href="v1/gui/governmentOffice.yaml">Open API specification file for the Award</a>
* <a href="v1/gui/country.yaml">Open API specification file for the IDV</a>
* <a href="v1/gui/place.yaml">Open API specification file for the Other Transaction Award</a>
* <a href="v1/gui/psc.yaml">Open API specification file for the Other Transaction IDV</a>
* <a href="v1/gui/naics.yaml">Open API specification file for the Other Transaction IDV</a>


## HTTP Response Codes

| HTTP Response Code | Description |
| ---- | ----------- |
| 200 | Successful. |
| 403 | API key is not correct or was not provided. |


## Contact Us