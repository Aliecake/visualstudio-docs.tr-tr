---
title: JMC_CODE_SPEC | Microsoft Docs
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
- JMC_CODE_SPEC
helpviewer_keywords:
- JMC_CODE_SPEC structure
ms.assetid: d89498f1-4234-46d9-b4e2-abbcbca5068a
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: fa8a3009f30f3813f1236ca68ab8b45b68a95d5f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49287020"
---
# <a name="jmccodespec"></a>JMC_CODE_SPEC
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı, modül JustMyCode bilgilerini ayarlamak için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct _JMC_CODE_SPEC {  
   BOOL fIsUserCode;  
   BSTR bstrModuleName;  
} JMC_CODE_SPEC;  
```  
  
```csharp  
public struct JMC_CODE_SPEC {  
   public int    fIsUserCode;  
   public string bstrModuleName;  
};  
```  
  
## <a name="members"></a>Üyeler  
 fIsUserCode  
 Sıfır olmayan (`TRUE`) modülü kullanıcı kodu; göz önünde bulundurulması, aksi takdirde, sıfır (`FALSE`) modülü harici kod olarak işlem görecek ve değil ayıklanacak ise.  
  
 bstrModuleName  
 Söz konusu modülün adı.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı için tür yapıları listesi olarak geçirilen [SetJustMyCodeState](../../../extensibility/debugger/reference/idebugengine3-setjustmycodestate.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [SetJustMyCodeState](../../../extensibility/debugger/reference/idebugengine3-setjustmycodestate.md)

