---
title: Idiasymbol::get_frontendminor | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSymbol::get_frontEndMinor method
ms.assetid: 40792153-827c-4859-be7c-6aa16d5abab6
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 30bfe092ed8454b14a7e26d77b375c75cabc0836
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolgetfrontendminor"></a>IDiaSymbol::get_frontEndMinor
Ön uç alt sürüm numarasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_frontEndMinor (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Front.end alt sürüm numarasını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliğin simge için kullanılabilir olup olmadığı anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Derleyici genellikle iki birincil öğeden oluşur: kaynak koduna bir ara forma ayrıştırma işleyen, ön uç (ayrıştırıcı) ve derlemeye Ara formun dönüştüren bir arka uç (Kod Oluşturucu). Seyrek için ön uç arka uçtan farklı bir sürüme sahip değil.  
  
 Bir ön uç veya arka uç sürüm numarası üç bölümden oluşur: \<ana >.\< İkincil >. \<Yapı > Burada \<ana > ana sürüm numarası \<küçük > ikincil sürüm numarası ve \<Yapı > yapı numarasıdır. Örneğin, 13.10.3077.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Başlık:|dia2.h|  
|Sürüm:|DIA SDK v7.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)