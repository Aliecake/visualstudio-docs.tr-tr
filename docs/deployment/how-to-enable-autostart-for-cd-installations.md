---
title: "Nasıl yapılır: CD yüklemeleri için AutoStart'ı etkinleştirme | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-deployment
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, AutoStart
- ClickOnce deployment, installation on CD or DVD
- deploying applications [ClickOnce], installation on CD or DVD
ms.assetid: caaec619-900c-4790-90e3-8c91f5347635
caps.latest.revision: "17"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: e3656c3d32dcba946cf66d7fba56a68b3de467f6
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2017
---
# <a name="how-to-enable-autostart-for-cd-installations"></a>Nasıl yapılır: CD Yüklemeleri için AutoStart'ı Etkinleştirme
Dağıtırken bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama CD-ROM veya DVD-ROM'UNDAN gibi çıkarılabilir medya kullanarak etkinleştirebilir `AutoStart` böylece [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama ortam eklendiğinde otomatik olarak başlatılır.  
  
 `AutoStart`üzerindeki etkin **Yayımla** sayfasında **Proje Tasarımcısı**.  
  
### <a name="to-enable-autostart"></a>AutoStart'ı etkinleştirmek için  
  
1.  Seçili bir proje ile **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.  
  
2.  Tıklatın **Yayımla** sekmesi.  
  
3.  Tıklatın **seçenekleri** düğmesi.  
  
     **Yayımla Seçenekleri** iletişim kutusu görüntülenir.  
  
4.  Tıklatın **dağıtım**.  
  
5.  Seçin **için CD yüklemeleri CD eklendiğinde, Kurulum otomatik olarak Başlat** onay kutusu.  
  
     Uygulama yayımlandığında Autorun.inf dosyası Yayımla konuma kopyalanacak.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: yayımlama sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)