---
title: BP_FLAGS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- BP_FLAGS
helpviewer_keywords:
- BP_FLAGS enumeration
ms.assetid: c45dfc74-5e7f-4f1e-a147-ab2a55dccbd0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 481dd21287ba3ca68c2abc61412785fc0151788d
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31109957"
---
# <a name="bpflags"></a>BP_FLAGS
Bir kesme noktası ayarlarken ek bilgileri belirtmek için kullanılabilir İsteğe bağlı bayraklar sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_BP_FLAGS {   
   BP_FLAG_NONE            = 0x0000,  
   BP_FLAG_MAP_DOCPOSITION = 0x0001,  
   BP_FLAG_DONT_STOP       = 0x0002  
};  
typedef DWORD BP_FLAGS;  
```  
  
```csharp  
public enum enum_BP_FLAGS {   
   BP_FLAG_NONE            = 0x0000,  
   BP_FLAG_MAP_DOCPOSITION = 0x0001,  
   BP_FLAG_DONT_STOP       = 0x0002  
};  
```  
  
## <a name="members"></a>Üyeler  
 BP_FLAG_NONE  
 Kesme noktası bayrak belirtir.  
  
 BP_FLAG_MAP_DOCPOSITION  
 Hata ayıklama altyapısı (DE) belge konumunu kullanarak kesme noktası eşlemelisiniz belirtir. Bu, yalnızca Active Server Pages (ASP) gibi komut dosyası odaklı kaynak dosyalarında ayarlamak kesme noktaları için geçerlidir.  
  
 BP_FLAG_DONT_STOP  
 Kesme noktası hata ayıklama motoru tarafından işlenmesi gerektiğini, ancak hata ayıklama altyapısı sonuçta var. durması gerektiğini değil belirtir (diğer bir deyişle, bir [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) olay nesnesi değil gönderilmesi gerektiğini). Bu bayrak, öncelikle tracepoints ile kullanılmak üzere tasarlanmıştır.  
  
## <a name="remarks"></a>Açıklamalar  
 İçin kullanılan `dwFlags` üyesi [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) ve [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapıları.  
  
 Bu değerlerin Bitsel ile birleştirilebilir `OR`.  
  
## <a name="requirements"></a>Gereksinimler  
 Başlık: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Numaralandırmalar](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)   
 [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)   
 [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md)