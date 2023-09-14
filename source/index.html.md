---
title: System AWS API

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
  - shell
  - HTTP
  - python
  - javascript
  - java

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the s-aws-api
---

# Relational Database Service (RDS)

## Accounts


```python
import requests

url = '/rds/account?user-id=743722'
headers = {'axon_client_id': '','axon_client_secret': ''}

req = requests.get(url, headers=headers)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell
curl "/rds/account?user-id=743722" \
  -H "axon_client_id: " \
  -H "axon_client_secret: " 
```

```HTTP
GET /rds/account?user-id=743722 HTTP/1.1
axon_client_id: 
axon_client_secret: 
```

```javascript
const headers = new Headers();
headers.append('axon_client_id', '');
headers.append('axon_client_secret', '');

const init = {
  method: 'GET',
  headers
};

fetch('/rds/account?user-id=743722', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```

```java
URL url = new URL("/rds/account?user-id=743722");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
con.setRequestProperty("axon_client_id", "");
con.setRequestProperty("axon_client_secret", "");

int status = con.getResponseCode();
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while((inputLine = in.readLine()) != null) {
	content.append(inputLine);
}
in.close();
con.disconnect();
System.out.println("Response status: " + status);
System.out.println(content.toString());
```

> The above command returns JSON structured like this:

```json
[
  {
  "accounts": [
    {
      "accountInfo": {
        "accountCurrencyCode": "USD",
        "accountStatusCode": "ACT",
        "accountStatusDescription": "Active",
        "amountDue": 80.15,
        "availableBalance": 293.82,
        "availableCredit": 293.82,
        "borrowerAvailable": 293.82,
        "branchOrgName": "SVBT",
        "branchOrgNumber": 1872,
        "cardHoldAmount": 0,
        "checkHoldAmount": 0,
        "closeReasonCode": "",
        "closeReasonDescription": null,
        "creditLimit": 2500,
        "currentBalance": 2206.18,
        "deliveryMethodCode": "PRNT",
        "deliveryMethodDescription": "*Printed Statement",
        "dueDate": "2022-02-17T00:00:00",
        "familyFlag": null,
        "fundSourceCode": "",
        "fundSourceDescription": null,
        "hsaCoverageTypeFlag": null,
        "hasLoanLimit": true,
        "hasRestrictions": false,
        "interestCycleCode": "",
        "interestCycleDescription": null,
        "interestRate": 0.0625,
        "interestYield": 0,
        "isPassbookAccount": false,
        "isRetirementAccount": false,
        "isRevolvingLoan": true,
        "isTransactionAccount": false,
        "isValid": true,
        "lastContactDate": "2022-01-17T00:00:00",
        "lastDepositDate": null,
        "lastInterestCreditAmount": null,
        "lastInterestCreditDate": null,
        "lastStatementDate": null,
        "mlAggregateBalance": null,
        "managementHoldAmount": 0,
        "maturityDate": "2030-12-24T00:00:00",
        "nickname": "Line of Credit",
        "openDate": "2000-11-24T00:00:00",
        "ownershipCode": "JA",
        "ownershipDescription": "Joint And",
        "pendingRegD3Count": 0,
        "pendingRegD6Count": 0,
        "regD3Count": 0,
        "regD6Count": 0,
        "regDDAvailableBalance": null,
        "regEOverdraftOptIn": null,
        "relatedBalance": null,
        "retirementAccountNumber": null,
        "statementCycleCode": "",
        "statementCycleDescription": null
      },
      "accountNumber": 4146825,
      "combinedStatement": {
        "primaryStatementAccount": null,
        "secondaryStatementAccounts": [],
        "summaryAccounts": []
      },
      "externalEntityId": null,
      "externalEntityInfo": null,
      "isExternalEntity": false,
      "loanAccountInfo": {
        "amortizationFirstDueDate": null,
        "amortizationLeadDays": null,
        "billingLeadDaysOverride": null,
        "branchOrgName": "SVBT",
        "branchOrgNumber": 1872,
        "contractDate": "2000-11-24T00:00:00",
        "hasRestrictions": false,
        "imminentDefaultFlag": false,
        "interestPaidToDate": "2021-12-23T00:00:00",
        "interestRate": ".0625",
        "isPrinSurplusProc": false,
        "isRepricingPlanAllowed": false,
        "lastPaymentAmount": null,
        "lastPaymentDate": null,
        "lastRateChangeDate": "2020-03-16T00:00:00",
        "maturityAnticipatedPayoffDate": null,
        "maturityDate": "2030-12-24T00:00:00",
        "nextPaymentDueDate": "2022-02-17T00:00:00",
        "nickName": "Line of Credit",
        "operatingFundAccruedInt": null,
        "operatingFundBalance": 0,
        "operatingFundIntRate": 0,
        "orignalLTVRatio": null,
        "paymentMethodCode": "BILL",
        "paymentMethodDescription": "Bill to Customer",
        "paymentStatus": "Current",
        "payoffBalanceAsOfDate": "2022-02-14T00:00:00",
        "pmtCalPeriods": [
          {
            "paymentAmount": null,
            "paymentCalculationPeriod": null,
            "paymentCalculationPeriodCode": "",
            "paymentTypeCode": "VACT"
          },
          {
            "paymentAmount": null,
            "paymentCalculationPeriod": null,
            "paymentCalculationPeriodCode": "",
            "paymentTypeCode": "VINT"
          }
        ],
        "priorInterestRate": 0.0725,
        "remainingPayments": null,
        "termMaturityDate": "2030-12-24T00:00:00",
        "totalPerDiem": 0.38
      },
      "orgPersons": null,
      "product": {
        "canDrawFrom": true,
        "canWriteChecks": true,
        "displayName": "Personal Line of Credit",
        "externalProductTypeCode": "",
        "externalProductTypeCodeDescription": "",
        "hsaSourceCode": null,
        "majorAccountType": "CNS",
        "minorAccountType": "CVLM",
        "productFullName": "Personal LOC Variable- Min 25 Consumer Loan",
        "productName": "Personal LOC Variable- Min 25",
        "retirementPlanCategory": null,
        "retirementPlanType": null
      },
      "userFields": null
    }
  ],
  "errors": null,
  "requestNumber": "",
  "requestTypeCode": "7704",
  "wasSuccessful": true
}
]
```

