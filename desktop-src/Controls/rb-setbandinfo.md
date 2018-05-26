---
title: RB\_SETBANDINFO message
description: Sets characteristics of an existing band in a rebar control.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO message Windows Controls
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# RB\_SETBANDINFO message

Sets characteristics of an existing band in a rebar control.

## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Zero-based index of the band to receive the new settings.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointer to a [**REBARBANDINFO**](/windows/win32/Commctrl/ns-commctrl-tagrebarbandinfoa?branch=master) structure that defines the band to be modified and the new settings. Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure. Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.

</dd> </dl>

## Return value

Returns nonzero if successful, or zero otherwise.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode and ANSI names<br/>   | **RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)<br/>             |



 

 




