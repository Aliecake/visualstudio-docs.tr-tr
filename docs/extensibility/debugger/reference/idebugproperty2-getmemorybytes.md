---
title: IDebugProperty2::GetMemoryBytes | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProperty2::GetMemoryBytes
helpviewer_keywords: IDebugProperty2::GetMemoryBytes
ms.assetid: b32042ed-7a06-4b4a-99ef-fe03b0aa61cc
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c5981a0fb11b4c8af203cf3d7ba33074c7ffd8cc
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idebugproperty2getmemorybytes"></a>IDebugProperty2::GetMemoryBytes
Bir özelliğin değerini oluşturan bellek bayt alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetMemoryBytes (   
   IDebugMemoryBytes2** ppMemoryBytes  
);  
```  
  
```csharp  
int GetMemoryBytes (   
   out IDebugMemoryBytes2 ppMemoryBytes  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppMemoryBytes`  
 [out] Döndürür bir [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md) özelliğinin değerini içeren belleği almak için kullanılan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde hata kodunu döndürür. Döndürür `S_GETMEMORYBYTES_NO_MEMORY_BYTES` almak için hiçbir bellek bayt varsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md)