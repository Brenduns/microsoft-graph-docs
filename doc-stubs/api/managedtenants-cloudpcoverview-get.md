---
title: "Get cloudPcOverview"
description: "Read the properties and relationships of a cloudPcOverview object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get cloudPcOverview
Namespace: microsoft.graph.managedTenants



Read the properties and relationships of a [cloudPcOverview](../resources/managedtenants-cloudpcoverview.md) object.

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
GET /tenantRelationships/managedTenants/cloudPcsOverview/{cloudPcOverviewId}
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

If successful, this method returns a `200 OK` response code and a [cloudPcOverview](../resources/managedtenants-cloudpcoverview.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_cloudpcoverview"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/tenantRelationships/managedTenants/cloudPcsOverview/{cloudPcOverviewId}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.cloudPcOverview"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.managedTenants.cloudPcOverview",
    "id": "6057790f-790f-6057-0f79-57600f795760",
    "tenantDisplayName": "String",
    "totalCloudPcStatus": "Integer",
    "numberOfCloudPcStatusNotProvisioned": "Integer",
    "numberOfCloudPcStatusProvisioning": "Integer",
    "numberOfCloudPcStatusProvisioned": "Integer",
    "numberOfCloudPcStatusUpgrading": "Integer",
    "numberOfCloudPcStatusInGracePeriod": "Integer",
    "numberOfCloudPcStatusDeprovisioning": "Integer",
    "numberOfCloudPcStatusFailed": "Integer",
    "numberOfCloudPcStatusUnknown": "Integer",
    "totalCloudPcConnectionStatus": "Integer",
    "numberOfCloudPcConnectionStatusPending": "Integer",
    "numberOfCloudPcConnectionStatusRunning": "Integer",
    "numberOfCloudPcConnectionStatusPassed": "Integer",
    "numberOfCloudPcConnectionStatusFailed": "Integer",
    "numberOfCloudPcConnectionStatusUnkownFutureValue": "Integer",
    "lastRefreshedDateTime": "String (timestamp)"
  }
}
```

