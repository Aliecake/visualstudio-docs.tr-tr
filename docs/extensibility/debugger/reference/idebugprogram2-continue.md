---
title: IDebugProgram2::Continue | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::Continue
helpviewer_keywords:
- IDebugProgram2::Continue
ms.assetid: e5a6e02a-d21b-4a03-a034-e8de1f71ce2e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f52fccf640cca32d4291b3d6fb8626c38370ded3
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31116753"
---
# <a name="idebugprogram2continue"></a>IDebugProgram2::Continue
Bu program durdurulmuş bir durumdan çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) korunur, ve programı yeniden yürütme.  
  
> [!NOTE]
>  Bu yöntem kullanım dışıdır. Kullanım [devam](../../../extensibility/debugger/reference/idebugprocess3-continue.md) yöntemi yerine.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Continue(   
   IDebugThread2* pThread  
);  
```  
  
```csharp  
int Continue(   
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pThread`  
 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) iş parçacığı temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, kaç tane program ayıklanacak veya program durdurma olayı oluşturan bağımsız olarak bu programı'nda çağrılır. Uygulama, önceki yürütme durumu (örneğin, bir adım) korumak ve hiçbir zaman önceki yürütülmesinin tamamlamadan önce durmuş gibi sorgulamanıza yürütme devam gerekir. Diğer bir deyişle, bu program bir iş parçacığında adım üzerinde işlem yapılması ve başka bir programı durduruldu ve ardından bu yöntemi çağrıldı için durduruldu, program özgün adım üzerinden işlemi tamamlamanız gerekir.  
  
> [!WARNING]
>  Bir durdurma veya bir anında (zaman uyumlu) olayın göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) bu çağrıyı; işlenirken hata ayıklayıcı aksi kilitlenebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [Olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)