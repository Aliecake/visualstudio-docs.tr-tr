---
title: IDebugEngine2::RemoveSetException | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugEngine2::RemoveSetException
helpviewer_keywords:
- IDebugEngine2::RemoveSetException
ms.assetid: bdd25097-0e9d-4218-b417-0497ea48d2e8
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: fcc3ddfccb622908359b1b28defa92ce1dfd3277
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49274046"
---
# <a name="idebugengine2removesetexception"></a>IDebugEngine2::RemoveSetException
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirtilen özel durum artık hata ayıklama altyapısı tarafından işlenecek şekilde kaldırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT RemoveSetException(   
   EXCEPTION_INFO* pException  
);  
```  
  
```csharp  
int RemoveSetException(   
   EXCEPTION_INFO[] pException  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pException`  
 [in] Bir [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md) kaldırılacak özel durumu açıklayan yapısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Kaldırılmakta olan özel durum daha önce daha önceki bir çağrı tarafından ayarlanmış olması gerekir [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) yöntemi.  
  
 Tüm küme özel durumları tek seferde kaldırmak için çağrı [RemoveAllSetExceptions](../../../extensibility/debugger/reference/idebugengine2-removeallsetexceptions.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)

