---
title: GSA Fleet API
banner-heading: GSA Fleet API
---


## Overview

The GSA Fleet API consists of GSA leased vehicle inventory information, and is intended for consumption by the owning federal agency.  The GSA Fleet API will provide the following information: 


<p><small><a href="#">Back to top</a></small></p>

## Getting Started

To begin using this API, you will need to send an email to FMSSupportAlert@gsa.gov requsting an API key be created for you.  Access to this information is srictly limited to the owning agency only and any API key will be configured to only the onwing agency's data.  

Once you receive an API key, you will need to provide this API key in the `x-api-key` HTTP header with every API request.

| HTTP Header Name | Description |
| ---- | ----------- |
| x-api-key | API key from api.data.gov.  For sample purposes, you can use `DEMO_KEY` as an API key. |




<p><small><a href="#">Back to top</a></small></p>

## API Description



This API provides the following information:

| Class/Tag |	City | Fund Code | VIN | State |	BLDACCT No 1 |
| Color | Zip | BLDACCT No 2 | State Tag |	Contact	| Equipment Code | 
| Model Name | Phone |	Unique Rate Indicator | Model Year |	Phone Extension |	Rent Rate Monthly | 
| Inventory Change Date | Alternate Phone |	Mileage Rate | Previous Class/Tag |	Alternate Phone Ext |	Bill Option Code | 
| STD Item # | Fax |	AR Rent Rate Monthly | Fuel Type |	Internet Address |	AR Rent Rate Mileage |
| Gas Tank Size |	Agency Indicator |	Vehicle Type | Engine Code |	Agency Bureau |	Garage State | 
| GVWR | Current Month End Mileage |	Garage Zip | Customer # |	Prev Month End Mileage | Covered MSA | 
| Address 1 | Average Miles |	Law Enforcement | Address 2 |	Description |	Manufacturer Name | 
| Address 3 |	Trans Date |	BOAC |



**Endpoint 1:** Not sure what to put here

**Description**   

**Query String Parameters**

| Parameter Name | Description |
| ---- | ----------- |
| ----- | --------------------- |
| --------------------- | --------------------------- |


**Expected Result**

| Name  | Description |
| ---- | ----------- |
| VehClassTag (integer) | G10-XXXXX |
| VehVIN (string) | 3XADPXL38XR11X686 |
| VehColor (string) | Red |
| VehStateTag (string) |  |
| VehManfName (string) | Ford |
| VehModelName (string) | FUSIONHEV |
| VehModelYear (string) | 2011 |
| VehInvChgDate (interger) | 20101001 |
| VehPrevClassTag (string) | G11-XXXXX |
| VehSTDitem (string) | 9H |
| VehFuelType (string) | GASOLINE HYBRID ELECTRIC |
| VehGasTankSize (string) | 18.0 |
| VehEngineCode (string) | 4.0 |
| VehGVWR (integer) | 4701 |
| CustBoac (string) | XX4525 |
| CustomerNo (string) | 11-55-00-XX4525-001 |
| CustomerAddr1 (string) | Customer Address |
| CustomerAddr2 (string) | Customer Address 2 |
| CustomerAddr3 (string) | Customer Address 3 |
| CustomerCity (string) | Fairfax |
| CustomerState (string) | VA |
| CustomerZipCode (string) | 22402-5506 |
| CustomerContact (string) | Alfred E. Newman |
| CustPhone (string) | 703-554-8856 |
| CustPhoneExt (integer) | 5525 |
| CustAltPhone (string) | 703-554-9654 |
| CustAltPhoneExt (integer) | 5535 |
| CustFaxNo (string) | 703-662-4245 |
| CusAgencyInd (string) | 50 |
| CusAgencyBureau (integer) | 99 50 |
| CurrMoEndMiles (integer) | 41523 |
| PrevMoEndMiles (integer) | 40552 |
| AvgMoMiles (integer) | 216 |
| IncomeDetlDesc1 (string) | Mileage Entry |
| FundCode (string) | 5500 |
| BldActNo1 (string) | Jefferies |
| BldActNo2 (string) | Garrison  |
| EquipCode (string) | 120205 |
| UniqueRateInd (string) | K |
| RRrentRateMly (string) | 206.00 |
| RRmileageRate (string) | 0.110 |
| BillOptCode (string) | A |
| ARrentRateMly (string) | 0.00 |
| ARrentRateMile (string) | 0.000 |
| VehType (string) | Sedan/St Wgn Compact |
| VehGarageState (string) | VA |
| VehGarageZipCd (integer) | 22402 |
| CoveredMSA (string) | Y |
| LawEnforce (string) | N |




**Endpoint 2:** Not sure what to put here

**Description**   

**Query String Parameters**

| Parameter Name | Description |
| ---- | ----------- |
| id integer | Unique Identifier |

**Expected Result**
(Same response as endpoint 1)

<p><small><a href="#">Back to top</a></small></p>

## OpenAPI Specification File

You can view the full details of this API in the OpenAPI Specification file available here:
<a href="v1/openapi.yaml">Open API specification file for the Sample API</a>

<p><small><a href="#">Back to top</a></small></p>

## HTTP Response Codes

The API will return one of the following responses:

| HTTP Response Code | Description |
| ---- | ----------- |
| 200 | Successful. Data will be returned in JSON format. |
| 400 | Bad request. Verify the query string parmaters that were provided. |
| 403 | API key is not correct or was not provided. |
| 4XX | Additional 400-level are caused by some type of error in the information submitted. |

<p><small><a href="#">Back to top</a></small></p>


## Contact Us

If you have any questions about this API, please contact FMSSupportAlert@gsa.gov.

<p><small><a href="#">Back to top</a></small></p>
