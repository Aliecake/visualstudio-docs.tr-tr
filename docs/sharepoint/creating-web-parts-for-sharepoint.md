---
title: SharePoint için Web bölümleri oluşturma | Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
f1_keywords:
- Microsoft.SharePoint.WebControls.DateTimeControl
- Microsoft.SharePoint.WebControls.CssLink
- Microsoft.SharePoint.WebControls.RssLink
- Microsoft.SharePoint.WebControls.Theme
- Microsoft.SharePoint.WebControls.AspMenu
- Microsoft.SharePoint.WebControls.ListProperty
- Microsoft.SharePoint.WebControls.ProjectProperty
- Microsoft.SharePoint.WebControls.FormsDigest
- Microsoft.SharePoint.WebControls.ScriptLink
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, Web Parts
- Web Parts [SharePoint development in Visual Studio], designing
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: cd92e4e4b5f4a0ae77cfae393d2d51446e17bcfe
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36327222"
---
# <a name="create-web-parts-for-sharepoint"></a>SharePoint Web bölümleri oluşturma
  Web Bölümleri'ni kullanarak, içerik, Görünüm ve bir SharePoint sitesinin sayfalarının davranışını bir tarayıcı kullanarak değiştirebilirsiniz. Web Bölümleri olan bir web bölümü sayfası içinde çalışan sunucu tarafı denetimleri: bir SharePoint sitesinde sayfaları yapı taşlarını oldukları. Bkz: [yapı taşı: Web Bölümleri](http://go.microsoft.com/fwlink/?LinkID=182097).  
  
 Oluşturun ve Visual Studio şablonlarını kullanarak bir SharePoint sitesinde web bölümleri hata ayıklama.  
  
## <a name="create-a-web-part-in-visual-studio"></a>Visual Studio'da bir web bölümü oluşturma
 Ekleyerek web bölümü oluşturma bir **Web Bölümü** herhangi bir SharePoint proje öğesi. Kullanabileceğiniz bir **Web Bölümü** korumalı bir çözüm veya bir Grup çözümü öğe.  
  
 Tasarımcı kullanarak bir web bölümü görsel olarak tasarlamak için oluşturmak istiyorsanız, bir **Visual Web Bölümü** proje veya ekleme **Visual Web Bölümü** herhangi bir SharePoint proje öğesi. Kullanabileceğiniz bir **Visual Web Bölümü** yalnızca bir Grup çözümü öğesinde.  
  
### <a name="web-part-item"></a>Web Bölümü öğesi
 A **Web Bölümü** öğesi bir SharePoint sitesi için bir web bölümü tasarlamak için kullanabileceğiniz dosyaları sağlar. Eklediğinizde bir **Web Bölümü** öğesi, Visual Studio projenizi bir klasör oluşturur ve ardından klasörüne birkaç dosyaları ekler. Aşağıdaki tabloda, her dosya açıklanmaktadır.  
  
|Dosya|Açıklama|  
|----------|-----------------|  
|*Elements.XML*|Projenizdeki Özellik tanım dosyası web bölümünü dağıtmak için kullandığı bilgileri içerir.|  
|.WebPart dosyası|SharePoint web bölümü Galerisi'nde, web bölümünü görüntülemek için gereken bilgileri sağlar.|  
|Kod dosyası|Web bölümü için denetimler ekleme ve özel içerik web bölümü içinde oluşturma yöntemleri içerir.|  
  
 Daha fazla bilgi için bkz: [nasıl yapılır: bir SharePoint web bölümü oluşturma](../sharepoint/how-to-create-a-sharepoint-web-part.md).  
  
### <a name="visual-web-part-item"></a>Visual web bölümü öğesi
 Visual web bölümü Visual Studio'da Visual Web Developer Tasarımcısı'nı kullanarak oluşturduğunuz web bir parçasıdır. Visual web bölümü aynı herhangi bir web parçası olarak çalışır. Denetimler, düğmeler ve metin kutuları gibi bir web bölümü eklemek için bir XML dosyasına kodu ekleyin. Ancak, denetimleri visual web bölümü için sürükleyerek ya da Visual Studio'dan kopyalayarak web bölümü eklemeniz **araç**. Tasarımcı sonra XML dosyasında gerekli kod oluşturur. Bkz: [nasıl yapılır: Tasarımcı kullanarak oluşturmak SharePoint web bölümü](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md).  
  
