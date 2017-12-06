---
title: IDebugPortEx2::GetProgram | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugPortEx2::GetProgram
helpviewer_keywords: IDebugPortEx2::GetProgram
ms.assetid: cd83a111-bfd5-4eae-b576-526466c6b6ec
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 17e4fd03c631be3eb0aeb06a7616df72c4186fb8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idebugportex2getprogram"></a>IDebugPortEx2::GetProgram
Bir program düğümüyle ilişkilendirilen program alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetProgram(   
   IDebugProgramNode2* pProgramNode,  
   IDebugProgram2**    ppProgram  
);  
```  
  
```csharp  
int GetProgram(   
   IDebugProgramNode2 pProgramNode,  
   out IDebugProgram2 ppProgram  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pProgramNode`  
 [in] Bir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) program düğümünü temsil eden nesne.  
  
 `ppProgram`  
 [out] Döndürür bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) program düğümle ilişkilendirilen programı temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)