---
title: IDebugProperty2::EnumChildren | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::EnumChildren
helpviewer_keywords:
- IDebugProperty2::EnumChildren
ms.assetid: cf79f666-65d1-417c-af7c-9271bac9a267
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9631ee89dc9d241932b745db4ce094799a899bad
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31122216"
---
# <a name="idebugproperty2enumchildren"></a>IDebugProperty2::EnumChildren
Alt özellik öğelerinin bir listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumChildren (   
   DEBUGPROP_INFO_FLAGS      dwFields,  
   DWORD                     dwRadix,  
   REFGUID                   guidFilter,  
   DBG_ATTRIB_FLAGS          dwAttribFilter,  
   LPCOLESTR                 pszNameFilter,  
   DWORD                     dwTimeout,  
   IEnumDebugPropertyInfo2** ppEnum  
);  
```  
  
```csharp  
int EnumChildren (   
   enum_DEBUGPROP_INFO_FLAGS   dwFields,  
   uint                        dwRadix,  
   ref Guid                    guidFilter,  
   uint                        dwAttribFilter,  
   string                      pszNameFilter,  
   uint                        dwTimeout,  
   out IEnumDebugPropertyInfo2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFields`  
 [in] Bayraklarını bileşimini [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md) hangi alanların numaralandırılmış belirten numaralandırma [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) yapıları olan doldurulmalıdır.  
  
 `dwRadix`  
 [in] Herhangi bir sayısal bilgi biçimlendirmede kullanılacak sayı tabanını belirtir.  
  
 `guidFilter`  
 [in] GUID ile kullanılan filtrenin `dwAttribFilter` ve `pszNameFilter` hangi seçmek için parametreleri `DEBUG_PROPERTY_INFO` alt öğeleri olan numaralandırılacak. Örneğin, `guidFilterLocals` yerel değişkenler için filtreler.  
  
 `dwAttribFilter`  
 [in] Bayraklarını bileşimini [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) , örneğin Numaralandırılacak nesnelerin türünü belirten numaralandırma `DBG_ATTRIB_METHOD` bu özellik alt olabilecek tüm yöntemleri için. İle birlikte kullanılan `guidFilter` ve `pszNameFilter` parametreleri.  
  
 `pszNameFilter`  
 [in] İle kullanılan filtresinin adını `guidFilter` ve `dwAttribFilter` hangi seçmek için parametreleri `DEBUG_PROPERTY_INFO` alt öğeleri olan numaralandırılacak. Örneğin, bu parametre için "MyX" filtreleri "MyX." adlı tüm alt öğeleri ayarlama  
  
 `dwTimeout`  
 [in] Bu yöntemle geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım `INFINITE` sonsuza kadar beklenecek.  
  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) alt özellikleri listesini içeren bir nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde hata kodunu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md)   
 [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)   
 [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md)