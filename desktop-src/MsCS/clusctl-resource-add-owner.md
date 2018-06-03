---
title: CLUSCTL\_RESOURCE\_ADD\_OWNER control code
description: Internal.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 0abdba34-7613-4a90-a94f-0afc7531c855
ms.prod: windows-server-dev
ms.technology: failover-clustering
ms.tgt_platform: multiple
keywords:
- CLUSCTL_RESOURCE_ADD_OWNER control code Failover Cluster
topic_type:
- apiref
api_name:
- CLUSCTL_RESOURCE_ADD_OWNER
api_location:
- ClusAPI.h
api_type:
- HeaderDef
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CLUSCTL\_RESOURCE\_ADD\_OWNER control code

Internal. Notifies a [resource DLL](resource-dlls.md) that a [node](nodes.md) has been added to the list of [*possible owner*](https://www.bing.com/search?q=*possible owner*) nodes for a [resource](resources.md) managed by the DLL. Resource DLLs receive this [control code](about-control-codes.md) as a [**ResourceControl**](/previous-versions/windows/desktop/api/ResApi/nc-resapi-presource_control_routine) parameter. Because the control code is internal, applications cannot use it in a control code function.

## Parameters

This control code has no parameters.

## Return value

This control code does not return a value.

## Remarks

### Resource DLL Support

Optional. Support the CLUSCTL\_RESOURCE\_ADD\_OWNER control code if the resource needs to retrieve or update properties or perform other tasks in response to the new possible owner. The [Resource Monitor](resource-monitor.md) does not provide any default processing.

For more information on the [**ResourceControl**](/previous-versions/windows/desktop/api/ResApi/nc-resapi-presource_control_routine) entry point, see [Implementing ResourceControl](implementing-resourcecontrol.md).

ClusAPI.h defines the 32 bits of CLUSCTL\_RESOURCE\_ADD\_OWNER as follows (for more information, see [Control Code Architecture](control-code-architecture.md)).



| Component      | Bit location | Value                                       |
|----------------|--------------|---------------------------------------------|
| Object code    | 24 31        | **CLUS\_OBJECT\_RESOURCE** (0x1)<br/> |
| Global bit     | 23           | **CLUS\_NOT\_GLOBAL** (0x0)<br/>      |
| Modify bit     | 22           | **CLUS\_MODIFY** (0x1)<br/>           |
| User bit       | 21           | **CLCTL\_CLUSTER\_BASE** (0x0)<br/>   |
| Type bit       | 20           | Internal (0x1)<br/>                   |
| Operation code | 0 23         | **CLCTL\_ADD\_OWNER** (0x50001a)<br/> |
| Access code    | 0 1          | **CLUS\_ACCESS\_WRITE** (0x2)<br/>    |



 

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                            |
| Minimum supported server<br/> | Windows Server 2008 Enterprise, Windows Server 2008 Datacenter<br/>            |
| Header<br/>                   | <dl> <dt>ClusAPI.h</dt> </dl> |



## See also

<dl> <dt>

[**AddClusterResourceNode**](/previous-versions/windows/desktop/api/ClusAPI/nc-clusapi-pclusapi_add_cluster_resource_node)
</dt> <dt>

[**ClusterResourceControl**](/previous-versions/windows/desktop/api/ClusAPI/nf-clusapi-clusterresourcecontrol)
</dt> <dt>

[**ResourceControl**](/previous-versions/windows/desktop/api/ResApi/nc-resapi-presource_control_routine)
</dt> </dl>

 

 




