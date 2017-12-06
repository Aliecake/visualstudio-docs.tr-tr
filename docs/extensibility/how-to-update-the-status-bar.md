---
title: "Nasıl yapılır: durum çubuğunu güncelleştirmesine | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
caps.latest.revision: "12"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6218d697880da3ebf0d9af5599b5a7ca37ddf2f9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-update-the-status-bar"></a>Nasıl yapılır: durum çubuğunda güncelleştir
**Durum çubuğu** denetim çubuğu bir veya daha fazla durum metin satırlarını ya da göstergeleri içeren pek çok uygulama penceresi en altında bulunur.  
  
### <a name="to-update-the-status-bar"></a>Durum çubuğu güncelleştirmek için  
  
1.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> form görünümü ve kod görünümü gibi düzenleyicinizi sağlayan her tek tek görünüm nesnesinde (DocView).  
  
2.  IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, bilgileri güncelleştirin **durum çubuğu** yöntemlerinin çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.  
  
    > [!NOTE]
    >  IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yalnızca belge pencerenizi başlangıçta etkinleştirildiğinde. Belge pencerenizi etkin olduğu süre kalanı için güncelleştirmeniz gerekir **durum çubuğu** Düzenleyicisi değişikliklerinizi durumu bilgileri.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 A **durum çubuğu** dört ayrı alanları içerir:  
  
-   Durum metni  
  
-   İlerleme çubuğu  
  
-   Animasyonlu simgesi  
  
-   Düzenleyici bilgileri  
  
 Daha fazla bilgi için bkz: [durum çubukları](/cpp/mfc/status-bars).  
  
 IDE otomatik olarak çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yöntemi, <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> belge pencerenizi etkinleştirildiğinde uygulama.  
  
 VSPackage uygulayan durum çubuğunda durum metni güncelleştirmek için sorumludur. Durum metin alanı boş metin ayarlanmışsa, "Hazır" Bu dizeye IDE sıfırlar ("") boşta kalma zaman.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Durum çubukları](/cpp/mfc/status-bars)