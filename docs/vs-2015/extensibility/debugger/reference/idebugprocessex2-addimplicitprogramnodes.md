---
title: IDebugProcessEx2::AddImplicitProgramNodes | Microsoft Docs
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
- IDebugProcessEx2::AddImplicitProgramNodes
helpviewer_keywords:
- IDebugProcessEx2::AddImplicitProgramNodes method
ms.assetid: 8b491b00-f9e7-45b3-9115-fe58c3464289
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 34c533a2bc20e0e32c981208ce95917ec9e6473e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49297030"
---
# <a name="idebugprocessex2addimplicitprogramnodes"></a>IDebugProcessEx2::AddImplicitProgramNodes
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, belirtilen her hata ayıklama altyapısı (DE) için bir program düğüm ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT AddImplicitProgramNodes(  
   REFGUID guidLaunchingEngine,  
   GUID*   rgguidSpecificEngines,  
   DWORD   celtSpecificEngines  
);  
```  
  
```csharp  
int AddImplicitProgramNodes(  
   ref Guid guidLaunchingEngine,  
   Guid[]   rgguidSpecificEngines,  
   uint     celtSpecificEngines  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidLaunchingEngine`  
 [in] `GUID` , Program başlatmak için kullanılacak olan (ve kendi program düğümleri eklemek için kabul edilir) bir DE.  
  
 `rgguidSpecificEngines`  
 [in] Dizi `GUID`DEs hangi programın düğümleri eklenir, s.  
  
 `celtSpecificEngines`  
 [in] Sayısını `GUID`s'te `rgguidSpecificEngines` dizisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [Program düğümleri](../../../extensibility/debugger/program-nodes.md) her DE listelenen için eklenecek `rgguidSpecificEngines`— başlatma altyapısı hariç (belirtildiği `guidLaunchingEngine`), bir program başlattığında kendi program düğümü eklemek için kabul.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramEx2](../../../extensibility/debugger/reference/idebugprogramex2.md)   
 [Program Düğümleri](../../../extensibility/debugger/program-nodes.md)

