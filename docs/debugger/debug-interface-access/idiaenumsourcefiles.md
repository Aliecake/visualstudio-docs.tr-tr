---
title: Idiaenumsourcefiles | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumSourceFiles interface
ms.assetid: 5c0779a6-a2ea-408a-90da-ebdecf2b83c0
caps.latest.revision: "12"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dbcd3e50e1b53a56342b5ab344ec54180001fa80
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumsourcefiles"></a>IDiaEnumSourceFiles
Veri kaynağında bulunan çeşitli kaynak dosyaları sıralar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaEnumSourceFiles : IUknown  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaEnumSourceFiles`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Idiaenumsourcefiles::get__newenum](../../debugger/debug-interface-access/idiaenumsourcefiles-get-newenum.md)|Alır `IEnumVARIANT Interface` bu Sıralayıcı sürümü.|  
|[Idiaenumsourcefiles::get_Count](../../debugger/debug-interface-access/idiaenumsourcefiles-get-count.md)|Kaynak dosyalarının sayısını alır.|  
|[Idiaenumsourcefiles::Item](../../debugger/debug-interface-access/idiaenumsourcefiles-item.md)|Bir kaynak dosya yoluyla bir dizin alır.|  
|[Idiaenumsourcefiles::Next](../../debugger/debug-interface-access/idiaenumsourcefiles-next.md)|Kaynak dosyaları numaralandırma dizisinde belirtilen sayısını alır.|  
|[Idiaenumsourcefiles::Skip](../../debugger/debug-interface-access/idiaenumsourcefiles-skip.md)|Belirtilen sayıda kaynak dosyalarında bir numaralandırma sırasını atlar.|  
|[Idiaenumsourcefiles::reset](../../debugger/debug-interface-access/idiaenumsourcefiles-reset.md)|Bir numaralandırma sırasını başlangıç durumuna sıfırlar.|  
|[Idiaenumsourcefiles::Clone](../../debugger/debug-interface-access/idiaenumsourcefiles-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim çağırarak elde `QueryInterface` yöntemi bir [Idiatable](../../debugger/debug-interface-access/idiatable.md) nesnesi. Ayrıntılar için bkz.  
  
## <a name="example"></a>Örnek  
 Bu örnek edinmeyi gösteren `IDiaEnumSourceFiles` DIA oturum nesnesi tablolarda listesinden arabirimi. Kaynak dosya bilgilerine erişme ilişkin bir örnek için bkz: [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) arabirimi.  
  
```C++  
  
IDiaEnumSourceFiles* GetEnumSourceFiless(IDiaSession *pSession)  
{  
    IDiaEnumSourceFiles * pUnknown    = NULL;  
    REFIID                iid         = __uuidof(IDiaEnumSourceFiles);  
    IDiaEnumTables*       pEnumTables = NULL;  
    IDiaTable*            pTable      = NULL;  
    ULONG                 celt        = 0;  
  
    if (pSession->getEnumTables(&pEnumTables) != S_OK)  
    {  
        wprintf(L"ERROR - GetTable() getEnumTables\n");  
        return NULL;  
    }  
    while (pEnumTables->Next(1, &pTable, &celt) == S_OK && celt == 1)  
    {  
        // There is only one table that matches the given iid  
        HRESULT hr = pTable->QueryInterface(iid, (void**)&pUnknown);  
        pTable->Release();  
        if (hr == S_OK)  
        {  
            break;  
        }  
    }  
    pEnumTables->Release();  
    return pUnknown;  
}  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Başlık: Dia2.h  
  
 Kitaplığı: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiasession::findfile](../../debugger/debug-interface-access/idiasession-findfile.md)   
 [Idiasession::findlinesbylinenum](../../debugger/debug-interface-access/idiasession-findlinesbylinenum.md)   
 [Idiatable](../../debugger/debug-interface-access/idiatable.md)