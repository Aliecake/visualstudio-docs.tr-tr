---
title: IEnumDebugPorts2::Next | Microsoft Docs
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
- IEnumDebugPorts2::Next
helpviewer_keywords:
- IEnumDebugPorts2::Next
ms.assetid: 3f43d18c-6bd1-4ddd-95ef-9550abd2ad09
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 85c18e93a6b45c804bc87212c48017fb0a7d2ca3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49294404"
---
# <a name="ienumdebugports2next"></a>IEnumDebugPorts2::Next
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Sabit listesinden alınmış sonraki öğe kümesini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Next(  
   ULONG         celt,  
   IDebugPort2** rgelt,  
   ULONG*        pceltFetched  
);  
```  
  
```csharp  
int Next(  
   uint          celt,  
   IDebugPort2[] rgelt,  
   ref uint      pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Alınacak öğelerin sayısı. Ayrıca en büyük boyutunu belirtir `rgelt` dizisi.  
  
 `rgelt`  
 [out içinde] Dizi [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) doldurulacak öğeleri.  
  
 `pceltFetched`  
 [out] Gerçekte döndürülen öğe sayısını döndürür `rgelt`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` istenen öğelerin sayısından daha az döndürülebilen; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)

