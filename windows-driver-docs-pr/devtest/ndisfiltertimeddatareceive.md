---
title: NdisFilterTimedDataReceive rule (ndis)
description: The NdisFilterTimedDataReceive rule verifies that an NDIS filter driver completes a receive request by the FilterReceiveNetBufferLists function before timing out.
ms.assetid: B7B557F5-2D41-4F1F-9DE6-6BE23860A39E
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
keywords: ["NdisFilterTimedDataReceive rule (ndis)"]
topic_type:
- apiref
api_name:
- NdisFilterTimedDataReceive
api_type:
- NA
---

# NdisFilterTimedDataReceive rule (ndis)


The **NdisFilterTimedDataReceive** rule verifies that an NDIS filter driver completes a receive request by the [*FilterReceiveNetBufferLists*](https://msdn.microsoft.com/library/windows/hardware/ff549960) function before timing out.

You can use a kernel debugger to help identify the cause of the problem. Check RULE\_STATE for PendingNbl, which points to the oldest pending [**NET\_BUFFER\_LIST**](https://msdn.microsoft.com/library/windows/hardware/ff568388). Use the [**!ndiskd.nbl**](https://msdn.microsoft.com/library/windows/hardware/ff564156) debugger extension. For information about using the debugger, see [Windows Debugging](https://msdn.microsoft.com/library/windows/hardware/ff551063).

|              |      |
|--------------|------|
| Driver model | NDIS |

|                                   |                                                                                                                                        |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Bug check(s) found with this rule | [**Bug Check 0xC4: DRIVER\_VERIFIER\_DETECTED\_VIOLATION**](https://msdn.microsoft.com/library/windows/hardware/ff560187) ( 0x00092012) |

How to test
-----------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">At run time</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Run [Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff545448) and select the [NDIS/WIFI verification](https://msdn.microsoft.com/library/windows/hardware/dn312128) option. This rule is also tested with the [DDI compliance checking](https://msdn.microsoft.com/library/windows/hardware/hh454208) option.</p></td>
</tr>
</tbody>
</table>

 

 

 