This endpoint retrieves all accounts

### HTTP Request

`GET http://axon.com/api/rds/account`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
user-id | String(required) | Person identifier to fecth the account numbers
axon_client_id | String(required) | ID key required to communicate with Keystone
axon_client_secret | String(required) | Secret key required to communicate with Keystone

<aside class="success">
200
</aside>
<aside class="warning">401: Unauthorized or invalid client application credentials.</aside>
<aside class="warning">500: Bad response from authorization server, or WSDL SOAP Fault error.</aside>

## Account - Transactions

```python
import requests

url = '/rds/account/transaction'
headers = {'axon_client_id': '','axon_client_secret': ''}
body = """{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}"""

req = requests.get(url, headers=headers, data=body)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell
curl "/rds/account/transaction" \
  -d "{\n  \"accountId\": \"892a51b3-f4f1-11ed-a65c-06b6511dd099\",\n  \"fromDate\": \"2023-03-27\",\n  \"toDate\": \"2023-04-27\"\n}" \
  -H "axon_client_id: " \
  -H "axon_client_secret: " 
```

```HTTP
GET /rds/account/transaction HTTP/1.1
axon_client_id: 
axon_client_secret: 

{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}
```

```javascript
const headers = new Headers();
headers.append('axon_client_id', '');
headers.append('axon_client_secret', '');

const body = `{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}`;

const init = {
  method: 'GET',
  headers,
  body
};

fetch('/rds/account/transaction', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```

```java
URL url = new URL("/rds/account/transaction");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
con.setRequestProperty("axon_client_id", "");
con.setRequestProperty("axon_client_secret", "");

/* Payload support */
con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes("{\n");
out.writeBytes("  \"accountId\": \"892a51b3-f4f1-11ed-a65c-06b6511dd099\",\n");
out.writeBytes("  \"fromDate\": \"2023-03-27\",\n");
out.writeBytes("  \"toDate\": \"2023-04-27\"\n");
out.writeBytes("}");
out.flush();
out.close();

int status = con.getResponseCode();
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while((inputLine = in.readLine()) != null) {
	content.append(inputLine);
}
in.close();
con.disconnect();
System.out.println("Response status: " + status);
System.out.println(content.toString());
```

