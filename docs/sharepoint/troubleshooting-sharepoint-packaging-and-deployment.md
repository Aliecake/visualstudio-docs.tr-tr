---
title: SharePoint paketleme ve dağıtım sorunlarını giderme | Microsoft Docs
ms.custom: ''
ms.date: 02/22/2017
ms.technology:
- office-development
ms.topic: conceptual
f1_keywords:
- VSTO.WorkflowDeployment.Troubleshooting
- VS.SharePointTools.Project.PackageRetraction
- VS.SharePointTools.Deployment.Troubleshooting
- VS.SharePointTools.Deploying.Troubleshooting
- VS.SharePointTools.Project.DeploymentTroubleshooting
- VS.SharePointTools.Project.SharePointNotInstalled
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packaging
- SharePoint development in Visual Studio, troubleshooting
- SharePoint development in Visual Studio, deployment conflict resolution
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ea1c04066099b385b03c1b81bc4d85c7fb13e329
ms.sourcegitcommit: d9e4ea95d0ea70827de281754067309a517205a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37120447"
---
# <a name="troubleshoot-sharepoint-packaging-and-deployment"></a>SharePoint paketleme ve dağıtım sorunlarını giderme
  Bu konuda paketini ve SharePoint çözümlerini dağıtırken karşılaşabileceğiniz çeşitli sorunlar ele alınmaktadır.

## <a name="enable-enhanced-debugging"></a>Gelişmiş hata ayıklamayı etkinleştir
 Visual Studio, SharePoint ve diğer katmanları arasında tanılamak için yığın izlemesi görüntülemek için EnableDiagnostics kayıt defteri anahtarını kullanabilirsiniz. Daha fazla bilgi için bkz: [hata ayıklama SharePoint çözümlerini](../sharepoint/debugging-sharepoint-solutions.md).

## <a name="add-project-output-to-the-solution-package"></a>Proje çıktı çözüm paketi ekleme
 Bir paketi paket tasarımcısını aracılığıyla proje çıktı ekleyebilirsiniz. Ancak, proje çıktı eklediğinizde, projenin platform SharePoint çözüm platformu eşleştiğinden emin olun. Kullanmanızı öneririz **herhangi bir CPU** SharePoint sunucusuna dağıtmak istediğiniz derlemeler için platform hedefi. Daha fazla bilgi için bkz: [derleme sayfası, Proje Tasarımcısı &#40;Visual Basic&#41; ](/visualstudio/ide/reference/compile-page-project-designer-visual-basic) ve [Gelişmiş derleyici Ayarları iletişim kutusu &#40;Visual Basic&#41;](/visualstudio/ide/reference/advanced-compiler-settings-dialog-box-visual-basic).

## <a name="validation-warnings-and-errors"></a>Doğrulama uyarıları ve hataları
 Visual Studio'da SharePoint geliştirme araçları çözüm paketi doğru biçimlendirildiğinden emin doğrulamak için doğrulama adımlarını gerçekleştirin. Özel doğrulama adımlarını, özellikleri ve paketler için de oluşturabilirsiniz. Daha fazla bilgi için bkz: [nasıl yapılır: özel özellik ve paket doğrulama kuralları için SharePoint çözümleri oluşturma](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md).

## <a name="deployment-conflict-resolution"></a>Dağıtım Çakışma çözümlemesi
 Bir SharePoint çözümünü dağıttığınızda, sunucu üzerindeki bir öğeyi çözüm paketi bir öğesiyle aynı adı, URL veya kimliği sahip olduğunda çakışmaları bulabilirsiniz. Değiştirebileceğiniz **dağıtım Çakışma çözümlemesi** çözmek için rapor veya modüller, Web bölümleri, liste örnekleri ve içerik türleri için Çakışmaları Yoksay özelliği.

 Aşağıdaki tabloda ayarlarını gösteren **dağıtım Çakışma çözümlemesi** özelliği.

|Değer|Açıklama|
|-----------|-----------------|
|Otomatik|Çakışmaları algılar ve çakışma otomatik olarak çözer.|
|Sor|Çakışmaları algılar ve bunları çakışmalarını çözme önce geliştiriciye raporlar.|
|Yok.|Çakışmaları algılamaz.|

## <a name="differences-between-f5-deployment"></a>F5 dağıtım arasındaki farklar
 Kullandığınızda [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] test ve hata ayıklama için yerel SharePoint server, SharePoint Proje dağıtmak için tarafından gerçekleştirilen bazı ek adımlar vardır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].

1.  Internet Information Service (IIS) dağıtım adımı sırasında sıfırlayın.

2.  İş akışları otomatik olarak ilişkilendirilir.

3.  Hiyerarşinin özelliği etkinleştirme sırayla paket Tasarımcısı'nda ayarlayın.

 Daha fazla değişiklik özel dağıtım adımlarını ekleyebilirsiniz **F5** davranışı. Daha fazla bilgi için bkz: [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturma](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md).

