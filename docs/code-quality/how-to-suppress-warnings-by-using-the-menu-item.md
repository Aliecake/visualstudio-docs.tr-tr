---
title: "Nasıl yapılır: menü öğesini kullanarak uyarıları bastırma | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- warnings, suppressing
- code analysis, suppressing warnings
ms.assetid: 36bd1850-dcde-4ed0-9bc3-0b83df434362
caps.latest.revision: "24"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a197170285a8f8a9d3f0cc01638557f30fd1f126
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-suppress-warnings-by-using-the-menu-item"></a>Nasıl yapılır: Menü Öğesini Kullanarak Uyarıları Bastırma
> [!NOTE]
>  Kaynak gizleme web sitesi projeleri için desteklenmiyor.  
  
 Kod çözümleme uyarıları gizlemek için Kod Analizi penceresini kullanabilirsiniz. Bir uyarı gizleme devre dışı bırakmasını ile aynı değil. Bir uyarı bastırma ihlali yalnızca belirli bir örneğine uygulanır. Aynı uyarı diğer ihlalleri hala hata listesi penceresini raporlanır.  
  
 Kod çözümleme çalıştırdıktan sonra bir veya daha fazla kod Analizi penceresinde görüntülenen Kod Analizi uyarıları uygulamanıza uygun olmadığını belirleyebilirsiniz. Örneğin, kodun doğru olduğunu belirleyebilirsiniz. Veya, bazı ihlalleri düşük öncelik ve geçerli geliştirme döngüsü sabit olmayan bir durum olabilir. Bir nedenle bağımsız olarak uyarı kodu gözden geçirildi ve bu uyarıyı atlanması belirlendi bilmeniz ekip üyelerinizin izin vermek için geçerli olmayan olduğunu göstermek sık faydalı olur. Kaynağındaki uyarı oluşturulduğu yakın bir gizleme koymadan izin verdiğinden gizleme yararlıdır.  
  
 Gizleme kaynak kodu veya genel gizleme dosyasında görüntülenip görüntülenmeyeceğini seçebilirsiniz. Bazı suppressions genel gizleme dosyasında yer almalıdır. Bu durumda, ise **içinde kaynak** seçeneği devre dışı bırakılacak.  
  
### <a name="to-suppress-a-warning-by-using-menu-item"></a>Menü öğesini kullanarak bir uyarıyı gizlemek için  
  
1.  Üzerinde **Çözümle** menüsünde seçin **Windows** ve ardından **Kod Analizi**.  
  
2.  İçinde **Kod Analizi** penceresinde, uyarı gösterme seçin.  
  
3.  Eylemler seçin ve ardından **bastırmak iletileri**ve ardından seçin **içinde kaynak** veya **proje gizleme dosyasını**.  
  
     Belirli uyarı gizlenen ve üzeri Kod Analizi penceresinde bir uyarı görüntülenir.  
  
> [!NOTE]
>  Bir hedef yok suppressions genel gizleme dosyasında görünür.