---
title: 'Hata: Uzak bilgisayar DCOM iletişimini başlatamadı | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.unmarshal_callback_failed
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: bbba0766-2502-4ef1-a75d-bf1f0db39e37
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 59c4be18adc854e326b8e756399818d46ba469ad
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49237932"
---
# <a name="error-remote-computer-could-not-initiate-dcom-communications"></a>Hata: Uzak bilgisayar DCOM iletişimini başlatamadı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uzak makinede yerel makine ile iletişim kurmak çalışırken bir DCOM hatası oluştu. Yerel makine olduğu makinedir  
  
 Visual Studio çalışıyor. Bu hata, çeşitli nedenlerle oluşabilir:  
  
-   Yerel makine etkin bir güvenlik duvarı vardır.  
  
-   Yerel makinede uzak makineden Windows kimlik doğrulaması çalışmıyor.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Yerel makinede Windows Güvenlik duvarı varsa, bkz. [ayarlanmış yukarı uzak Araçlar cihazda](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c) yerel hata ayıklama için güvenlik duvarını yapılandırma hakkında yönergeler için.  
  
2.  Uzak sunucudan yerel makine üzerindeki bir dosya paylaşımına açmaya çalışırken tarafından Windows kimlik doğrulamasını Sına.  
  
3.  Windows kimlik doğrulama geri yüklemek için her iki makine yeniden deneyin. Yerel ve Uzak makinelerde Kerberos hataları için olay günlüklerini inceleyin ve bilinen sorunlar için etki alanı yöneticileri ile iletişime geçin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Cihazda uzak araçları ayarlama](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)



