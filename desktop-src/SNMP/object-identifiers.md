---
title: Object Identifiers
description: An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Object Identifiers

An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure. Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers. Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.

The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers. The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.

The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".

For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.

 

 



