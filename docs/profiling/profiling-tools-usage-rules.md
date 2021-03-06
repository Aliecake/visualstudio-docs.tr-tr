---
title: Profil Araçları Kullanım Kuralları | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: afa7db3b-8c1d-473a-81ac-24ede112a17f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cdd5733d950a0b7f2bdd2c433fa7bb91e9e02ec1
ms.sourcegitcommit: 42ea834b446ac65c679fa1043f853bea5f1c9c95
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/19/2018
ms.locfileid: "31582091"
---
# <a name="profiling-tools-usage-rules"></a>Profil Araçları Kullanım Kuralları
Profil oluşturma araçları kullanım kategorideki performans kuralları en verimli şekilde verileri toplamak için profil oluşturucu kullanmaya yönelik kılavuz sağlar.  
  
|||  
|-|-|  
|[DA0002: VSPerfCorProf.dll eksik](../profiling/da0002-vsperfcorprof-dll-is-missing.md)|Komut satırından profil oluşturma için eksik veri içeriyor olabilir [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] ikili dosyaları. Bu doğru ortam değişkenleri ayarlayarak değil neden olabilir.|  
|[DA0003: Pek çok çekirdek örneği](../profiling/da0003-many-kernel-samples.md)|İkili hedef yürütülmesi dışında oluşan çok sayıda profil örnekleri kaydedilmiş. Daha doğru veri toplamak için izleme metodunu kullanmayı düşünün.|  
|[DA0004: Yüksek işlemci kullanımı](../profiling/da0004-high-processor-usage.md)|Profil oluşturma verilerini Çalıştır profili oluşturma sırasında işlemci sürekli olarak meşgul önerir. Daha doğru verileri toplamak için örnekleme yöntemini kullanarak göz önünde bulundurun.|  
|[DA0008: Toplanan örnek az](../profiling/da0008-few-samples-collected.md)|Profil çalıştırmak toplanan örnek sayısını istatistiksel olarak önemli olmadığı yüksek değildi. Yeniden profil oluşturma ve uygulama için uzun süre çalışan göz önünde bulundurun. Ayrıca, verileri toplamak için izleme metodunu kullanarak göz önünde bulundurun.|  
|[DA0026: Aşırı çekirdek CPU süresi işleme](../profiling/da0026-excessive-kernel-cpu-time-processing.md)|Profil oluşturma çalışma zamanında önemli miktarda işlemci çekirdek modunda oluştu. Örnekleme süresi ölçü olarak kullanmak yerine ölçüm olarak sistem çağrıları kullanarak göz önünde bulundurun.|  
|[DA0029: Desteklenmeyen CLR Sürümü](../profiling/da0029-unsupported-clr-version.md)|Profili ikili bir sürümünü kullandığını [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] Profil Oluşturucu tarafından desteklenmiyor. Profil Oluşturucu raporları sembol adları çözümlenemiyor.|  
|[DA0030: Veritabanı projeleri için Katman Etkileşim ölçümlerini topla](../profiling/da0030-gather-tier-interaction-measurements-for-database-projects.md)|Çok sayıda yöntemleri çağrıları <xref:System.Data?displayProperty=fullName> ad alanı toplandı. Veritabanı çağrılarını hakkında verileri içerecek şekilde profilinizde katman etkileşim verileri toplama çalıştıran göz önünde bulundurun.|