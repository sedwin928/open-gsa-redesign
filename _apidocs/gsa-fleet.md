---
title: GSA Fleet API
banner-heading: GSA Fleet API
---


## Overview

The GSA Fleet API consists of GSA leased vehicle inventory information, and is intended for consumption by the owning federal agency.  The GSA Fleet API will provide the following information: 

| Class/Tag |	City |
| Fund Code | VIN |
| State |	BLDACCT No 1 |
| Color | Zip | 
| BLDACCT No 2 | State Tag |	
| Contact	| Equipment Code | 
| Model Name | Phone |	
| Unique Rate Indicator | Model Year |	
| Phone Extension |	Rent Rate Monthly | 
| Inventory Change Date | Alternate Phone |	
| Mileage Rate | Previous Class/Tag |	
| Alternate Phone Ext |	Bill Option Code | 
| STD Item # | Fax |	
| AR Rent Rate Monthly | Fuel Type |	
| Internet Address |	AR Rent Rate Mileage |
| Gas Tank Size |	Agency Indicator |	
| Vehicle Type | Engine Code |	
| Agency Bureau |	Garage State | 
| GVWR | Current Month End Mileage |	
| Garage Zip | Customer # |	
| Prev Month End Mileage | Covered MSA | 
| Address 1 | Average Miles |	
| Law Enforcement | Address 2 |	
| Description |	Manufacturer Name | 
| Address 3 |	Trans Date |	
| BOAC |




<p><small><a href="#">Back to top</a></small></p>

## Getting Started

To begin using this API, you will need to send an email to FMSSupportAlert@gsa.gov requsting an API key be created for you.  Access to this information is srictly limited to the owning agency only and any API key will be configured to only the onwing agency's data.  

Once you receive an API key, you will need to provide this API key in the `x-api-key` HTTP header with every API request.

| HTTP Header Name | Description |
| ---- | ----------- |
| x-api-key | API key from api.data.gov.  For sample purposes, you can use `DEMO_KEY` as an API key. |




<p><small><a href="#">Back to top</a></small></p>

## API Description



This API has two primary endpoints:

**Endpoint 1:** https://api.gsa.gov/travel/citypairs/v0/airfares

**Description**   Negotiated airfares

**Query String Parameters**

| Parameter Name | Description |
| ---- | ----------- |
| award_year string | Year of airfare award. Example: '2017' |
| origin_airport_abbrev string | Origin airport abbreviation. Example: 'ABQ'. Must include either this or the destination airport abbreviation. |
| destination_airport_abbrev | Destination airport abbreviation. Example: 'BWI'. Must include either this or the origination airport abbreviation. |

**Expected Result**

| Name  | Description |
| ---- | ----------- |
| ID (integer, optional) | Generated unique identifier. |
| ITEM_NUM (string, optional) | Item number. |
| AWARD_YEAR (string, optional) | Award Year. |
| ORIGIN_AIRPORT_ABBREV (string, optional) | Origin Airport Abbreviation. |
| DESTINATION_AIRPORT_ABBREV (string, optional) | Destinatoin Airport Abbreviation. |
| ORIGIN_CITY_NAME (string, optional) | Original City Name. |
| ORIGIN_STATE (string, optional) | Origin State. |
| ORIGIN_COUNTRY (string, optional) | Origin Country. |
| DESTINATION_CITY_NAME (string, optional) | Destination City Name. |
| DESTINATION_STATE (string, optional) | Destination State. |
| DESTINATION_COUNTRY (string, optional) | Destination Country. |
| AIRLINE_ABBREV (string, optional) | Airline Abbreviation. |
| AWARDED_SERV (string, optional) | Awarded Serv. |
| PAX_COUNT (string, optional) | PAX Count. |
| YCA_FARE (integer, optional) | YCA Fare. |
| XCA_FARE (integer, optional) | XCA Fare. |
| BUSINESS_FARE (integer, optional) | Business Fare. |
| ORIGIN_AIRPORT_LOCATION (string, optional) | Origin Airport Location. |
| DESTINATION_AIRPORT_LOCATION (string, optional) | Destination Airport Location. |
| ORIGIN_CITY_STATE_AIRPORT (string, optional) | Origin City State Airport. |
| DESTINATION_CITY_STATE_AIRPORT (string, optional) | Destination City State Airport. |
| EFFECTIVE_DATE (string, optional) | Expiration Date. |
| EXPIRATION_DATE (string, optional) | Expiration Date. |



**Endpoint 2:** https://api.gsa.gov/travel/citypairs/v0/airfares/{id}

**Description**   Individual airfare by ID

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
