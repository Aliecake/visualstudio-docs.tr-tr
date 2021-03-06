---
title: IDebugProgramEngines2::EnumPossibleEngines | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgramEngines2::EnumPossibleEngines
helpviewer_keywords:
- IDebugProgramEngines2::EnumPossibleEngines
ms.assetid: 993d70a4-f6a5-4e47-a603-0b162b9fde00
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d30eb28398569aa3d14b4a7dd363abac785f352c
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31116080"
---
# <a name="idebugprogramengines2enumpossibleengines"></a>IDebugProgramEngines2::EnumPossibleEngines
Bu program ayıklayabilirsiniz tüm olası hata ayıklama altyapısı (DE) GUID'lerini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumPossibleEngines(   
   DWORD  celtBuffer,  
   GUID*  rgguidEngines,  
   DWORD* pceltEngines  
);  
```  
  
```csharp  
int EnumPossibleEngines(   
   uint      celtBuffer,  
   GUID[]    rgguidEngines,  
   ref DWORD pceltEngines  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celtBuffer`  
 [in] Döndürülecek DE GUID'ler sayısı. Bu da en büyük boyutunu belirtir `rgguidEngines` dizi.  
  
 `rgguidEngines`  
 [içinde out] Doldurulacak DE GUID'ler dizisi.  
  
 `pceltEngines`  
 [out] Döndürülen DE GUID'ler gerçek sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür [C++] `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` veya [C#] arabellek büyüklükte değilse 0x8007007A.  
  
## <a name="remarks"></a>Açıklamalar  
 Kaç tane motorları var olduğunu belirlemek için bu yöntemle kez çağrısı `celtBuffer` parametresi 0 olarak ayarlanmış ve `rgguidEngines` parametresi null bir değere ayarlayın. Bu döndürür `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` (0x8007007A için C#) ve `pceltEngines` parametresi gerekli arabellek boyutu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramEngines2](../../../extensibility/debugger/reference/idebugprogramengines2.md)