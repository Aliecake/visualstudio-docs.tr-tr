---
title: 'Hata: Microsoft Visual Studio uzaktan hata ayıklama İzleyicisi uzak bilgisayarda bu bilgisayara bağlanma izni yok | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.error.access_denied_oncallback
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, Windows version error
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 266a301bca4953066621d759518c1754052dfeb2
ms.sourcegitcommit: eefffa7ebe339d1297cdc12f51a813e7849d7e95
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2018
ms.locfileid: "34177975"
---
# <a name="error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-does-not-have-permission-to-connect-to-this-computer"></a>Hata: Uzak bilgisayardaki Microsoft Visual Studio Uzaktan Hata Ayıklama İzleyicisinin bu bilgisayara bağlanma izni yok.
Visual Studio uzaktan hata ayıklama İzleyicisi (msvsmon) çalıştırmayı denediğinizde kullanıcının yerel bilgisayarda bir hesabı yoksa bu hata oluşur.  
  
### <a name="to-fix-this-problem"></a>Bu sorunu gidermek için  
  
-   Visual Studio hata ayıklayıcısı ana bilgisayar ile aynı adı ve parola msvsmon uzak bilgisayarda çalışan kullanıcı hesabı olarak bir kullanıcı hesabı eklemek,  
  
     \- veya -  
  
-   Msvsmon yerel bilgisayara çağırma izni olan bir kullanıcı olarak çalıştırın. Başka bir deyişle, kullanıcının bir etki alanı kullanıcısı ve msvsmon bilgisayarda yönetici olması gerekir. Msvsmon iki yoldan biriyle çalıştırmak için kullanıcı hesabı belirtebilirsiniz:  
  
    -   Msvsmon simgesini sağ tıklatın ve seçin **Çalıştır** kısayol menüsünde  
  
     \- veya -  
  
    -   Komut istemine `runas.exe`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan hata ayıklama](../debugger/remote-debugging.md)