---
title: IEnumDebugObjects::Reset | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IEnumDebugObjects::Reset
helpviewer_keywords: IEnumDebugObjects::Reset method
ms.assetid: 4a245e47-cc39-4177-b83d-083ea0e3190f
caps.latest.revision: "6"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e7b42e3b57752af5ab1e6086711ab020b5ee7946
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="ienumdebugobjectsreset"></a>IEnumDebugObjects::Reset
Bu yöntem ilk öğeye numaralandırması sıfırlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Reset(void);  
```  
  
```csharp  
int Reset();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemi çağrıldıktan sonra sonraki çağrısı [sonraki](../../../extensibility/debugger/reference/ienumdebugobjects-next.md) sabit listesinin ilk öğesini döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md)   
 [Sonraki](../../../extensibility/debugger/reference/ienumdebugobjects-next.md)