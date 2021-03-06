---
title: Visio çözümleri
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office projects [Office development in Visual Studio], Visio
- solutions [Office development in Visual Studio], Visio
- Visio [Office development in Visual Studio]
- templates [Office development in Visual Studio], Visio
- projects [Office development in Visual Studio], Visio
- Office solutions [Office development in Visual Studio], Visio
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: c583108d1cc7aca35b8df4f20d787571c865e400
ms.sourcegitcommit: 4cd4aef53e7035d23e7d1d0f66f51ac8480622a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34767822"
---
# <a name="visio-solutions"></a>Visio çözümleri
  Visual Studio Proje şablonları, Microsoft Office Visio için VSTO eklentileri oluşturmak için kullanabileceğiniz sağlar. VSTO eklentileri Visio otomatikleştirmek, Visio özelliklerini genişletmek veya Visio kullanıcı arabirimi (UI) özelleştirmek için kullanabilirsiniz.  
  
 VSTO eklentileri hakkında daha fazla bilgi için bkz: [VSTO eklentileri programlamaya başlamak](../vsto/getting-started-programming-vsto-add-ins.md) ve [mimarisi, VSTO eklentileri](../vsto/architecture-of-vsto-add-ins.md). Microsoft Office ile programlamada yeniyseniz, bkz: [başlama &#40;Visual Studio'da Office geliştirme&#41;](../vsto/getting-started-office-development-in-visual-studio.md).  
  
 **Uygulandığı öğe:** Bu konu başlığı altındaki bilgiler Visio 2010 VSTO eklentisi projelerine yöneliktir. Daha fazla bilgi için bkz: [Office uygulaması ve proje türüne göre kullanılabilen özellikler](../vsto/features-available-by-office-application-and-project-type.md).  
  
> [!NOTE]  
>  Office deneyimi boyunca genişletmek çözümleri geliştirirken ilgileniyor [birden çok platform](https://dev.office.com/add-in-availability)? Yeni [Office eklentileri modeli](https://dev.office.com/docs/add-ins/overview/office-add-ins). VSTO eklentilerini ve çözümlerle karşılaştırıldığında küçük bir yer Office eklentileri sahip ve teknoloji, HTML5, JavaScript, CSS3 ve XML gibi programlama neredeyse her web kullanarak oluşturabilirsiniz.  
  
## <a name="automate-visio-by-using-the-visio-object-model"></a>Visio nesne modelini kullanarak Visio otomatikleştirme  
 Visio nesne modeline kuruluş şemaları, akış çizelgeleri, proje zaman çizelgeleri, ağ şemaları, office alanları ve daha fazlası için diyagramlar oluşturmak için Visio otomatikleştirmek için kullanabileceğiniz birçok sınıf sağlar. API, ortak görevleri gerçekleştirmek için kod yazmanıza olanak sağlar:  
  
-   Oluşturun ve şekil ve metinler diyagramlarda getirin.  
  
-   İş mantığına göre şekil davranışını ve kullanıcı girişi yönetin.  
  
-   Kaydırma ve yakınlaştırma gibi diyagramı görselleştirme denetler.  
  
-   Uygulama kullanıcı Arabirimi özelleştirin.  
  
-   Visio'ya dış veri almak, şekillere bağlama ve grafik bir sayfada görüntüleme.  
  
 Adım adım yordamlar görüntülemek ve kod belgeler ve şekiller çalışmak için Visio nesne modelini kullanma örnekleri [Visio belgeleriyle çalışma](../vsto/working-with-visio-documents.md) ve [Visio şekilleri ile çalışma](../vsto/working-with-visio-shapes.md).  
  
 Bir VSTO eklentiden Visio nesne modeline erişmek için `Application` alanını `ThisAddIn` projenizdeki sınıfı. `Application` Alan döndürür bir `Microsoft.Office.Interop.Visio.Application` Visio geçerli örneği temsil eden nesne. Daha fazla bilgi için bkz: [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md).  
  
 Visio nesne modeline çağırdığınızda, Visio için birincil birlikte çalışma derlemesi (PIA) sağlanan türleri kullanabilirsiniz. PIA yönetilen kod için VSTO eklentisi ve Visio'da COM nesne modeli arasında köprü gibi davranır. Visio PIA içindeki tüm türler tanımlanan `Microsoft.Office.Interop.Visio` ad alanı. Birincil birlikte çalışma derlemeleri hakkında daha fazla bilgi için bkz: [Office çözümleri geliştirmesine genel bakış &#40;VSTO&#41; ](../vsto/office-solutions-development-overview-vsto.md) ve [Office birincil birlikte çalışma derlemeleri](../vsto/office-primary-interop-assemblies.md).  
  
## <a name="visio-object-model-overview"></a>Visio nesne modeline genel bakış  
 Visio nesne modeline genel bakış bulabilirsiniz [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md), Visio nesne modeli başvurusu ve SDK'ları bağlantılar içerir.  
  
## <a name="customize-the-user-interface-of-visio"></a>Visio kullanıcı arabirimini özelleştirme  
 Visio UI aşağıdaki özelleştirme seçenekleri vardır.  
  
|Görev|Daha fazla bilgi için|  
|----------|--------------------------|  
|Şerit özelleştirin.|[Şeride Genel Bakış](../vsto/ribbon-overview.md)|  
  
 UI özelleştirme hakkında daha fazla bilgi için VBA başvuru belgelerine bakın [Visio.UIObject](https://msdn.microsoft.com/library/office/ff765763.aspx) sınıfı.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSTO eklentileri programlama kullanmaya başlama](../vsto/getting-started-programming-vsto-add-ins.md)   
 [Office çözümleri geliştirmesine genel bakış &#40;VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md)   
 [VSTO eklentileri mimarisi](../vsto/architecture-of-vsto-add-ins.md)   
 [Nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [VSTO eklentilerini programlama](../vsto/programming-vsto-add-ins.md)   
 [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)   
 [Office birincil birlikte çalışma derlemeleri](../vsto/office-primary-interop-assemblies.md)   
 [Office kullanıcı arabirimini özelleştirme](../vsto/office-ui-customization.md)   
 [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md)   
 [Visio 2010 Office geliştirme](http://go.microsoft.com/fwlink/?LinkId=199017)  
  