---
title: ProcessOn ve ProcessOff | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: d3dc6a7e-bc0f-48a6-a4ec-f386348bb296
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b94001c13f5925107cecb49936ecdc5fb1e73514
ms.sourcegitcommit: 34f7d23ce3bd140dcae875b602d5719bb4363ed1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35254364"
---
# <a name="processon-and-processoff"></a>ProcessOn ve ProcessOff
VSPerfCmd.exe **ProcessOff** ve **ProcessOn** subcommands duraklatıp belirtilen işlem için bir komut satırı profil oluşturma oturumu profil oluşturma. **ProcessOff** profil oluşturma işlemi durdurur ve **ProcessOn** profil oluşturma işlemini başlatır.  
  
 Çoğu durumda, belirttiğiniz **ProcessOn** veya **ProcessOff** yalnızca seçeneği bir VSPerfCmd.exe olarak komut satırı, ancak bunlar da birleştirilebilir ile **GlobalOn**, **GlobalOff**, **ThreadOn**, ve **ThreadOff** subcommands.  
  
 **ProcessOn** ve **ProcessOff** subcommands etkileşimde **GlobalOn** ve **GlobalOff** veri denetimi komutları komut satırı profil oluşturma oturumu tüm işlemler için koleksiyonda ve **ThreadOn** ve **ThreadOff** belirtilen bir iş parçacığı için veri toplama denetim komutları.  
  
 **ProcessOff** ve **ProcessOn** subcommands profil oluşturucu API işlevleri tarafından yönetilebilir işlem başlatma/durdurma sayısı da etkiler.  
  
-   **ProcessOff** hemen işlem başlatma/durdurma sayısı 0 olarak ayarlar ve bu nedenle profil duraklatır.  
  
-   **ProcessOn** hemen işlem başlatma/durdurma sayısı 1'e ayarlar ve bu nedenle sürdürür profil oluşturma.  
  
 Daha fazla bilgi için bkz: [profil oluşturma araçları API'leri](../profiling/profiling-tools-apis.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
VSPerfCmd.exe /{ProcessOff|ProcessOn}:PID [Options]  
  
```  
  
#### <a name="parameters"></a>Parametreler  
 `PID`  
 Tamsayı başlatmak veya durdurmak için işlem tanıtıcısı. İşlem kimlikleri listelenir **işlem** sekmesi Windows Görev Yöneticisi'nin.  
  
## <a name="required-subcommands"></a>Gerekli komutları  
 Yok.  
  
## <a name="valid-subcommands"></a>Geçerli komutları  
 **ProcessOn** ve **ProcessOff** de aşağıdaki komutları içeren komut satırları belirtilebilir.  
  
 **Başlat:** `Method`  
 Komut satırı profil oluşturma oturumu başlatır ve belirtilen profil oluşturma yöntemini ayarlar.  
  
 **Başlat:** `AppName`  
 Belirtilen uygulamayı başlatır ve profil oluşturma örnekleme yöntemi ile başlar.  
  
 **Ekle:** `PID`  
 Belirtilen işlem profil başlar.  
  
 **GlobalOff**&#124;**GlobalOn**  
 Durdurur veya bir komut satırı profil oluşturma oturumu tüm işlemler için profil başlatır.  
  
 {**ThreadOff**&#124;**ThreadOn**}**:**`TID`  
 Durdurur veya belirtilen iş parçacığı (yalnızca izleme metodunu) için profil oluşturma başlatır.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, **ProcessOff** alt, uygulama başlangıcından profil oluşturma verilerini toplamak için kullanılır.  
  
```cmd  
; Initialize the profiler.  
VSPerfCmd.exe /Start:Trace /Output:Instrument.vsp   
; Start the instrumented application.  
; Stop profiling the process after startup.  
VSPerfCmd.exe /ProcessOff:12345  
; Shut down the target application.  
; Close the profiler.  
VSPerfCmd /Shutdown  
  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Hizmetleri](../profiling/command-line-profiling-of-services.md)