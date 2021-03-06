---
title: IDebugPortEx2::LaunchSuspended | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugPortEx2::LaunchSuspended
helpviewer_keywords:
- IDebugPortEx2::LaunchSuspended
ms.assetid: 34b2cf99-2e52-4757-8969-1d12ac517ec0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9f22afc50a1a2874d4853acbf9ff72cae622e790
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31114897"
---
# <a name="idebugportex2launchsuspended"></a>IDebugPortEx2::LaunchSuspended
Yürütülebilir bir dosyanın başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT LaunchSuspended(   
   LPCOLESTR        pszExe,  
   LPCOLESTR        pszArgs,  
   LPCOLESTR        pszDir,  
   BSTR             bstrEnv,  
   DWORD            hStdInput,  
   DWORD            hStdOutput,  
   DWORD            hStdError,  
   IDebugProcess2** ppPortProcess  
);  
```  
  
```csharp  
int LaunchSuspended(   
   string             pszExe,  
   string             pszArgs,  
   string             pszDir,  
   string             bstrEnv,  
   uint               hStdInput,  
   uint               hStdOutput,  
   uint               hStdError,  
   out IDebugProcess2 ppPortProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszExe`  
 [in] Başlatılacak yürütülebilir dosya adı. Bu bir tam yol veya göreli belirtilen çalışma dizini olarak olabilir `pszDir` parametresi.  
  
 `pszArgs`  
 [in] Yürütülebilir dosyaya geçirilecek bağımsız değişkenler. Bağımsız değişken yoksa null değeri olabilir.  
  
 `pszDir`  
 [in] Yürütülebilir dosya tarafından kullanılan çalışma dizinini adı. Çalışma dizini gerekliyse bir null değer olabilir.  
  
 `bstrEnv`  
 [in] Ek bir NULL Sonlandırıcı tarafından izlenen null ile sonlandırılmış dizeler ortam bloğu.  
  
 `hStdInput`  
 [in] Bir alternatif giriş akışı işleyin. Yeniden yönlendirme gerekli değilse 0 olabilir.  
  
 `hStdOutput`  
 [in] Alternatif çıkış akışına işleyin. Yeniden yönlendirme gerekli değilse 0 olabilir.  
  
 `hStdError`  
 [in] Diğer hata çıkış akışına işleyin. Yeniden yönlendirme gerekli değilse 0 olabilir.  
  
 `ppPortProcess`  
 [out] Döndürür bir [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) başlatılan işlemi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, BT'nin askıya şekilde işlemi ve herhangi bir kod çalıştırmayan belirmelidir. [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md) yöntemi işlemini sürdürmek için çağrılır.  
  
 Bir programı bir hata ayıklama altyapısı da başlatılabilir. Ayrıntılar için bkz [bir Program başlatma](../../../extensibility/debugger/launching-a-program.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)   
 [Program Başlatma](../../../extensibility/debugger/launching-a-program.md)