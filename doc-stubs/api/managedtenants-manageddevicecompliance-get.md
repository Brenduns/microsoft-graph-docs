---
title: "Get managedDeviceCompliance"
description: "Read the properties and relationships of a managedDeviceCompliance object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get managedDeviceCompliance
Namespace: microsoft.graph.managedTenants



Read the properties and relationships of a [managedDeviceCompliance](../resources/managedtenants-manageddevicecompliance.md) object.

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
GET /tenantRelationships/managedTenants/managedDeviceCompliances/{managedDeviceComplianceId}
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

If successful, this method returns a `200 OK` response code and a [managedDeviceCompliance](../resources/managedtenants-manageddevicecompliance.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_manageddevicecompliance"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationships/managedTenants/managedDeviceCompliances/{managedDeviceComplianceId}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managedDeviceCompliance"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.managedTenants.managedDeviceCompliance",
    "id": "c157c18d-c18d-c157-8dc1-57c18dc157c1",
    "tenantId": "String",
    "tenantDisplayName": "String",
    "managedDeviceId": "String",
    "managedDeviceName": "String",
    "complianceStatus": "String",
    "osDescription": "String",
    "osVersion": "String",
    "lastSyncDateTime": "String (timestamp)",
    "ownerType": "String",
    "model": "String",
    "manufacturer": "String",
    "inGracePeriodUntilDateTime": "String (timestamp)",
    "lastRefreshedDateTime": "String (timestamp)",
    "deviceType": "String"
  }
}
```

