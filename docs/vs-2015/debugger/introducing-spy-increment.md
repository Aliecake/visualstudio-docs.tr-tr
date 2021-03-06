---
title: Spy ++ ile tanışın | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Spy++
ms.assetid: 733b514b-63a9-402d-89aa-4f0416766655
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5e420adb00bc8972aead555eb281826db689914
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49276269"
---
# <a name="introducing-spy"></a>Spy++'a Giriş
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Spy ++ aşağıdaki görevleri gerçekleştirmenize olanak sağlar:  
  
-   Sistem nesneleri arasındaki ilişkileri grafik ağacını görüntüler. Bunlar [işlemleri](../debugger/processes-view.md), [iş parçacıkları](../debugger/threads-view.md), ve [windows](../debugger/windows-view.md).  
  
-   Belirtilen arama [windows](../debugger/how-to-search-for-a-window-in-windows-view.md), [iş parçacıkları](../debugger/how-to-search-for-a-thread-in-threads-view.md), [işlemleri](../debugger/how-to-search-for-a-process-in-processes-view.md), veya [iletileri](../debugger/how-to-search-for-a-message-in-messages-view.md).  
  
-   Özelliklerini görüntülemek seçili [windows](../debugger/how-to-display-window-properties.md), [iş parçacıkları](../debugger/how-to-display-thread-properties.md), [işlemleri](../debugger/how-to-display-process-properties.md), veya [iletileri](../debugger/how-to-display-message-properties.md).  
  
-   Bir pencere, iş parçacığı, işlem veya ileti görünümünde doğrudan'ı seçin.  
  
-   Kullanım [Bulucu Aracı](../debugger/how-to-use-the-finder-tool.md) fare işaretçisini konumlandırma tarafından bir pencere seçmek için.  
  
-   Ayarlama **iletisi seçenekleri** karmaşık ileti günlüğü seçimi parametreleri kullanarak.  
  
 Spy ++ araç çubuğu ve daha hızlı çalışmanıza yardımcı olmak için köprüler sahiptir. Ayrıca sağlar bir **Yenile** etkin Görünümü güncelleştirmek için komut bir **pencere Bulucu Aracı** yayılırlar daha kolay hale getirmek için ve bir **yazı tipi** görünümü windows özelleştirmek için iletişim kutusu. Ayrıca, Spy ++, kaydetme ve kullanıcı tercihlerini geri yükleme sağlar.  
  
 Çeşitli Spy ++ windows, sık kullanılan komutlar bir kısayol menüsünü görüntülemek için sağ tıklayabilirsiniz. Hangi komutlar işaretçi nerede olduğuna bağlıdır. Örneğin, pencere görünümünde bir girişi sağ tıklatın ve Seçili pencerenin görünür olup, ardından **vurgulayın** kısayol menüsünde, daha kolay bulunabilir yükleyebilmeleri için seçilen pencere kenarlığını neden olur.  
  
> [!NOTE]
>  Spy ++ benzeyen iki diğer yardımcı programları vardır: işlemler, iş parçacıkları ve DDESPY ayrıntılarını gösteren PView. EXE, dinamik veri değişimi (DDE) iletileri izlemenize izin verir.  
  
## <a name="64-bit-operating-systems"></a>64-bit işletim sistemleri  
 Spy ++'ın iki sürümü vardır. Spy ++ (spyxx.exe) adlı ilk sürümü, 32 bit işlemde çalışan bir pencere gönderilen iletileri görüntülemek için tasarlanmıştır. Örneğin, Visual Studio 32-bit işlem içinde çalışır. Bu nedenle, Spy ++ gönderilen iletileri görüntülemek için kullanabileceğiniz **Çözüm Gezgini**. Visual Studio'da çoğu derlemeler için varsayılan yapılandırma bir 32-bit işlem içinde çalıştırmak için bu ilk sürümünde Spy ++ kullanılabilir olanı olduğu **Araçları** Visual Studio'daki menü.  
  
 Spy ++ (64-bit) (spyxx_amd64.exe) adlı dosyanın ikinci sürümü, 64-bit işlem içinde çalışmakta olan bir pencere gönderilen iletileri görüntülemek için tasarlanmıştır. Örneğin, bir 64-bit işletim sisteminde 64-bit işlem içinde not defteri çalışır. Bu nedenle, Spy ++ (64-bit) Not Defteri'ne gönderilen iletileri görüntülemek için kullanabilirsiniz. Spy ++ (64-bit) genellikle bulunur  
  
 .. \\ *Visual Studio yükleme klasörü*\Common7\Tools\spyxx_amd64.exe.  
  
 Her iki sürümünde de Spy ++ doğrudan komut satırından çalıştırabilirsiniz.  
  
> [!NOTE]
>  Spy ++ (64-bit) dosya adı "amd" içerse de, Windows işletim sistemi üzerinde herhangi bir x64 çalıştırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Spy ++ kullanma](../debugger/using-spy-increment.md)   
 [Spy ++ görünümleri](../debugger/spy-increment-views.md)   
 [Spy++ Başvurusu](../debugger/spy-increment-reference.md)




