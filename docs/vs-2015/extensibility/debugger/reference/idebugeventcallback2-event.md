---
title: IDebugEventCallback2::Event | Microsoft Docs
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
- IDebugEventCallback2::Event
helpviewer_keywords:
- IDebugEventCallback2::Event
ms.assetid: e5a3345b-d460-4e40-8f5b-3111c56a2ed9
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 64bd10dffeee90bc1f74e120eee1d831659390df
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49246992"
---
# <a name="idebugeventcallback2event"></a>IDebugEventCallback2::Event
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama olaylarını bildirim gönderir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Event(   
   IDebugEngine2*  pEngine,  
   IDebugProcess2* pProcess,  
   IDebugProgram2* pProgram,  
   IDebugThread2*  pThread,  
   IDebugEvent2*   pEvent,  
   REFIID          riidEvent,  
   DWORD           dwAttrib  
);  
```  
  
```csharp  
int Event(   
   IDebugEngine2  pEngine,  
   IDebugProcess2 pProcess,  
   IDebugProgram2 pProgram,  
   IDebugThread2  pThread,  
   IDebugEvent2   pEvent,  
   ref Guid       riidEvent,  
   uint           dwAttrib  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pEngine`  
 [in] Bir [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) bu olayı gönderirken hata ayıklama altyapısı (DE) temsil eden nesne. Bir DE out bu parametreyi doldurmak için gereklidir.  
  
 `pProcess`  
 [in] Bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) olayın gerçekleştiği işlemini temsil eden nesne. Bu parametre oturum hata ayıklama Yöneticisi (SDM) tarafından doldurulur. Bir DE, bu parametre için null değeri her zaman geçirir.  
  
 `pProgram`  
 [in] Bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) programın bu olay gerçekleştiği temsil eden nesne. Çoğu olaylar için bu parametre null bir değer değil.  
  
 `pThread`  
 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) bu olay gerçekleştiği iş parçacığını temsil eden nesne. Olayları durdurmak için yığın çerçevesinin bu parametresinden alındıkça Bu parametre bir null değer olamaz.  
  
 `pEvent`  
 [in] Bir [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) hata ayıklama olayı temsil eden nesne.  
  
 `riidEvent`  
 [in] Hangi olay arabirimi almak için tanımlayan GUID `pEvent` parametresi.  
  
 `dwAttrib`  
 [in] Bayraklarının bir birleşimi [EVENTATTRIBUTES](../../../extensibility/debugger/reference/eventattributes.md) sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem çağrılırken `dwAttrib` parametresi, döndürülen değer eşleşmelidir [GetAttributes](../../../extensibility/debugger/reference/idebugevent2-getattributes.md) olay nesne üzerinde adlandırıldığı gibi yöntemi geçirilen `pEvent` parametresi.  
  
 Bir olay zaman uyumsuz olup olmamasına bakılmaksızın tüm hata ayıklama olayları zaman uyumsuz olarak gönderilir. Bir DE bu yöntemini çağırdığında, yalnızca olay alındı olmadığını dönüş değeri olay olup olmadığını işlendi, göstermez. Aslında, bu yöntem döndürüldüğünde çoğu durumda, olay işlenmedi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [EVENTATTRIBUTES](../../../extensibility/debugger/reference/eventattributes.md)