> The above command returns JSON structured like this:

```json
{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}
```

This endpoint retrieves an account transaction

<aside class="success">
200
</aside>
<aside class="warning">401: Unauthorized or invalid client application credentials.</aside>
<aside class="warning">500: Bad response from authorization server, or WSDL SOAP Fault error.</aside>

### HTTP Request

`GET /rds/account/transaction`

### Headers

Parameter | Description
--------- | -----------
axon_client_id | String (Required)
axon_client_secret | String (Required)

## GET Enrich - Transactions

```python
import requests

url = '/rds/enrich/transaction'
headers = {'axon_client_id': '','axon_client_secret': ''}
body = """{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}"""

req = requests.get(url, headers=headers, data=body)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell
curl "/rds/enrich/transaction" \
  -d "{\n  \"accountId\": \"892a51b3-f4f1-11ed-a65c-06b6511dd099\",\n  \"fromDate\": \"2023-03-27\",\n  \"toDate\": \"2023-04-27\"\n}" \
  -H "axon_client_id: " \
  -H "axon_client_secret: " 
```

```javascript
const headers = new Headers();
headers.append('axon_client_id', '');
headers.append('axon_client_secret', '');

const body = `{
  "accountId": "892a51b3-f4f1-11ed-a65c-06b6511dd099",
  "fromDate": "2023-03-27",
  "toDate": "2023-04-27"
}`;

const init = {
  method: 'GET',
  headers,
  body
};

fetch('/rds/enrich/transaction', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```
```java
URL url = new URL("/rds/enrich/transaction");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
con.setRequestProperty("axon_client_id", "");
con.setRequestProperty("axon_client_secret", "");

/* Payload support */
con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes("{\n");
out.writeBytes("  \"accountId\": \"892a51b3-f4f1-11ed-a65c-06b6511dd099\",\n");
out.writeBytes("  \"fromDate\": \"2023-03-27\",\n");
out.writeBytes("  \"toDate\": \"2023-04-27\"\n");
out.writeBytes("}");
out.flush();
out.close();

int status = con.getResponseCode();
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while((inputLine = in.readLine()) != null) {
	content.append(inputLine);
}
in.close();
con.disconnect();
System.out.println("Response status: " + status);
System.out.println(content.toString());
```

This endpoint enriches an account transaction

<aside class="success">
200
</aside>
<aside class="warning">401: Unauthorized or invalid client application credentials.</aside>
<aside class="warning">500: Bad response from authorization server, or WSDL SOAP Fault error.</aside>

### HTTP Request

`GET /rds/enrich/transaction`

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
accountId | String (Required) | Account Id to fetch the transactions
fromDate | String | From date to fetch account transactions
toDate | String | To date to fetch account transactions

## POST Enrich - Transactions

```python
import requests

url = '/rds/enrich/transaction'
headers = {'axon_client_id': '','axon_client_secret': ''}

req = requests.post(url, headers=headers)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell
curl "/rds/enrich/transaction" \
  -X POST \
  -H "axon_client_id: " \
  -H "axon_client_secret: " 

```

```javascript
const headers = new Headers();
headers.append('axon_client_id', '');
headers.append('axon_client_secret', '');

const init = {
  method: 'POST',
  headers
};

fetch('/rds/enrich/transaction', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```

```java
URL url = new URL("/rds/enrich/transaction");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("POST");
con.setRequestProperty("axon_client_id", "");
con.setRequestProperty("axon_client_secret", "");

int status = con.getResponseCode();
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while((inputLine = in.readLine()) != null) {
	content.append(inputLine);
}
in.close();
con.disconnect();
System.out.println("Response status: " + status);
System.out.println(content.toString());
```

This endpoint enriches an account transaction

<aside class="success">
200
</aside>
<aside class="warning">401: Unauthorized or invalid client application credentials.</aside>
<aside class="warning">500: Bad response from authorization server, or WSDL SOAP Fault error.</aside>

