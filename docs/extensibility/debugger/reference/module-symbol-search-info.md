---
title: MODULE_SYMBOL_SEARCH_INFO | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- MODULE_SYMBOL_SEARCH_INFO
helpviewer_keywords:
- MODULE_SYMBOL_SEARCH_INFO structure
ms.assetid: 432aff03-08a5-4c5a-b2d5-e212090fc70a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: bb62fb0a830c8c3bf6bb9b7ca186e001573b7b37
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31126246"
---
# <a name="modulesymbolsearchinfo"></a>MODULE_SYMBOL_SEARCH_INFO
Arandığını sembol arama yolları hakkındaki durum bilgilerini içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef struct _tagSYMBOL_SEARCH_INFO  
{  
   SYMBOL_SEARCH_INFO_FIELDS dwValidFields;  
   BSTR                      bstrVerboseSearchInfo;  
} MODULE_SYMBOL_SEARCH_INFO;  
```  
  
```csharp  
public struct MODULE_SYMBOL_SEARCH_INFO {  
   public uint   dwValidFields;  
   public string bstrVerboseSearchInfo;  
}  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwValidFields`  
 Bayraklarını bileşimini [SYMBOL_SEARCH_INFO_FIELDS](../../../extensibility/debugger/reference/symbol-search-info-fields.md) bu yapısı içinde açıklanan arama bilgileri türünü belirtme numaralandırması.  
  
 `bstrVerboseSearchInfo`  
 Arama yolu ve tek bir dize halinde birleştirilmiş sonuçları.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı çağrısından döndürülen [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) yöntemi.  
  
 Varsa `bstrVerboseSearchInfo` alanı boş değil ve ardından arama yolları ve arama sonuçlarını listesini içerir. Listenin sonucu tarafından izlenen bir üç nokta ("..."), ve ardından bir yolu biçimlendirilir. Birden fazla yol sonuç çifti varsa, her bir çifti "\r\n" (satır-return/satır besleme) çifti tarafından ayrılır. Desen şöyle görünür:  
  
 \<yolu >... \<sonuç > \r\n\<yolu >... \<sonuç > \r\n\<yolu >... \<sonuç >  
  
 Son girişi \r\n sırası yok unutmayın.  
  
 Olası işte `bstrVerboseSearchInfo` standart dışı gönderilen dize.  
  
 `c:\symbols\user32.pdb... File not found.`  
  
 `c:\winnt\symbols\user32.pdb... Version does not match.`  
  
 `\\symbols\symbols\user32.dll\0a8sd0ad8ad\user32.pdb... Symbols loaded.`  
  
## <a name="requirements"></a>Gereksinimler  
 Başlık: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimleri](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)