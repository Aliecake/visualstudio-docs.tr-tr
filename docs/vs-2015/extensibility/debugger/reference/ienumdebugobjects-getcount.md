---
title: IEnumDebugObjects::GetCount | Microsoft Docs
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
- IEnumDebugObjects::GetCount
helpviewer_keywords:
- IEnumDebugObjects::GetCount method
ms.assetid: 9cbc5db4-03ae-479f-a664-13cad66ad210
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d9478ac84637bc76bed42488931b2457ab5aadf7
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49178028"
---
# <a name="ienumdebugobjectsgetcount"></a>IEnumDebugObjects::GetCount
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem numaralandırmada öğelerin sayısını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetCount(  
   [out] ULONG* pcelt  
);  
```  
  
```csharp  
int GetCount(  
   out uint pcelt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcelt`  
 [out] Numaralandırmada öğelerin sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem yalnızca ileri, kopyalama, atlama ve sıfırlama uygulanması gerektiğini belirten geleneksel COM numaralandırma arabiriminin bir parçası değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md)

