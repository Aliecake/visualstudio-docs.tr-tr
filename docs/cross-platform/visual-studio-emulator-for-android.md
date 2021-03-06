---
title: Android için Visual Studio öykünücüsü | Microsoft Docs
ms.custom: ''
ms.date: 07/03/2018
ms.technology: vs-ide-mobile
ms.topic: conceptual
ms.assetid: 80f0104f-a4db-44dd-bd55-37bb67776c62
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d6799bc7d3a2a79fadfb6d0535b8ccbbf0b0cffd
ms.sourcegitcommit: 1ab675a872848c81a44d6b4bd3a49958fe673c56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44283672"
---
# <a name="visual-studio-emulator-for-android"></a>Android için Visual Studio Öykünücüsü

Android için Visual Studio öykünücüsü Android cihaz öykünen bir masaüstü uygulamasıdır. Bu, hata ayıklama ve fiziksel bir cihaz olmadan Android uygulamalarını test etmek için sanallaştırılmış bir ortam sağlar. Ayrıca, uygulama prototipleri için yalıtılmış bir ortam sağlar.  

> [!IMPORTANT]
> Çoğu senaryoda, Google Android öykünücüsü Android için Visual Studio öykünücüsü'nün yerine kullanılması önerilir:
> - Android için Visual Studio öykünücü, Visual Studio 2015 tarihinden sonra desteklenmiyor.
> - Öykünücü görüntüleri Android 6.0 sürümünden daha sonra Android için Visual Studio öykünücüsü kullanılabilir değil.
> - Google Android öykünücüsü artık destekliyor [Hyper-V](https://docs.microsoft.com/xamarin/android/get-started/installation/android-emulator/hardware-acceleration#hyper-v).
> - Apache Cordova için Visual Studio Araçları, Google Android öykünücüsü ile çalışır. Daha fazla bilgi için [Apache Cordova uygulamanızı Android'de çalıştırma](/visualstudio/cross-platform/tools-for-cordova/run-your-app/run-app-android#google-android-emulator) (Bu makalede açıklandığı gibi Hyper-V devre dışı bırakmak zorunda unutmayın).
>
> Google Android öykünücüsü'nü ve yapılandırma hakkında daha fazla bilgi için bkz. [Android Emulator Kurulumu](https://docs.microsoft.com/xamarin/android/get-started/installation/android-emulator/).
  
 Android için Visual Studio öykünücüsü, gerçek bir cihaz için karşılaştırılabilir performans sağlayacak şekilde tasarlanmıştır. Ancak, uygulamanızı yayımlamadan önce fiziksel bir cihazda uygulamanızı test etmenizi öneririz.  
  
 Android platformları, ekran çözünürlükleri ve Android için Visual Studio öykünücüsü tarafından desteklenen diğer donanım özellikleri her bir benzersiz bir cihaz profili uygulamanızı test edebilirsiniz.
  
##  <a name="Installing"></a> Yükleme ve kaldırma  
 Yükleme  
  
 Android için Visual Studio öykünücü, Visual Studio'da platformlar arası araçları, bir bileşenidir ve platformlar arası mobil geliştirme, daha sonra ortak Araçlar ve yazılım geliştirme setleri seçtiğinizde, özel bir Visual Studio Kurulumu sırasında yüklenir, ve ardından Visual Studio öykünücüsü Android için.  
  
 Kaldırma  
  
 Denetim Masası'ndaki Program Ekle/Kaldır'ı kullanarak Android için Visual Studio öykünücü kaldırabilirsiniz.  
  
> [!NOTE]
>  Visual Studio'nun öykünücü kaldırmaz. Öykünücü ayrı olarak kaldırmanız gerekir.  
  
 Android için Visual Studio öykünücü kaldırdığınızda, Hyper-V sanal Ethernet öykünücü kullanmak oluşturulan bağdaştırıcıların otomatik olarak kaldırılmaz. Hyper-V Yöneticisi'ni açarak ve sonra öykünücü VHD görüntüleri birini seçerek ağ sekmesini seçerek seçerek bu sanal bağdaştırıcılar (Eğer kullanımda olmayan) el ile kaldırabilirsiniz **Kaldır** bu sekmede görünür anahtarların her biri için.  
  
##  <a name="Requirements"></a> Sistem gereksinimleri ve geriye dönük uyumluluk  
 Donanım, yazılım ve Android için Visual Studio öykünücüsü'nü yapılandırma gereksinimleri hakkında önemli bilgiler için aşağıdaki konuya bakın.  
  
-   [Android için Visual Studio öykünücüsü sistem gereksinimleri](../cross-platform/system-requirements-for-the-visual-studio-emulator-for-android.md)  
  
 Android için Visual Studio öykünücü, Visual Studio 2015 gerektirir; Visual Studio'nun önceki sürümleriyle geriye dönük olarak uyumlu değil.  
  
 Öykünücü yeni sürümleri eski sürümlerinin üzerine yüklenir (ve bazı durumlarda, ayarları, uygulamalar ve dosyalar üzerinde bu görüntüleri yüklü atılıyor eski görüntülerin değiştirin olabilir).  
  
##  <a name="Networking"></a> Android için Visual Studio öykünücüsü'nü de ağ  
 Android için Visual Studio öykünücüsü ' ağ bağlantısı, bir masaüstü bilgisayarın bu özelliklere sahip bir bağlantı gibi davranır:  
  
-   Öykünücü ağ üzerinde kendi IP adresine sahip ayrı bir cihaz olarak görünür.  
  
-   Öykünücü ile zaten yüklü değilse ek ağ yazılımı gerektirmez.  
  
-   Bir Windows etki alanına katılmamış.  
  
 Öykünücü'nın ağ bağlantısı özelliklerini anlamak için bu Android telefonunuzdan aynı ağa bir Wi-Fi bağlantısı için benzer olarak düşünebilirsiniz. Telefonunuzda çalışan bir uygulamanın bir ağ kaynağına, Wi-Fi bağlantısı üzerinden erişebilirsiniz, öykünücü üzerinde çalışan bir uygulama da aynı ağ kaynağına erişebilirsiniz.  
  
 Ağ gereksinimleri hakkında daha fazla bilgi için bkz. [Android için Visual Studio öykünücüsü sistem gereksinimleri](../cross-platform/system-requirements-for-the-visual-studio-emulator-for-android.md)  
  
 Ağ sorunlarını giderme hakkında daha fazla bilgi için bkz. [Android için Visual Studio öykünücü sorun giderme](../cross-platform/troubleshooting-the-visual-studio-emulator-for-android.md).  
  
##  <a name="Configuring"></a> Android için Visual Studio öykünücüsü'nü yapılandırma  
 Android uygulamanız için Uyumluluk şaşırtıcı çeşitli Android donanım üzerinde test zor olabilir. Android telefonlar ve tabletler pazarında kapsayan çok çeşitli sürümleri ve ekran boyutları ve birçok farklı donanım yapılandırmalarında (RAM, CPU, mimarisi, vb.) gelir. Android için Visual Studio öykünücüsü, bu cihaz profillerini kullanarak kolaylaştırır. Cihaz profillerinin kümemizdeki Samsung, Motorola, Sony, LG ve diğer cihazlar dahil pazardaki en popüler donanımı temsil eder.  
  
 Visual Studio 2015'te yüklemek, kaldırmak ve öykünücü Yöneticisi'ni kullanarak cihaz profilleri Başlat. Öykünücü Yöneticisi'ni seçerek erişim **Araçları**, ardından **Android için Visual Studio öykünücü**.  
  
 ![Android Manager için Visual Studio öykünücüsü](../cross-platform/media/android_emu_manager.png "Android_Emu_Manager")  
  
 Varsayılan olarak, dört önceden yüklenmiş cihaz profilleri vardır (KitKat ve Lollipop phone/5 "ve 7/tablet" yapılandırmaları), simgeler ve beyaz metinli belirtti. Siz seçene kadar diğer profiller listede gri renkte görünür **profil Yükle** düğmesi ve yüklemeyi tamamlar. API düzeyine göre listeyi filtreleyin ve ayrıntıları tam yapılandırma ayrıntılarını görüntülemek için bir profil alt sağ tarafındaki oka tıklayın.  
  
 Hedeflemek istediğiniz profilleri kümesine yükledikten sonra bu yeni profiller doğrudan Manager'dan yeşil tuşlarına basarak başlatabilirsiniz **Play** düğmesi. Bunlar herhangi bir Visual Studio platformlar arası mobil proje türünü hata ayıklama hedef açılır menüde görünür.  
  
##  <a name="FeaturesTest"></a> Öykünücüde test etme özellikleri  
 Öykünücüde test özellikleri hakkında ayrıntılı bilgi için bkz. Bu [blog gönderisi](https://blogs.msdn.microsoft.com/devops/2014/11/12/introducing-visual-studios-emulator-for-android/).  
  
##  <a name="FeaturesNonTest"></a> Öykünücüde test etme özellikleri  
 Aşağıdaki listede Android platform özellikleri açıklar, **olamaz** öykünücüsünde test edin. Bu özellikler fiziksel bir cihaz üzerinde test gerekir.  
  
-   Compass  
  
-   Jiroskop  
  
-   Titreşim denetleyicisi  
  
-   Parlaklık. Öykünücü parlaklık düzeyini değiştirme görsel olarak cihaz ekranda görüntülenme şeklini etkilemez.  
  
##  <a name="Support"></a> Destek kaynakları  
 Ana bilgisayarınızın sistem gereksinimlerini karşıladığından ve bu sorun giderme Kılavuzu'nda ele alınmayan bir sorunla karşılaşırsanız varsa:  
  
-   StackOverflow kullanma hakkında bir soru sorun [android öykünücüsü](http://stackoverflow.com/questions/tagged/android-emulator) ve visual studio etiketi.  
  
-   Visual Studio'da veya öykünücü Yöneticisi'nde gönderme gülümseme aracını kullanarak bir sorun bildirin.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Android için Visual Studio öykünücüsü sistem gereksinimleri](../cross-platform/system-requirements-for-the-visual-studio-emulator-for-android.md)   
 [Android için Visual Studio Öykünücüsü’nde Sorun Giderme](../cross-platform/troubleshooting-the-visual-studio-emulator-for-android.md)
