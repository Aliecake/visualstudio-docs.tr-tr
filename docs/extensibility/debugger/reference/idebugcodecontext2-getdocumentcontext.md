---
title: IDebugCodeContext2::GetDocumentContext | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugCodeContext2::GetDocumentContext
helpviewer_keywords:
- IDebugCodeContext2::GetDocumentContext
ms.assetid: d552cc92-963f-43c1-949f-ae6b63a427b8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 833ba9131a8c6b1449833bbeca52d0f1d7b53649
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31105638"
---
# <a name="idebugcodecontext2getdocumentcontext"></a>IDebugCodeContext2::GetDocumentContext
Bu kod bağlamına karşılık gelen belge bağlamını alır. Belge bağlamı bu yönergeyi oluşturulan kaynak koduna karşılık gelen kaynak dosyasında bir konumu temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetDocumentContext(   
   IDebugDocumentContext2** ppSrcCxt  
);  
```  
  
```csharp  
int GetDocumentContext(   
   out IDebugDocumentContext2 ppSrcCxt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppSrcCxt`  
 [out] Döndürür [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) kod bağlamına karşılık gelen nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Kod bağlam konumda bir yürütme akışı kodu yönerge olsa da genellikle, belge bağlamı, bir kaynak dosya konumu olarak değerlendirilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)