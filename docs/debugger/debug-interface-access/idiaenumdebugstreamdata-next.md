---
title: Idiaenumdebugstreamdata::Next | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreamData::Next method
ms.assetid: 114171dd-38fd-4bd7-a702-8ff887ffc99b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 81e816edd5b93ffdfec46d36d9aabba154ab035d
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31458700"
---
# <a name="idiaenumdebugstreamdatanext"></a>IDiaEnumDebugStreamData::Next
Belirtilen bir numaralandırılmış dizisi kayıtlarının sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Next (   
   ULONG  celt,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[],  
   ULONG* pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Alınacak kayıt sayısı.  
  
 cbData  
 [in] Veri arabelleğinin bayt cinsinden boyutu.  
  
 pcbData  
 [out] Döndürülen bayt sayısını döndürür. Varsa `data` NULL ise `pcbData` tüm kayıtları istenen bayt veri kullanılabilir toplam sayısını içerir.  
  
 veri]  
 [out] Hata ayıklama akışı kayıt veri ile doldurulacak olan bir arabellek.  
  
 pceltFetched  
 [içinde out] Kayıt sayısı döndürür `data`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`. Döndürür `S_FALSE` olması durumunda daha fazla kayıt yok. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumdebugstreamdata](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)   
 [IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)