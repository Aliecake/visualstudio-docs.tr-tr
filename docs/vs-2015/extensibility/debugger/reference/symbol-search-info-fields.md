---
title: SYMBOL_SEARCH_INFO_FIELDS | Microsoft Docs
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
- SYMBOL_SEARCH_INFO_FIELDS
helpviewer_keywords:
- SYMBOL_SEARCH_INFO_FIELDS enumeration
ms.assetid: bce35af0-722d-46d4-afa6-eaae598c51ff
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 30b7f452b78d9ab446adccab61893af07473098c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49287826"
---
# <a name="symbolsearchinfofields"></a>SYMBOL_SEARCH_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Sembol bilgilerini almak için türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
typedef DWORD SYMBOL_SEARCH_INFO_FIELDS;  
```  
  
```csharp  
public enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
  
```  
  
## <a name="members"></a>Üyeler  
 SSIF_NONE  
 Bayrak gösterir  
  
 SSIF_VERBOSE_SEARCH_INFO  
 Tüm simgeleri bulmak için kullanılan yolların arama döndürür  
  
## <a name="remarks"></a>Açıklamalar  
 Bu bayraklar parametresi olarak geçirilir [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) döndürülen bilgi miktarını belirlemek için yöntemi.  
  
> [!NOTE]
>  Şu anda yalnızca `SSIF_VERBOSE_SEARCH_INFO` desteklenir, ve olarak belirtilmelidir `dwFlags` parametresi `IDebugModule3::GetSymbolInfo`. Diğer tüm değerler, bir hata döndürülür.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)

