---
title: Idialoadcallback::notifydebugdir | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaLoadCallback::NotifyDebugDir method
ms.assetid: bd04e2f6-0dbf-4742-a556-96f2cd99aa19
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ecb14b340df745ebb06d4bf7da571916e0ae6760
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49262398"
---
# <a name="idialoadcallbacknotifydebugdir"></a>IDiaLoadCallback::NotifyDebugDir
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama dizini .exe dosyasında bulundu çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT NotifyDebugDir (   
   BOOL  fExecutable,  
   DWORD cbData,  
   BYTE  data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fExecutable`  
 [in] `TRUE` hata ayıklama dizini, yürütülebilir bir dosya (.dbg Dosya yerine) salt okunur ise.  
  
 `cbData`  
 [in] Hata ayıklama dizininde bulunan verileri baytlık sayısı.  
  
 `data[]`  
 [in] Oturum hata ayıklama dizini doldurulmuş bir dizi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş kodu genellikle göz ardı edilir.  
  
## <a name="remarks"></a>Açıklamalar  
 [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yürütülebilir dosya işlenirken bir hata ayıklama dizini bulduğunda, bu geri çağırma yöntemini çağırır.  
  
 Bu yöntem, hata ayıklama bilgisi .pdb dosyasında bulunan dışındaki desteklemek için istemcinin ters mühendislik hata ayıklama ve/veya yürütülebilir dosya ihtiyacını ortadan kaldırır. Bu verilerle istemcide kullanılabilir hata ayıklama bilgilerinin türünü ve bu yürütülebilir dosya veya .dbg dosyasında bulunan tanıyabilirsiniz.  
  
 Çoğu istemci çünkü bu geri çağırma gerekmeyeceğinden `IDiaDataSource::loadDataForExe` yöntemi .pdb hem .dbg dosyaları sembolleri sunmak için gerekli olduğunda şeffaf bir şekilde açılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idialoadcallback2](../../debugger/debug-interface-access/idialoadcallback2.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)



