---
title: DiaAddressMapEntry | Microsoft Docs
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
- DiaAddressMapEntry enumeration
ms.assetid: 5d0ae226-981d-4541-a801-fc4993fe663b
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1ae4e4de3d3f81f335609201ce510b64a4b0f385
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49208936"
---
# <a name="diaaddressmapentry"></a>DiaAddressMapEntry
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir adres eşlemesi bir girişe açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
struct DiaAddressMapEntry {   
   DWORD rva,  
   DWORD rvaTo  
};  
```  
  
## <a name="elements"></a>Öğeleri  
 `rva`  
 A. görüntüdeki göreli sanal adres (RVA)  
  
 `rvaTo`  
 Göreli sanal adres `rva` görüntüde b eşlenir  
  
## <a name="remarks"></a>Açıklamalar  
 Bir adres eşlemesi tek bir görüntü düzeninden bir çeviri (A) için başka bir (B) sağlar. Bir dizi `DiaAddressMapEntry` ölçütü yapıları `rva` adres Haritası tanımlar.  
  
 Bir adresi çevrilecek `addrA`, bir adrese bir görüntüdeki `addrB`, görüntü B, aşağıdaki adımları gerçekleştirin:  
  
1.  Eşleme girişi için arama `e`, en büyük ile `rva` ya da eşit `addrA`.  
  
2.  Ayarlama `delta = addrA – e.rva`.  
  
3.  Ayarlama `addrB = e.rvaTo + delta`.  
  
 Bir dizi `DiaAddressMapEntry` yapıları geçirildiğinde [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: dia2.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)