## <a name="sharepoint-controls"></a>SharePoint denetimleri
 Visual Studio, uygulama sayfaları gibi SharePoint sayfaları oluşturmak için bazı denetimler sağlar. Bu denetimler görünür **araç** altında **SharePoint denetimleri**. Bu denetimler için işlevsellik türetilen [Microsoft.SharePoint.WebControls](http://go.microsoft.com/fwlink/?LinkId=235315) SharePoint site ve liste sayfalarında kullanılan ASP.NET sunucu denetimleri içeren ad alanı.  
  
|Denetim adı|Açıklama|  
|------------------|-----------------|  
|[AspMenu](http://go.microsoft.com/fwlink/?LinkId=235307)|Bir ASP menüsü ekler. Daha fazla bilgi için bkz: [Menü denetimine genel bakış](http://go.microsoft.com/fwlink/?LinkId=235316).|  
|[CssLink](http://go.microsoft.com/fwlink/?LinkId=235308)|Ekler bir **bağlantı** öğesine *.aspx* sayfasında ve bir veya daha fazla dış stil sayfası tarafından tanımlandı geçerlidir **CssRegistration**.|  
|[DateTimeControl](http://go.microsoft.com/fwlink/?LinkId=235306)|DateTime denetime ekler *.aspx* sayfası.|  
|[FormDigest](http://go.microsoft.com/fwlink/?LinkId=235309)|Güvenlik doğrulaması içine ekler *.aspx* sayfası|  
|[ListProperty](http://go.microsoft.com/fwlink/?LinkId=235310)|Bir özelliği, belirtilen bir liste döndürür.|  
|[ProjectProperty](http://go.microsoft.com/fwlink/?LinkId=235311)|Genel özellik geçerli Web sitesinin döndürür.|  
|[RssLink](http://go.microsoft.com/fwlink/?LinkId=235312)|İçine bir RSS bağlantısını ekler *.aspx* sayfası.|  
|[ScriptLink](http://go.microsoft.com/fwlink/?LinkId=235313)|Özellikleri ve sayfa işlendiğinde bunlar istenebilir bir sayfadaki komut dosyaları gibi kaynakları kaydetme için yöntemleri sağlar.|  
|[Tema](http://go.microsoft.com/fwlink/?LinkId=235314)|Bir temayı uygular *.aspx* sayfası.|  
  
## <a name="debug-a-web-part"></a>Bir web bölümü hata ayıklama
 Diğer Visual Studio projeleri debug gibi bir web bölümünü içeren bir SharePoint Proje ayıklayabilirsiniz. Visual Studio hata ayıklayıcısını başlattığınızda, Visual Studio SharePoint sitesini açar.  
  
 Kodunuzdaki hataları ayıklamanıza başlamak için SharePoint web bölümü sayfasına web bölümü ekleyin.  
  
 SharePoint projeleri hata ayıklama hakkında daha fazla bilgi için bkz: [sorun giderme SharePoint çözümlerini](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
## <a name="visual-web-part-limitations"></a>Visual web bölümü sınırlamaları
 Visual Studio ile başlayarak, korumalı SharePoint çözümleri ve küme çözümleri için visual web bölümleri ekleyebilirsiniz. Ancak, visual web bölümleri, aşağıdaki sınırlamalara sahiptir:  
  
-   Visual web bölümleri değiştirilebilir parametreler desteklemez. Daha fazla bilgi için bkz: [değiştirilebilir parametreler](../sharepoint/replaceable-parameters.md).  
  
-   Kullanıcı denetimleri veya visual web bölümleri sürüklenen ve bırakılan veya değiştirilemez visual web bölümleri kopyalanır. Bu eylem bir yapı hatasına neden olur.  
  
-   Visual web bölümleri SharePoint server belirteçleri $SPUrl gibi doğrudan desteklemez. Daha fazla bilgi için "Belirteci kısıtlamaları içinde korumalı Visual Web Bölümleri" konusuna bakın. [sorun giderme SharePoint çözümlerini](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
-   Visual web bölümleri korumalı bir çözümde bazen alma hatası, "korumalı kod ana bilgisayar hizmeti isteği işlemek için çok meşgul olduğundan korumalı kod yürütme isteği reddedildi." Bu hata hakkında daha fazla bilgi için bu postasına bakın [SharePoint geliştirici ekibi blogu](http://go.microsoft.com/fwlink/?LinkId=225932).  
  
-   Sunucu tarafı JavaScript hata ayıklama Visual Studio'da desteklenmez, ancak istemci tarafı JavaScript hata ayıklama desteklenir.  
  
     Satır içi JavaScript bir sunucu tarafı biçimlendirme dosyasına ekleyebilirsiniz, ancak hata ayıklama kesme noktaları biçimlendirme eklenen için desteklenmiyor. JavaScript hata ayıklama için dış JavaScript dosyası biçimlendirme dosyasındaki başvuru ve ardından JavaScript dosyasında kesme noktaları ayarlayın.  
  
-   Satır içi hata ayıklama [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] kod işaretleme dosyasının yerine oluşturulan kod dosyasında yapılması gerekir.  
  
-   Visual web bölümleri kullanımını desteklemez `<@ Assembly Src=` yönergesi.  
  
-   SharePoint web denetimleri ve bazı [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] denetimleri SharePoint korumalı ortamında desteklenmez. Desteklenmeyen denetimler visual web bölümü hata korumalı bir çözümde kullanılan "'Tema' 'Microsoft.SharePoint.WebControls' ad alanında yok türü veya ad alanı adı" görüntülenir.  
  
 Korumalı çözümler hakkında daha fazla bilgi için bkz: [korumalı arasındaki farklar ve Grup çözümleri](../sharepoint/differences-between-sandboxed-and-farm-solutions.md).  
  
## <a name="create-older-style-sharepoint-based-web-parts"></a>Eski stil SharePoint tabanlı web bölümleri oluşturma
 Özel oluşturmak için Visual Studio şablonları kullanabilirsiniz [!INCLUDE[vstecasplong](../sharepoint/includes/vstecasplong-md.md)] için SharePoint web bölümleri. [!INCLUDE[vstecasplong](../sharepoint/includes/vstecasplong-md.md)] Web Bölümleri üstünde yerleşiktir [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] web bölümü altyapı ve yeni projeler için önerilen türüdür.  
  
 Çok az durumlarda, SharePoint tabanlı web bölümü eski stil kullanarak bir web bölümü oluşturma gerekebilir. Web bölümleri'nin bu türleri oluşturmak için Visual Studio'yu kullanabilirsiniz, ancak Visual Studio özellikle bunları oluşturmanıza yardımcı olmak için tasarlanmış şablonları sağlamaz.  
  
 Ne zaman daha eski olan bir stil SharePoint tabanlı web bölümü oluşturmak isteyebilirsiniz hakkında daha fazla bilgi için bkz: [Windows SharePoint Services Web Bölümü altyapısında](http://go.microsoft.com/fwlink/?LinkId=169290). Eski stil SharePoint tabanlı web bölümünü kullanarak bir web bölümü oluşturma hakkında daha fazla bilgi için bkz: [temel bir SharePoint Web Bölümü oluşturma izlenecek](http://go.microsoft.com/fwlink/?LinkId=169288).  
  
## <a name="related-topics"></a>İlgili konular
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[Nasıl yapılır: bir SharePoint web bölümü oluşturma](../sharepoint/how-to-create-a-sharepoint-web-part.md)|SharePoint sayfaları için web bölümleri oluşturulacağı gösterilmektedir.|  
|[Nasıl yapılır: Tasarımcı kullanarak bir SharePoint web bölümü oluşturma](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md)|Görsel tasarım yüzeyini kullanarak SharePoint için web bölümleri oluşturulacağı gösterilmektedir.|  
|[Nasıl yapılır: bir SharePoint uygulama sayfası veya web bölümü için bir kullanıcı denetimi oluşturma](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md)|Uygulama sayfaları ve SharePoint çalıştıran web bölümleri tarafından kullanılabilecek özel, yeniden kullanılabilir denetimler oluşturma gösterir.|  
|[İzlenecek yol: SharePoint için bir web bölümü oluşturma](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md)|Bir web bölümü SharePoint için tasarım konuları açıklanmaktadır.|  
|[İzlenecek yol: Tasarımcı kullanarak bir web bölümü SharePoint için oluşturma](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint-by-using-a-designer.md)|Denetimleri görsel tasarım yüzeyine sürükleyerek bir web bölümü SharePoint için tasarım konuları açıklanmaktadır.|  
|[İzlenecek yol: SharePoint için OData görüntüleyen bir Silverlight web parçası oluşturma](../sharepoint/walkthrough-creating-a-silverlight-web-part-that-displays-odata-for-sharepoint.md)|Bir web bölümü Silverlight uygulamasını barındıran ve SharePoint listeleri verileri görüntüleyen bir SharePoint için tasarım konuları açıklanmaktadır.|  
  
