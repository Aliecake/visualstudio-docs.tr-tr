---
title: SharePoint projelerini genişletme | Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- projects [SharePoint development in Visual Studio], extending
- SharePoint development in Visual Studio, extending projects
- SharePoint projects, extending
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 76648e128db23415d6a986a7d0087968c549bd13
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36326014"
---
# <a name="extend-sharepoint-projects"></a>SharePoint projeleri genişletme
  SharePoint projeleri proje düzeyi özelliklerini özelleştirmek istediğiniz zaman bir proje uzantısı oluşturma. Örneğin, özel Proje özelliklerini eklemek ya da kullanıcı bir SharePoint çözüm Visual Studio'da geliştirir başlatılan proje düzeyi olaylara yanıt.  
  
## <a name="create-project-extensions"></a>Proje uzantıları oluşturma
 Bir proje öğesi genişletmek için uygulayan bir Visual Studio uzantısı derleme <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> arabirimi. Daha fazla bilgi için bkz: [nasıl yapılır: bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).  
  
 Bir proje uzantısı oluşturduğunuzda, SharePoint projelerine aşağıdaki işlevler de ekleyebilirsiniz:  
  
-   Bir kısayol menü öğesi ekleyin. Bir SharePoint proje düğümünde için kısayol menüsünü açtığınızda menü öğesi görünür **Çözüm Gezgini** düğümünü sağ tıklayarak veya seçmeden ve ardından seçme **Shift** +  **F10** anahtarları. Daha fazla bilgi için bkz: [nasıl yapılır: bir kısayol menü öğesini SharePoint projelerine ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md).  
  
-   Bir özel özellik ekleyin. Özellik görünür **özellikleri** bir SharePoint Proje seçtiğinizde penceresi **Çözüm Gezgini**. Daha fazla bilgi için bkz: [nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).  
  
 Oluşturma, dağıtma ve bir proje uzantısı test izlenecek yol için bkz: [izlenecek yol: bir SharePoint proje uzantısı oluşturma](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md).  
  
## <a name="understand-the-relationship-between-project-extensions-and-project-instances"></a>Proje uzantıları ve proje Örnekler arasındaki ilişkiyi anlama
 Bir proje uzantısı oluşturma, herhangi bir SharePoint proje türünü açıldığında uzantıyı yükler [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Liste tanımları, içerik türleri ve Olay alıcıları gibi birkaç SharePoint proje şablonları içerir. Ancak, yalnızca bir SharePoint proje türü yok. Görüntülenen Proje türleri **yeni proje** iletişim kutusu, yalnızca bir veya daha fazla SharePoint Proje öğeleri birlikte paketini şablonlardır. Yalnızca bir SharePoint proje türü olduğundan, bir proje için oluşturulmuş uzantıları tüm SharePoint projeler için geçerlidir. Örneğin, yalnızca geçerli uzantı oluşturamazsınız bir **içerik türü** projesi.  
  
 Belirli bir proje örneğine erişmek için aşağıdakilerden birini ele <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents> olayları *projectService* parametresi uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension.Initialize%2A> yöntemi. Örneğin, bir SharePoint projesine bir çözüme eklendiğinde belirlemek için tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectAdded> olay. Daha fazla bilgi için bkz: [nasıl yapılır: bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)   
 [Nasıl yapılır: bir kısayol menü öğesini SharePoint projelerine ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md)   
 [Nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md)   
 [İzlenecek yol: bir SharePoint proje uzantısı oluşturma](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md)   
 [Özel SharePoint proje öğesi türlerini tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)   
 [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)   
 [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)   
 [SharePoint Proje sistemini genişletme](../sharepoint/extending-the-sharepoint-project-system.md)  
  
  
