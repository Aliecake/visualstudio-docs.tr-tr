---
title: IDiaSymbol::get_liveRangeStartAddressOffset | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSymbol::get_liveRangeStartAddressOffset
ms.assetid: f5b28914-0a14-4b22-8259-59d7f97ee610
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3e0755705c92d998facc5c4687d5f99866dee8a9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolgetliverangestartaddressoffset"></a>IDiaSymbol::get_liveRangeStartAddressOffset
Yerel simgenin geçerli aralığın başlangıç adresi uzaklık bölümünü döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_liveRangeStartAddressOffset (   
   DWORD* offset  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `offset`  
 [out] Başlangıç adresi aralığı uzaklık bölümünü döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
> [!NOTE]
>  Döndürülen hata kodu simgenin dinamik aralık bilgileri yok anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Uzaklık ve bölüm biçimlendirilmiş simgenin geçerli olduğu aralığının başlangıcını adresidir.  
  
 Adresin bölüm bölümünü almak için [IDiaSymbol::get_liveRangeStartAddressSection](../../debugger/debug-interface-access/idiasymbol-get-liverangestartaddresssection.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Başlık: Dia2.h  
  
 Kitaplığı: diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)