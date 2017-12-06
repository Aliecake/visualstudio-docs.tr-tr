---
title: IDiaSymbol::findChildrenExByAddr | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSymbol::findChildrenExByAddr
ms.assetid: c1e7885d-2d15-4529-9ac2-32dd22efe31c
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a8f5dbd7a6ad06ba10690e92042c9722eca5c99e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolfindchildrenexbyaddr"></a>IDiaSymbol::findChildrenExByAddr
Belirtilen bir adres geçerli öğenin alt öğelerine simgenin alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findChildrenExByAddr (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   DWORD             address,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `symtag`  
 [in] ' Da tanımlandığı gibi alınması için alt simge etiketleri belirtir [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md). Kümesine `SymTagNull` alınması tüm alt öğeleri için.  
  
 `name`  
 [in] Alınacak öğenin alt öğelerine adını belirtir. Kümesine `NULL` alınması tüm alt öğeleri için.  
  
 `compareFlags`  
 [in] Ad eşleştirme için uygulanacak karşılaştırma seçeneklerini belirtir. Gelen değerleri [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md) numaralandırma tek başına veya birlikte kullanılabilir.  
  
 `address`  
 [in] Simgenin adresi.  
  
 `ppResult`  
 [out] Döndürür bir [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md) alt simge listesini içeren nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` simgenin en az bir alt bulunamadı ya da döndürür `S_FALSE` alt öğesi bulundu; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Döndürülen yerel semboller dinamik aralık bilgileri içerir.  
  
## <a name="requirements"></a>Gereksinimler  
 Başlık: Dia2.h  
  
 Kitaplığı: diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md)   
 [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [Idiasession::findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md)