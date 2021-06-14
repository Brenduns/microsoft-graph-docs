---
title: "List credentialUserRegistrationsSummaries"
description: "Get the credentialUserRegistrationsSummary resources from the credentialUserRegistrationsSummaries navigation property."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List credentialUserRegistrationsSummaries
Namespace: microsoft.graph.managedTenants



Get the credentialUserRegistrationsSummary resources from the credentialUserRegistrationsSummaries navigation property.

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
GET /tenantRelationships/managedTenants/credentialUserRegistrationsSummaries
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

If successful, this method returns a `200 OK` response code and a collection of [credentialUserRegistrationsSummary](../resources/credentialuserregistrationssummary.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_credentialuserregistrationssummary"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationships/managedTenants/credentialUserRegistrationsSummaries
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.credentialUserRegistrationsSummary)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedTenants.credentialUserRegistrationsSummary",
      "id": "aef28d78-8d78-aef2-788d-f2ae788df2ae",
      "tenantId": "String",
      "tenantDisplayName": "String",
      "mfaAndSsprCapableUserCount": "Integer",
      "ssprEnabledUserCount": "Integer",
      "mfaRegisteredUserCount": "Integer",
      "ssprRegisteredUserCount": "Integer",
      "totalUserCount": "Integer",
      "securityDefaultsEnabled": "Boolean",
      "mfaConditionalAccessPolicyState": "String",
      "lastRefreshedDateTime": "String (timestamp)"
    }
  ]
}
```

