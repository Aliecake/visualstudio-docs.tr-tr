---
title: 'DA0003: Pek çok çekirdek örneği | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.rules.DA0003
- vs.performance.DA0003
- vs.performance.3
- vs.performance.rules.DAManyKernelSamples
ms.assetid: c1f46f77-eb95-42e5-b340-d86bc9de41b4
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fd4412fc120eb0a0fa039ac91bec4da4ba4a6f44
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42695210"
---
# <a name="da0003-many-kernel-samples"></a>DA0003: Pek çok çekirdek örneği
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda en son sürümünü şu yolda bulunabilir: [DA0003: pek çok çekirdek örneği](https://docs.microsoft.com/visualstudio/profiling/da0003-many-kernel-samples).  
  
Kural Kimliği | DA0003 |  
| Kategori | Profil oluşturma araçları kullanım |  
| Profil oluşturma yöntemlerini | Örnekleme |  
| İleti | Çekirdek modunda bir yüksek oranda örnekleri var. Bu, yüksek hacimli g/ç etkinliğinin veya yüksek oranda bağlam belirtebilir. Uygulamanızı Instrumentation Mode kullanarak yeniden profil oluşturmayı göz önünde bulundurun. |  
| Kural türü | Bilgi |  
  
## <a name="cause"></a>Sebep  
 Uygulama için toplanan çağrı yığını örnekleri önemli bir kısmı çekirdek modunda yürütülüyor. Farklı bir profil oluşturma yöntemini kullanarak uygulamanızın profilini oluşturmanız göz önünde bulundurun.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Windows çekirdek modu veya kullanıcı modu kod çalıştırılabilir. (Çekirdek modu da ayrıcalıklı modu olarak adlandırılır.) Bir cihaz sürücüleri gibi alt düzey sistem kodu yalnızca çekirdek modunda çalışır. Bir kullanıcı modu uygulaması için iş parçacığı veya işlem eşitleme temellerine bekleyin ya da sistem çağrıları yapmak için g/ç işlemleri gerçekleştirmek için çekirdek moduna geçiş yapabilirsiniz.  
  
 Örnekleme, kullanıcı modunda çalışmayı yapan zamanlarının çoğunu harcama uygulamaları profil oluştururken en etkili olur. Uygulama çekirdek modunda yürütülürken toplanan örneklerin sayısı sık g/ç işlemleri belirtebilir veya anahtarlarının oluşan bu bağlamı gösterebilir. Bu işlemlerin hiçbiri örnekleme metodu kullanılarak araştırılabilir. Çok fazla sayıda çekirdek modu örneği alınır, örnekleme verileri istatistiksel açıdan anlamlı olması için yeterli kullanıcı modu örnekleri içerebilir.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Uygulamanız aşağıdaki seçeneklerden birini kullanarak yeniden profil oluşturmayı göz önünde bulundurun:  
  
-   İzleme metodunu kullanarak profili.  
  
-   Daha fazla örnek kullanıcı modunda toplanacak denemek için örnekleme hızını artırın.


