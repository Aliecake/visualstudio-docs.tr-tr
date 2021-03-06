---
title: Performans oturumlarını yapılandırma | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- common tasks, performance
- common tasks, profiling tools
- profiling tools, common tasks
- performance, gathering data
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: df9ba88809303e5d093c4fb644e4b936dfbcf1f0
ms.sourcegitcommit: 0aafcfa08ef74f162af2e5079be77061d7885cac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34692206"
---
# <a name="configure-performance-sessions"></a>Performans oturumlarını yapılandırma
Kullanarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, çok çeşitli çok sayıda uygulama türleri için performans verilerini toplayabilir. Bu bölümde Performans oturumunu ve hedef ikili performans Wizardand özelliklerini ilginizi çeken verileri toplamak için profil oluşturma araçları yapılandırmak için nasıl kullanılacağını gösterir. Profil oluşturma araçları yapılandırma özellikleri de profil çalıştırılmasıyla toplanan veri miktarını denetlemek için kullanılabilir. Daha fazla bilgi için bkz: [denetim veri toplama](../profiling/controlling-data-collection.md).  
  
> [!NOTE]
>  Çoğu durumda, performans Sihirbazı'nı varsayılan özelliklerini kullanarak profil oluşturma verileri toplama etkili bir yoldur. Daha fazla bilgi için bkz: [yeni başlayanlar Kılavuzu performans profili oluşturma için](../profiling/beginners-guide-to-performance-profiling.md) ve [Başlarken](../profiling/getting-started-with-performance-tools.md).  
  
## <a name="common-tasks"></a>Ortak görevler
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Temel profil oluşturma seçenekleri ayarlayın:** yapılandırmanız gerekir [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] Microsoft Simge sunucusunu kullanmak için. Bu simge, Windows ve diğer Microsoft uygulamaları geçerli sürümü için işlevi ve parametre adları gibi erişebildiğinizden emin hale getirir. Profil Araçları ve profil oluşturma veri dosyalarıyla adları sistem izinleri gibi bir profil oluşturma oturumu başlatılmadan önce diğer genel seçenekleri de belirtebilirsiniz.|-   [Nasıl yapılır: başvuru Windows sembol bilgileri](../profiling/how-to-reference-windows-symbol-information.md)<br />-   [Nasıl yapılır: sembol bilgilerini serileştirme](../profiling/how-to-serialize-symbol-information.md)<br />-   [Nasıl yapılır: geçerli oturum ayarlayın](../profiling/how-to-set-the-current-session.md)<br />-   [Nasıl yapılır: izinleri ayarla](../profiling/how-to-set-permissions.md)<br />-   [Nasıl yapılır: performans veri dosyası adlandırma seçeneklerini ayarlama](../profiling/how-to-set-performance-data-file-name-options.md)|  
|**Toplamak istediğiniz verileri belirtin:** profil oluşturma oturumu yapılandırmak için kullandığınız yordam profil oluşturmayı istediğiniz hedef uygulama türü ve toplamak istediğiniz performans veri türüne bağlıdır.|-   [Nasıl yapılır: Koleksiyon yöntemleri seçme](../profiling/how-to-choose-collection-methods.md)<br />-   [Örnekleme kullanarak performans istatistikleri toplama](../profiling/collecting-performance-statistics-by-using-sampling.md)<br />-   [.NET bellek ayırma ve yaşam süresi verilerini topla](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [İzleme kullanarak ayrıntılı zamanlama verileri toplama](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)<br />-   [Nasıl yapılır: web sayfalarında profili JavaScript kodu](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [İş parçacığı ve işlem eşzamanlılık verileri toplama](../profiling/collecting-thread-and-process-concurrency-data.md)<br />-   [Ek performans verileri toplama](../profiling/collecting-additional-performance-data.md)|  
|**Gelişmiş yapılandırma seçenekleri ayarlayın:** ortak dil çalışma zamanı (CLR) birden fazla sürümünü yükleme .NET Framework uygulamaları profili oluşturduğunuzda, profil için hangi sürümün belirtebilirsiniz. Bir performans oturumunda birden çok .exe dosyaları varsa, ikili dosyaları başlangıç sırasını ayarlayabilirsiniz.|-   [Nasıl yapılır: .NET Framework çalışma zamanı belirtin](../profiling/how-to-specify-the-dotnet-framework-runtime.md)<br />-   [Nasıl yapılır: başlatmak için ikili belirtin](../profiling/how-to-specify-the-binary-to-start.md)|  
  
## <a name="related-sections"></a>İlgili bölümler  
 [Veri toplamayı denetleme](../profiling/controlling-data-collection.md)  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Performans Gezgini](../profiling/performance-explorer.md)