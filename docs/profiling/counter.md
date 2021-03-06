---
title: Sayaç | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: aa4b4cdb-e6ea-433a-9579-56f3785e1385
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d09dc41f3726f21b432f39a504b5ea8b320bf107
ms.sourcegitcommit: 58052c29fc61c9a1ca55a64a63a7fdcde34668a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34749251"
---
# <a name="counter"></a>Sayaç
**Sayaç** seçeneği verileri işlemci (Donanım) performans sayaçlarını toplar.  
  
-   Örnekleme profili oluşturma yöntemi, kullanırken **sayaç** yongadaki performans sayacı ve örnekleme aralığı kullanmak için sayacı olaylarını sayısını belirtir. Örnekleme kullanırken, yalnızca bir sayaç belirtebilirsiniz.  
  
-   İzleme profili oluşturma yöntemi kullanırken, geçerli ve önceki koleksiyon olaylar arasındaki süreyi oluştu sayacı olay sayısı profil oluşturucu raporları ayrı alanlar olarak listelenir. Birden çok **sayaç** araçları kullanılırken seçenekleri belirtilebilir.  
  
 Her işlemci türü donanım performans sayaçları kendi kümesi vardır. Profil Oluşturucu neredeyse tüm işlemciler için ortak olan genel performans sayaçları kümesini tanımlar. Bilgisayarınızda genel ve işlemci özgü sayaçları listelemek için VSPerfCmd kullanın **QueryCounters** komutu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
VSPerfCmd.exe {/Launch:AppName | /Attach PID} /Counter:Name[,Reload[,FriendlyName]][Options]  
```  
  
```cmd  
VSPerfCmd.exe /Start:Method /Counter:Name[,Reload[,FriendlyName]][/Counter:Name[,Reload[,FriendlyName]]][Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Name`  
 Sayaç adı. VSPerfCmd.exe kullanmak **/QueryCounters** bilgisayardaki kullanılabilir sayaçlar adlarını listelemek için seçeneği.  
  
 `Reload`  
 Sayaç olaylarını örnekleme aralığı sayısı. İzleme yöntemi ile kullanmayın.  
  
 `FriendlyName`  
 (İsteğe bağlı) Yerine kullanılacak dizesi `Name` profil oluşturucu raporları ve görünümlerin sütun üst bilgileri.  
  
## <a name="required-options"></a>Gerekli seçenekler  
 Sayaç seçeneği, yalnızca aşağıdaki seçeneklerden biriyle kullanılabilir:  
  
 **Başlat:** `Trace`  
 Profil Oluşturucu izleme yöntemini kullanmak için başlatır.  
  
 **Başlat:** `AppName`  
 Belirtilen uygulama ve profil oluşturucu başlatır. Profil Oluşturucu örnekleme yöntemini kullanmak için başlatılmalıdır.  
  
 **Ekle:** `PID`  
 Profil Oluşturucu başlatır ve işlem kimliği tarafından belirtilen işlem ekler Profil Oluşturucu örnekleme yöntemini kullanmak için başlatılmalıdır.  
  
## <a name="example"></a>Örnek  
 Örnekleme yöntemi örneği 1000 her oluşumu uygulama NonHaltedCycles genel profil oluşturucu sayacın örnek gösterilmiştir.  
  
 İzleme yöntemi örneği L2InstructionFetches sayacı olaylarını toplamak için profil oluşturucu başlatma gösterilmiştir. L2InstructionFetches sayaç adı işlemciyi özeldir.  
  
```cmd  
; Sample Method Example  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /Counter:NonHaltedCycles,1000,"Non-Halted Cycles"  
  
;INSTRUMENTATION METHOD EXAMPLE  
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /Counter:L2InstructionFetches,,"L2 Cache Instruction Fetches"  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Hizmetleri](../profiling/command-line-profiling-of-services.md)