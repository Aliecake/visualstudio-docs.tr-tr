---
title: IDebugCoreServer2::GetMachineUtilities_V7 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugCoreServer2::GetMachineUtilities_V7
helpviewer_keywords: IDebugCoreServer2::GetMachineUtilities_V7
ms.assetid: 64c1f08f-853b-4498-9810-29791581ef2f
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 301af8eb2e6b317a532fec6dfdd5ac64f62d12a9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idebugcoreserver2getmachineutilitiesv7"></a>IDebugCoreServer2::GetMachineUtilities_V7
Bu yöntem, bir sunucu için makine yardımcı programları alır.  
  
> [!NOTE]
>  Bu yöntem artık kullanılmıyor: kullanmayın ([!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] her zaman döndürür `E_NOTIMPL` bu yöntem çağrılır varsa). Geçmiş nedenlerle korunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetMachineUtilities_V7(  
   IDebugMDMUtil2_V7** ppUtil  
);  
```  
  
```csharp  
int GetMachineUtilities_V7(  
   out IDebugMDMUtil2_V7 ppUtil  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppUtil`  
 [out] Döndürür bir `IDebugMDMUtil2_V7` makine yardımcı programları bilgilerini temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Her zaman döndürür `E_NOTIMPL`, yöntem uygulanmadı belirten.  
  
## <a name="remarks"></a>Açıklamalar  
 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]her zaman döndürür `E_NOTIMPL` varsa bu yöntem çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)