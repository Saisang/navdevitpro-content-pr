---
title: Update purchaseInvoiceLines | Microsoft Docs
description: Updates a purchase invoice line object in Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-businesscentral
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/19/2018
ms.author: solsen
---

# Update purchaseInvoiceLines
Update the properties of a purchase invoice line object for Dynamics 365 Business Central.

## HTTP request

```
PATCH /financials/companies({id})/purchaseInvoices({id})/purchaseInvoiceLines(documentId=({id}),sequence=({number}))
```

## Request headers
|Header        |Value                    |
|--------------|-------------------------|
|Authorization |Bearer {token}. Required.|
|Content-Type  |application/json         |
|If-Match      |Required. When this request header is included and the eTag provided does not match the current tag on the **purchaseInvoiceLines**, the **purchaseInvoiceLines** will not be updated. |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

## Response
If successful, this method returns a ```200 OK``` response code and an updated **purchaseInvoiceLines** object in the response body.

## Example

**Request**

Here is an example of the request.
```json
PATCH https://graph.microsoft.com/beta/financials/companies({id})/purchaseInvoices({id})/purchaseInvoiceLines(documentId=({id}),sequence=({number}))
Content-type: application/json

{
  "description": "someText"
}
```

**Response**

Here is an example of the response. 

> **Note**: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "documentId": "id-value",
  "sequence": 10000,
  "itemId": "id-value",
  "accountId": "id-value",
  "lineType": "Item",
  "description": "someText",
  "unitCost": 71.1,
  "quantity": 96,
  "discountAmount": 0,
  "discountPercent": 0,
  "discountAppliedBeforeTax": false,
  "amountExcludingTax": 6825.6,
  "taxCode": "VAT10",
  "taxPercent": 10,
  "totalTaxAmount": 682.56,
  "amountIncludingTax": 7508.16,
  "invoiceDiscountAllocation": 0,
  "netAmount": 6825.6,
  "netTaxAmount": 682.56,
  "netAmountIncludingTax": 7508.16,
  "expectedReceiptDate": "2015-02-24"
}
```

## See also
[Graph Reference](../api/dynamics_graph_reference.md)  
[Working with Dynamics 365 Business Central in Microsoft Graph](../resources/dynamics_overview.md)  
[Error Codes](../dynamics_error_codes.md)  
[Purchase Invoice Line](../resources/dynamics_purchaseinvoiceline.md)  
[Get Purchase Invoice Line](../api/dynamics_purchaseinvoiceline_get.md)  
[Create Purchase Invoice Line](../api/dynamics_create_purchaseinvoiceline.md)  
[Delete Purchase Invoice Line](../api/dynamics_purchaseinvoiceline_delete.md)  