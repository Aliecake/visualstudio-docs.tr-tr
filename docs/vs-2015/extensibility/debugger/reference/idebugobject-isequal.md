---
title: IDebugObject::IsEqual | Microsoft Docs
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
- IDebugObject::IsEqual
helpviewer_keywords:
- IDebugObject::IsEqual method
ms.assetid: 4b76e663-ef2e-41ff-9be1-bf26d666a34a
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 11c11ace52e9a2b51537f00ee9e2add935edab05
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252635"
---
# <a name="idebugobjectisequal"></a>IDebugObject::IsEqual
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu nesne bir nesneyle karşılaştırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT IsEqual(   
   IDebugObject* pObject,  
   BOOL*         pfIsEqual  
);  
```  
  
```csharp  
int IsEqual(  
   IDebugObject pObject,  
   out int      pfIsEqual  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pObject`  
 [in] Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) karşılaştırma yapılacak nesne temsil eden nesne.  
  
 `pfIsEqual`  
 [out] Sıfır olmayan döndürür (`TRUE`) nesnelerin değerler, eşit; Aksi takdirde, sıfır döndürür (`FALSE`).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, bu yöntem tarafından temsil edilen değerleri adresleri karşılaştırabilirsiniz `pObject` parametresi ve bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne; adresleri eşitse sonra nesneler eşit kabul edilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)

