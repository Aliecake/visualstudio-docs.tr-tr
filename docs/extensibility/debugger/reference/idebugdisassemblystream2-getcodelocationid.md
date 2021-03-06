---
title: IDebugDisassemblyStream2::GetCodeLocationId | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
helpviewer_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
ms.assetid: 567adfb8-2f54-499a-a027-e4ecb82277ef
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 86682bb64f041cd8ee1b08bbec02c28492cac7a9
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31107653"
---
# <a name="idebugdisassemblystream2getcodelocationid"></a>IDebugDisassemblyStream2::GetCodeLocationId
Belirli kodu bağlamı için bir kod konumu tanımlayıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetCodeLocationId(   
   IDebugCodeContext2* pCodeContext,  
   UINT64*             puCodeLocationId  
);  
```  
  
```csharp  
int GetCodeLocationId(   
   IDebugCodeContext2 pCodeContext,  
   out ulong          puCodeLocationId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCodeContext`  
 [in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) tanımlayıcıya dönüştürülecek nesne.  
  
 `puCodeLocationId`  
 [out] Kod konumu tanımlayıcısını döndürür. Açıklamalar bakın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_CODE_CONTEXT_OUT_OF_SCOPE` kodu bağlamı geçerli olup olmadığını ancak kapsamı dışında.  
  
## <a name="remarks"></a>Açıklamalar  
 Kod konumu ayrıştırılmış destekleme hata ayıklama altyapısına (DE) belirli tanımlayıcısıdır. Bu konum tanımlayıcı kod konumda izlemek için DE tarafından dahili olarak kullanılır ve genellikle bir adres veya uzaklık belli bir türde. Bir konum kodu bağlamı başka bir konum kodu bağlamı küçükse ilk kod bağlam karşılık gelen kod konumu tanıtıcısı da ikinci kodu bağlamı kod konumu tanıtıcısı daha küçük olmalıdır sonra tek gereksinim olmasıdır.  
  
 Bir kod konumu tanımlayıcı kod bağlamında almak için arama [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md)