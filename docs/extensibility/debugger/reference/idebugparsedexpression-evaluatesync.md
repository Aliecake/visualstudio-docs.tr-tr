---
title: IDebugParsedExpression::EvaluateSync | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugParsedExpression::EvaluateSync
helpviewer_keywords:
- IDebugParsedExpression::EvaluateSync method
ms.assetid: 0ea04cfa-de87-4b6c-897e-4572c1a28942
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0b67294b6bb22ff9607be726415b6aae8a2a9524
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31115248"
---
# <a name="idebugparsedexpressionevaluatesync"></a>IDebugParsedExpression::EvaluateSync
Bu yöntem, ayrıştırılmış ifadeyi hesaplar ve isteğe bağlı olarak başka bir veri türü sonucu çevirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EvaluateSync(   
   DWORD                 dwEvalFlags,  
   DWORD                 dwTimeout,  
   IDebugSymbolProvider* pSymbolProvider,  
   IDebugAddress*        pAddress,  
   IDebugBinder*         pBinder,  
   BSTR                  bstrResultType,  
   IDebugProperty2**     ppResult  
);  
```  
  
```csharp  
int EvaluateSync(  
   uint                 dwEvalFlags,   
   uint                 dwTimeout,   
   IDebugSymbolProvider pSymbolProvider,   
   IDebugAddress        pAddress,   
   IDebugBinder         pBinder,   
   string               bstrResultType,   
   out IDebugProperty2  ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwEvalFlags`  
 [in] Bir birleşimini [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) nasıl değerlendirilecek ifadesidir kontrol sabitleri.  
  
 `dwTimeout`  
 [in] Bu yöntemle geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım `INFINITE` sonsuza kadar beklenecek.  
  
 `pSymbolProvider`  
 [in] Sembol sağlayıcısı olarak ifade edilen, bir [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) arabirimi.  
  
 `pAddress`  
 [in] Geçerli yürütme konumu olarak ifade edilen bir yöntem içinde bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.  
  
 `pBinder`  
 [in] İfade bağlayıcı bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) arabirimi.  
  
 `bstrResultType`  
 [in] Sonuç türü için atamalısınız. Bu bağımsız değişken null değeri olabilir.  
  
 `ppResult`  
 [out] Döndürür [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) değerlendirme sonuçlarını temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendirme bağlamının tarafından verilen `pAddress`, hangi içeren yöntemini belirlemek üzere mümkün kılar ve ardından ifade sembolleri değerini belirlemek için dil kullanım kapsamını kuralları.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)