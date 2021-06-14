---
title: "List windowsProtectionStates"
description: "Get the windowsProtectionState resources from the windowsProtectionStates navigation property."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List windowsProtectionStates
Namespace: microsoft.graph.managedTenants



Get the windowsProtectionState resources from the windowsProtectionStates navigation property.

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
GET /tenantRelationships/managedTenants/windowsProtectionStates
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

If successful, this method returns a `200 OK` response code and a collection of [windowsProtectionState](../resources/windowsprotectionstate.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_windowsprotectionstate"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationships/managedTenants/windowsProtectionStates
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.managedTenants.windowsProtectionState)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedTenants.windowsProtectionState",
      "id": "4893d73b-d73b-4893-3bd7-93483bd79348",
      "tenantId": "String",
      "tenantDisplayName": "String",
      "managedDeviceId": "String",
      "managedDeviceName": "String",
      "malwareProtectionEnabled": "Boolean",
      "managedDeviceHealthState": "String",
      "realTimeProtectionEnabled": "Boolean",
      "networkInspectionSystemEnabled": "Boolean",
      "quickScanOverdue": "Boolean",
      "fullScanOverdue": "Boolean",
      "signatureUpdateOverdue": "Boolean",
      "rebootRequired": "Boolean",
      "attentionRequired": "Boolean",
      "fullScanRequired": "Boolean",
      "engineVersion": "String",
      "signatureVersion": "String",
      "antiMalwareVersion": "String",
      "lastQuickScanDateTime": "String (timestamp)",
      "lastFullScanDateTime": "String (timestamp)",
      "lastQuickScanSignatureVersion": "String",
      "lastFullScanSignatureVersion": "String",
      "lastReportedDateTime": "String (timestamp)",
      "devicePropertyRefreshDateTime": "String (timestamp)",
      "deviceDeleted": "Boolean",
      "lastRefreshedDateTime": "String (timestamp)"
    }
  ]
}
```

