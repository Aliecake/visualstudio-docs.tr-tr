---
title: IDebugFunctionObject::CreateStringObject | Microsoft Docs
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
- IDebugFunctionObject::CreateStringObject
helpviewer_keywords:
- IDebugFunctionObject::CreateStringObject method
ms.assetid: fd6070ab-07d4-4ea1-8d71-b16592d6f1a7
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b6a533dd7fa55ea85a9b4c75f80daf70b462ec25
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49245472"
---
# <a name="idebugfunctionobjectcreatestringobject"></a>IDebugFunctionObject::CreateStringObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir dize nesnesi oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT CreateStringObject(   
   LPCOLESTR      pcstrString,  
   IDebugObject** ppObject  
);  
```  
  
```csharp  
int CreateStringObject(  
   string      pcstrString,   
   out IDebugObject ppOjbect  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcstrString`  
 [in] Dize nesnesi için dize değeri.  
  
 `ppObject`  
 [out] Döndürür bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) yeni oluşturulan bir dize nesnesini temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Tarafından temsil edilen işlevi parametresi bir dize temsil eden bir nesne oluşturmak için bu yöntemi çağırın [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)

