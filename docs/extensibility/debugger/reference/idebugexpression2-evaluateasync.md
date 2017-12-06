---
title: IDebugExpression2::EvaluateAsync | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugExpression2::EvaluateAsync
helpviewer_keywords: IDebugExpression2::EvaluateAsync
ms.assetid: 848fe6cb-0759-42f2-890b-d2b551c527d6
caps.latest.revision: "15"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 371dbeff80ce424cbb37aad6be4265aeec437cd0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="idebugexpression2evaluateasync"></a>IDebugExpression2::EvaluateAsync
Bu yöntem ifade zaman uyumsuz olarak değerlendirilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EvaluateAsync (   
   EVALFLAGS             dwFlags,  
   IDebugEventCallback2* pExprCallback  
);  
```  
  
```csharp  
int EvaluateAsync(  
   enum_EVALFLAGS       dwFlags,   
   IDebugEventCallback2 pExprCallback  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFlags`  
 [in] Bayraklarını bileşimini [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) ifade değerlendirme denetim numaralandırması.  
  
 `pExprCallback`  
 [in] Bu parametre bir null değer her zaman olur.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Tipik hata kodu verilmiştir:  
  
|Hata|Açıklama|  
|-----------|-----------------|  
|E_EVALUATE_BUSY_WITH_EVALUATION|Başka bir deyim şu anda değerlendiriliyor ve eşzamanlı ifade değerlendirme desteklenmiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendirme başlatıldıktan hemen sonra bu yöntem döndürmelidir. İfade başarıyla değerlendirildiğinde bir [IDebugExpressionEvaluationCompleteEvent2](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) gönderilmelidir [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) aracılığıyla sağlanan gibi olay geri çağırma [Ekle ](../../../extensibility/debugger/reference/idebugprogram2-attach.md) veya [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte basit bir için bu yöntemi uygulaması gösterilmektedir `CExpression` uygulayan nesne [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) arabirimi.  
  
```cpp  
HRESULT CExpression::EvaluateAsync(EVALFLAGS dwFlags,  
                                   IDebugEventCallback2* pExprCallback)  
{  
    // Set the aborted state to FALSE  
    // in case the user tries to redo the evaluation after aborting.  
    m_bAborted = FALSE;  
    // Post the WM_EVAL_EXPR message in the message queue of the current thread.  
    // This starts the expression evaluation on a background thread.  
    PostThreadMessage(GetCurrentThreadId(), WM_EVAL_EXPR, 0, (LPARAM) this);  
    return S_OK;  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)   
 [IDebugExpressionEvaluationCompleteEvent2](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md)   
 [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)