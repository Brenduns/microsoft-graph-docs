---
title: "updates resource type"
description: "Entity that acts as a container for all Windows Update for Business deployment service functionality."
author: "Alice-at-Microsoft"
localization_priority: Normal
ms.prod: "w10"
doc_type: resourcePageType
---

# updates resource type

Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Entity that acts as a container for all Windows Update for Business deployment service functionality.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|Read-only. Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|catalog|[microsoft.graph.windowsUpdates.catalog](../resources/windowsupdates-catalog.md)|Catalog of content that can be approved for deployment by the deployment service. Read-only.|
|deployments|[microsoft.graph.windowsUpdates.deployment](../resources/windowsupdates-deployment.md) collection|Deployments created using the deployment service. Read-only.|
|updatableAssets|[microsoft.graph.windowsUpdates.updatableAsset](../resources/windowsupdates-updatableasset.md) collection|Assets registered with the deployment service that can receive updates. Read-only.|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUpdates.updates",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdates.updates",
  "id": "String (identifier)"
}
```

## Interaction between Graph APIs 
When you use multiple Graph API channels to manage Windows Updates for a device, edits from one Graph API can overwrite edits from the other without awareness. This can create configurations for Windows Updates that are temporary as well as confuse the expected update behaviors. 

As a best practice, use only one Graph API channel to manage the same resources for Windows Updates. The available channels include: 
- **Microsoft Intune or the Device updates Graph API** -   When you use Intune through the Microsoft Endpoint Manager admin center, Intune uses the Graph API for device updates (beginning with this article) to manage Windows Updates. The results are the same as when you use this Graph API directly, without the Intune UI.  Through this Graph API, the configurations and edits for windows updates that get stored in the Windows Update service are associated with Intune. This association is used to identify and display details and status back to Intune. 

- **WUfB-DS Graph API** ([Windows Update for Business deployment service Graph API](https://docs.microsoft.com/windows/deployment/update/deployment-service-overview)). The WUfB-DS Graph API is distinct from that used by Intune. The WUfB-DS Graph API doesn’t keep track of the source for edits or objects in the Windows Update service. If it overwrites objects owned by Intune, Intune won’t be aware of the change or state.

If you choose to use both the Device updates Graph API and the WUfB-DS Graph API, we recommend that you keep the policies and deployments managed by Intune independent from those managed by WUfB-DS Graph API.

