---
title: "Test alanı 4: İade | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], checking items in
- source control plug-ins, checking items in
ms.assetid: d0329fa8-7a8d-4d30-b67b-6f2a97b75a30
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3694e8f4a8cdbdac147df3d6e60324888bccf048
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="test-area-4-check-in"></a>Test alanı 4: İade etme
Bu kaynak denetimi eklenti test alanını kapsayan sürüm deposuna güncelleştirilmiş öğeleri gönderme **iade** komutu.  
  
## <a name="command-menu-access"></a>Komut menü erişimi  
 Aşağıdaki [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı menü yolları test çalışmaları kullanılır.  
  
##### <a name="check-in"></a>Teslim etme:  
 **Dosya**, **kaynak denetimi**, **iade**.  
  
 **Dosya**, **iade**.  
  
 Kısayol menüsünde **iade**.  
  
## <a name="common-expected-behavior"></a>Ortak beklenen bir davranış  
  
-   Proje ve çözüm ya da kaynak denetimi altında proje için eklenen dosyalar görünür **iade** iletişim kutusu ve **Bekleyen İadeler** penceresi.  
  
-   Sonra iade eklenen öğeler kaynak denetiminde görünür.  
  
-   Sonra iade güncelleştirilmiş deposunda düzgün sürümlü öğelerdir.  
  
## <a name="test-cases"></a>Test çalışmaları  
 Belirli test çalışmaları iade test alanı için verilmiştir.  
  
### <a name="case-4a-modified-items"></a>Case 4a: öğeler  
 Değiştirilmiş kaynak denetimi altında bir dosyayı güncelleştirmek için eylemde onay kullanmayı açıklar.  
  
|Eylem|Test adımları|Doğrulamak için beklenen sonuçları|  
|------------|----------------|--------------------------------|  
|Kullanıma alınmış bir metin dosyası değiştirmek, yalnızca dosyasını denetleyin (**iade** iletişim kutusu)|1.  Yeni bir proje ile bir metin dosyası oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Kullanıma alma ve metin dosyasını değiştirin.<br />4.  İade Et iletişim kutusu üzerinden kontrol edin (**dosya**, **kaynak denetimi**, **iade**).|Ortak beklenen davranıştır.|  
|Kullanıma alınmış bir metin dosyası değiştirmek, yalnızca dosyasını denetleyin (**Bekleyen İadeler** penceresi)|1.  Yeni bir proje ile bir metin dosyası oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Kullanıma alma ve metin dosyasını değiştirin.<br />4.  Aracılığıyla iade **Bekleyen İadeler** penceresi.|Ortak beklenen davranıştır.|  
  
### <a name="case-4b-adding-files"></a>Case 4b: dosya ekleme  
 Bir proje veya bir çözüm için bir öğe için bir dosya eklerken, proje ve çözüm aynı zamanda değiştirmeniz gerekir. Bu nedenle üst dosyasının de kullanıma ve ek tamamlamak için iade edilmesi gerekir.  
  
|Eylem|Test adımları|Doğrulamak için beklenen sonuçları|  
|------------|----------------|--------------------------------|  
|Bir metin dosyası ekleyin ve her şeyi denetleyin (**iade** iletişim kutusu)|1.  Yeni bir proje oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Bir metin dosyası projeye ekleyin.<br />4.  Proje kullanıma istendiğinde kabul edin.<br />5.  Çözümde seçin **Çözüm Gezgini**.<br />6.  İade Et **iade** iletişim kutusu.|Ortak beklenen davranıştır.|  
|Bir metin dosyası ekleyin ve her şeyi denetleyin (**Bekleyen İadeler** penceresi)|1.  Yeni bir proje oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Bir metin dosyası projeye ekleyin.<br />4.  Proje kullanıma istendiğinde kabul edin.<br />5.  Çözümden iade **Bekleyen İadeler** penceresi.|Ortak beklenen bir davranış|  
  
### <a name="case-4c-adding-projects"></a>Bu durumda 4 c: projelerine ekleme  
 Bir çözüme proje ekleme, çözümü aynı zamanda değiştirmeniz gerekir. Bu nedenle çözüm dosyasını da kullanıma ve ek tamamlamak için iade edilmesi gerekir.  
  
|Eylem|Test adımları|Doğrulamak için beklenen sonuçları|  
|------------|----------------|--------------------------------|  
|Kaynak denetimi altında boş bir çözüme proje ekleme (**iade** iletişim kutusu)|1.  Boş bir çözüm oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Yeni bir proje ekleyin.<br />4.  Çözümün kullanıma istendiğinde kabul edin.<br />5.  İade Et **iade** iletişim kutusu.|Ortak beklenen davranıştır.|  
|Kaynak denetimi altında boş bir çözüme proje ekleme (**Bekleyen İadeler** penceresi)|1.  Boş bir çözüm oluşturun.<br />2.  Çözümü kaynak denetimine ekleyin.<br />3.  Yeni bir proje ekleyin.<br />4.  Çözümün kullanıma istendiğinde kabul edin.<br />5.  Çözümden iade **Bekleyen İadeler** penceresi.|Ortak beklenen davranıştır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak denetimi eklentiler için test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)