## <a name="delay-displaying-sharepoint-page-when-deploy-visual-web-part"></a>SharePoint sayfası görüntüleme gecikme visual web bölümünü dağıtırken
 SharePoint sayfası üzerinde Bin klasörü için bir Visual Web bölümünü dağıtırken görünür uzun süren [!INCLUDE[wiprlhext](../sharepoint/includes/wiprlhext-md.md)], [!INCLUDE[win7](../sharepoint/includes/win7-md.md)], veya [!INCLUDE[winsvr08](../sharepoint/includes/winsvr08-md.md)]. Üst düzey bir klasördeki tüm dosyaları değiştirirseniz [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] Bin dizini gibi dizini tüm Web uygulaması yeniden derler. Bu, en fazla 25 işleme süresini saniye cinsinden SharePoint sayfası için bir gecikmeye neden olabilir.

### <a name="error-message"></a>Hata iletisi
 Yok.

### <a name="resolution"></a>Çözüm
 Bu sorunu geçici olarak çözmek için aşağıdaki adımları gerçekleştirin:

1.  KB967535 Microsoft Support makalesini özetlendiği gibi güncelleştirmesini [DÜZELTİN: ASP.NET IIS 7.0 Windows Vista ve Windows Server 2008 için iki sorunu düzeltmek bir düzeltme kullanılabilir](http://go.microsoft.com/fwlink/?LinkId=179055).

2.  Web.config dosyasında aşağıdaki satırı ekleyin:

    ```xml
    <compilation batch="false" optimizeCompilations="true">
    ```

## <a name="sharepoint-project-deployment-fails-with-error-failed-to-extract-the-cab-file-in-the-solution"></a>SharePoint proje dağıtımı "çözümdeki cab dosyası ayıklanamadı" hatasıyla başarısız oluyor
 Herhangi bir SharePoint Proje öğe adı ayraç içeriyorsa, çözümü dağıtımda bir hata ile başarısız olur.

### <a name="error-message"></a>Hata iletisi
 Bir hata oluştu 'Çözüm Ekle' dağıtım adımda: çözümdeki cab dosyası ayıklanamadı.

### <a name="resolution"></a>Çözüm
 Bu sorunu geçici olarak çözmek için SharePoint Proje öğeleri adlarında parantezleri kaldırın.

## <a name="error-appears-when-deploying-a-visual-web-part-to-a-site-on-a-different-web-application"></a>Visual web bölümü bir siteye farklı bir web uygulamasına dağıtırken hata görünür
 Visual Web Bölümü, bir Web uygulaması, birinde dışında bir siteye dağıtmak ilk kez şu anda (visual Web bölümünün SiteUrl özelliğini değiştirerek) dağıtıldığı, bir hata alıyorsunuz.

### <a name="error-message"></a>Hata iletisi
 Dağıtım adımı 'Çözüm Ekle' hata oluştu: [#] kimlikli özellik bu grupta yüklü. Açıkça özelliği yeniden yüklemek için zorlama özniteliğini kullanın.

### <a name="resolution"></a>Çözüm
 Visual Web Bölümü özelliklerini SharePoint'te geri çekilebilir şekilde nedeniyle bu hata oluşur. Visual Web bölümü başarıyla dağıtmak için çözümü yeniden seçerek dağıtmak **F5** anahtarı.

## <a name="warning-appears-when-deploying-nested-user-controls"></a>İç içe geçmiş kullanıcı denetimleri dağıtırken uyarı görünür
 Bu uyarı, bir kullanıcı denetimini içeren bir visual Web Bölümü veya visual Web bölümünü içeren bir kullanıcı denetimi veya başka bir kullanıcı denetimi gibi iç içe geçmiş kullanıcı denetimleri olan bir SharePoint çözüm dağıtma oluşur. Bu uyarı araç sürükleyerek ya da kullanarak bir Tasarımcı denetim eklemek isteyip oluşur @Register kaynağı görünümündeki yönergesi.

### <a name="error-message"></a>Hata iletisi
 1 öğe uyarı ' [*denetim adı*]' bilinen bir öğe değil. Bu Web sitesinde bir derleme hatası ise veya web.config dosyasında eksik ortaya çıkabilir.

### <a name="resolution"></a>Çözüm
 Varsa [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] proje sistemi bir iç içe geçmiş kullanıcı denetimi uyumlu değil, IntelliSense sağlayamaz ve uyarı yayar. Proje sistemi bir iç içe geçmiş kullanıcı denetimi farkında değildir proje oluşturulmadı ve tasarımcı kapalı ve yeniden açık değil veya durumunda otomatik geri çekmek seçeneği etkin olduğunda, kullanıcı denetimi neden olan hata ayıklama sonra SharePoint kovanından çekilmesini.

 Bu uyarıyı kaldırmak için projeyi oluşturun ve sonra kapatın ve tasarımcı yeniden açın ya da devre dışı bırakma seçeneği projesi için otomatik olarak ayıkla. Bunu yapmak için temizleyin **otomatik-hata ayıklama sonra geri çekmek** onay kutusunu **SharePoint** Proje Özellikleri iletişim kutusunda.

## <a name="see-also"></a>Ayrıca bkz.
 [Paket ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)

