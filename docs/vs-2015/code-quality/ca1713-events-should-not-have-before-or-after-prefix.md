---
title: 'CA1713: Olaylarda önce veya sonra önek olmamalıdır | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- EventsShouldNotHaveBeforeOrAfterPrefix
- CA1713
helpviewer_keywords:
- CA1713
- EventsShouldNotHaveBeforeOrAfterPrefix
ms.assetid: 855772a4-aa9e-410b-88c1-c5fba1ca63da
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 9046c5ecd247b5648e9b0e9923f51f9f6c962c44
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49238387"
---
# <a name="ca1713-events-should-not-have-before-or-after-prefix"></a>CA1713: Olaylarda önce veya sonra önek olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|EventsShouldNotHaveBeforeOrAfterPrefix|
|CheckId|CA1713|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Olay adı, 'Before' veya 'After' ile başlar.

## <a name="rule-description"></a>Kural Tanımı
 Olay adları olayı oluşturan eylem açıklamalıdır. Belirli bir sırayla ilgili olayları adlandırmak için şimdiki veya geçmiş zamanı göreceli konumun sıralı eylemlerini belirtmek için kullanın. Olay çifti adlandırma kaynak kapatırken oluştuğunda, örneğin, 'Kapanış' ve 'Kapalı' yerine 'BeforeClose' ve 'AfterClose' adını.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Olay adı ön ekini kaldırın ve mevcut ya da bir fiil, geçmiş şimdiki kullanılacak adını değiştirmeyi göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.