### HTTP Request

`POST /rds/enrich/transaction`

### Headers

Parameter | Description
--------- | -----------
axon_client_id | String (Required)
axon_client_secret | String (Required)

# Kinesis Stream

## POST Record

```python
import requests

url = '/kinesis/record'
headers = {'axon_client_id': '','axon_client_secret': ''}
body = """{
  "streamName": "axon_api_dev",
  "partitionKey": "ACCOUNT-6",
  "data": {
    "self": "/api/v1/me/payees/2809cbbb1a614b4aa4466a90f0368f4a",
    "id": "2809cbbb1a614b4aa4466a90f0368f4a"
  },
  "result": {
    "success": true,
    "resultInfo": []
  }
}"""

req = requests.post(url, headers=headers, data=body)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell
curl "/kinesis/record" \
  -X POST \
  -d "{\n  \"streamName\": \"axon_api_dev\",\n  \"partitionKey\": \"ACCOUNT-6\",\n  \"data\": {\n    \"self\": \"/api/v1/me/payees/2809cbbb1a614b4aa4466a90f0368f4a\",\n    \"id\": \"2809cbbb1a614b4aa4466a90f0368f4a\"\n  },\n  \"result\": {\n    \"success\": true,\n    \"resultInfo\": []\n  }\n}" \
  -H "axon_client_id: " \
  -H "axon_client_secret: " 
```

```javascript
const headers = new Headers();
headers.append('axon_client_id', '');
headers.append('axon_client_secret', '');

const body = `{
  "streamName": "axon_api_dev",
  "partitionKey": "ACCOUNT-6",
  "data": {
    "self": "/api/v1/me/payees/2809cbbb1a614b4aa4466a90f0368f4a",
    "id": "2809cbbb1a614b4aa4466a90f0368f4a"
  },
  "result": {
    "success": true,
    "resultInfo": []
  }
}`;

const init = {
  method: 'POST',
  headers,
  body
};

fetch('/kinesis/record', init)
.then((response) => {
  return response.json(); // or .text() or .blob() ...
})
.then((text) => {
  // text is the response body
})
.catch((e) => {
  // error in e.message
});
```

```java
URL url = new URL("/kinesis/record");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("POST");
con.setRequestProperty("axon_client_id", "");
con.setRequestProperty("axon_client_secret", "");

/* Payload support */
con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes("{\n");
out.writeBytes("  \"streamName\": \"axon_api_dev\",\n");
out.writeBytes("  \"partitionKey\": \"ACCOUNT-6\",\n");
out.writeBytes("  \"data\": {\n");
out.writeBytes("    \"self\": \"/api/v1/me/payees/2809cbbb1a614b4aa4466a90f0368f4a\",\n");
out.writeBytes("    \"id\": \"2809cbbb1a614b4aa4466a90f0368f4a\"\n");
out.writeBytes("  },\n");
out.writeBytes("  \"result\": {\n");
out.writeBytes("    \"success\": true,\n");
out.writeBytes("    \"resultInfo\": []\n");
out.writeBytes("  }\n");
out.writeBytes("}");
out.flush();
out.close();

int status = con.getResponseCode();
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer content = new StringBuffer();
while((inputLine = in.readLine()) != null) {
	content.append(inputLine);
}
in.close();
con.disconnect();
System.out.println("Response status: " + status);
System.out.println(content.toString());
```
> The above command returns JSON structured like this:

```json
{
  "sequenceNumber": "49606335212815173325497162993557985561890649613956808706",
  "shardId": "shardId-000000000000",
  "requestId": "fc908c18-1bbc-9722-ab8d-c7577970ebdc",
  "date": "Fri, 24 Apr 2020 20:16:15 GMT",
  "httpStatusCode": 200
}
```

This endpoint posts records to RDS

<aside class="success">
200
</aside>
<aside class="warning">401: Unauthorized or invalid client application credentials.</aside>
<aside class="warning">500: Bad response from authorization server, or WSDL SOAP Fault error.</aside>

### HTTP Request

`POST /kinesis/record`

### Headers

Parameter | Description
--------- | -----------
axon_client_id | String (Required)
axon_client_secret | String (Required)
