---
title: IDebugDisassemblyStream2::GetDocument | Microsoft Docs
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
- IDebugDisassemblyStream2::GetDocument
helpviewer_keywords:
- IDebugDisassemblyStream2::GetDocument
ms.assetid: 3d039a44-ebaa-4413-ac18-7cfd92c408bd
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f0cd8bc5dd2b29dad95fedfe7f18d530cfe8355d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217145"
---
# <a name="idebugdisassemblystream2getdocument"></a>IDebugDisassemblyStream2::GetDocument
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu giriş akışı ile ilişkilendirilen kaynak belge alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetDocument(   
   BSTR              bstrDocumentUrl,  
   IDebugDocument2** ppDocument  
);  
```  
  
```csharp  
int GetDocument(   
   string              bstrDocumentUrl,  
   out IDebugDocument2 ppDocument  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `bstrDocumentUrl`  
 [in] Belge URL'si.  
  
 `ppDocument`  
 [out] Döndürür bir [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) belgeyi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, gerçek bir dosyasında saklanmaz metin belgeleriniz hata ayıklama altyapısı tarafından uygulanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)

