---
title: Idiastackframe::get_registervalue | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaStackFrame::get_registerValue method
ms.assetid: cbe3d8ac-319a-40ac-bc3e-4eb81b2d7807
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a454beb98fc8579bf625dbdb64db1cf60f8dd50a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idiastackframegetregistervalue"></a>IDiaStackFrame::get_registerValue
Belirtilen bir kayıt değeri yığın çerçevesinde depolanmış olarak alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_registerValue(  
   ULONG      registerIndex,  
   ULONGLONG *pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `registerIndex`  
 [in] Aşağıdakilerden birini [CV_HREG_e numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md) numaralandırma değerleri.  
  
 `pRetVal`  
 [out] Kayıt defterinde depolanan değer.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde, hata kodunu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiastackframe](../../debugger/debug-interface-access/idiastackframe.md)   
 [CV_HREG_e numaralandırması](../../debugger/debug-interface-access/cv-hreg-e.md)