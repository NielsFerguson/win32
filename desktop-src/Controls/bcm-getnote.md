---
title: BCM\_GETNOTE message
description: Gets the text of the note associated with a command link button. You can send this message explicitly or use the Button\_GetNote macro.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE message Windows Controls
topic_type:
- apiref
api_name:
- BCM_GETNOTE
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

# BCM\_GETNOTE message

Gets the text of the note associated with a command link button. You can send this message explicitly or use the [**Button\_GetNote**](/windows/win32/Commctrl/nf-commctrl-button_getnote?branch=master) macro.

## Parameters

<dl> <dt>

*wParam* \[in, out\]
</dt> <dd>

A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.

</dd> <dt>

*lParam* \[out\]
</dt> <dd>

The string buffer to receive the text. The buffer must be large enough to accommodate the terminating NULL character.

</dd> </dl>

## Return value

If the message succeeds, it returns **TRUE**. Otherwise it returns **FALSE**.

## Remarks

The **BCM\_GETNOTE** message works only with buttons that have the the [**BS\_COMMANDLINK**](button-styles.md#bs-commandlink) or [**BS\_DEFCOMMANDLINK**](button-styles.md#bs-defcommandlink) button style.

[**GetLastError**](https://msdn.microsoft.com/library/windows/desktop/ms679360) will contain:

-   ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md#bs-defcommandlink) or [**BS\_COMMANDLINK**](button-styles.md#bs-commandlink) style.
-   ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small. The *wParam* parameter will contain the required buffer size, in characters.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[Button Styles](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Button Types](button-types-and-styles.md)
</dt> </dl>

 

 




