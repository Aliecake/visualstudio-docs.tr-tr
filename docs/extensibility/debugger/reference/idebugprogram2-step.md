---
title: IDebugProgram2::Step | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::Step
helpviewer_keywords:
- IDebugProgram2::Step
ms.assetid: e4c2ffce-9810-4088-8162-eac9ef04f2a9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 10685adb27c9bf2e962beccb7e68f19ce5c27eeb
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31118563"
---
# <a name="idebugprogram2step"></a>IDebugProgram2::Step
Bir adımı gerçekleştirir.  
  
> [!NOTE]
>  Bu yöntem kullanım dışıdır. Kullanım [adım](../../../extensibility/debugger/reference/idebugprocess3-step.md) yöntemi yerine.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Step(   
   IDebugThread2*  pThread,  
   STEPKIND        sk,  
   STEPUNIT        step  
);  
```  
  
```csharp  
int Step(   
   IDebugThread2  pThread,  
   enum_STEPKIND  sk,  
   enum_STEPUNIT  step  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pThread`  
 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) adım adım iş parçacığı temsil eden nesne.  
  
 `sk`  
 [in] Arasında bir değer [STEPKIND](../../../extensibility/debugger/reference/stepkind.md) numaralandırma adım türünü belirtir.  
  
 `step`  
 [in] Arasında bir değer [STEPUNIT](../../../extensibility/debugger/reference/stepunit.md) (örneğin, deyimi veya yönerge) adım birimini belirtir numaralandırması.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Durumunda herhangi bir iş parçacığı eşitleme veya iş parçacıkları arasında iletişimi, belirli bir iş parçacığı adımlarken programı başka bir iş parçacığı çalıştırmanız gerekir.  
  
> [!WARNING]
>  Bir durdurma veya bir anında (zaman uyumlu) olayın göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) bu çağrıyı; işlenirken hata ayıklayıcı aksi kilitlenebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [Olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)