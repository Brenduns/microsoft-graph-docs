---
title: "List conditionalAccessPolicyCoverages"
description: "Get a list of the conditionalAccessPolicyCoverage objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List conditionalAccessPolicyCoverages
Namespace: microsoft.graph.managedTenants



Get a list of the [conditionalAccessPolicyCoverage](../resources/managedtenants-conditionalaccesspolicycoverage.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /tenantRelationships/managedTenants/conditionalAccessPolicyCoverages
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [conditionalAccessPolicyCoverage](../resources/conditionalaccesspolicycoverage.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_conditionalaccesspolicycoverage"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationships/managedTenants/conditionalAccessPolicyCoverages
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.conditionalAccessPolicyCoverage)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedTenants.conditionalAccessPolicyCoverage",
      "id": "877e299c-299c-877e-9c29-7e879c297e87",
      "tenantDisplayName": "String",
      "conditionalAccessPolicyState": "String",
      "requiresDeviceCompliance": "Boolean",
      "latestPolicyModifiedDateTime": "String (timestamp)"
    }
  ]
}
```

