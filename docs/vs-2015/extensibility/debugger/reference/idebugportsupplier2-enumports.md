---
title: IDebugPortSupplier2::EnumPorts | Microsoft Docs
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
- IDebugPortSupplier2::EnumPorts
helpviewer_keywords:
- IDebugPortSupplier2::EnumPorts
ms.assetid: 88b57fd2-eba1-44fa-bd34-cf2ad2b1ff87
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b39ee4d4a31bea6563681143a564eee71a1b3912
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49264120"
---
# <a name="idebugportsupplier2enumports"></a>IDebugPortSupplier2::EnumPorts
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bağlantı noktası sağlayıcısı tarafından sağlanan tüm bağlantı noktalarının bir listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT EnumPorts(   
   IEnumDebugPorts2** ppEnum  
);  
```  
  
```csharp  
int EnumPorts(   
   out IEnumDebugPorts2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md) sağlanan bağlantı noktalarının bir listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)

