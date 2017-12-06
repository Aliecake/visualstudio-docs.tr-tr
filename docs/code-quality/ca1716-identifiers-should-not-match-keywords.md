---
title: "CA1716: Tanımlayıcılar anahtar sözcükleri eşleşmemelidir | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
helpviewer_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
caps.latest.revision: "21"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 619fc7867d14a26f2c3b674b4b8ac8b2d8fba114
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="ca1716-identifiers-should-not-match-keywords"></a>CA1716: Tanımlayıcılar anahtar sözcüklerle eşleşmemelidir
|||  
|-|-|  
|TypeName|IdentifiersShouldNotMatchKeywords|  
|CheckId|CA1716|  
|Kategori|Microsoft.Naming|  
|Yeni Değişiklik|Yeni|  
  
## <a name="cause"></a>Sebep  
 Bir ad alanı, bir tür veya viritual veya arabirim üye adı ayrılmış bir anahtar sözcük bir programlama dili eşleşir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Ad alanlarını, türleri için tanımlayıcıları ve sanal ve arabirim üyeleri olmayan ortak dil çalışma zamanı hedef dilleri tarafından tanımlanan anahtar sözcükleri eşleşmelidir. Kullanılan dil ve anahtar sözcüğü bağlı olarak, derleyici hataları ve belirsizlikleri kitaplığı kullanmak zorlaştırabilir.  
  
 Bu kural, anahtar sözcükler aşağıdaki dillerde karşı denetler:  
  
-   Visual Basic  
  
-   C#  
  
-   C++/CLI  
  
 Büyük küçük harf duyarsız karşılaştırma için kullanıldığından [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] anahtar sözcükleri ve büyük küçük harfe duyarlı karşılaştırma diğer diller için kullanılır.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Anahtar sözcükler listesinde görünmeyen bir ad seçin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Tanımlayıcı API kullanıcılarının karıştırır değil ve kitaplık tüm kullanılabilir dilde kullanılabilir olduğunu ikna varsa bir uyarı bu kuraldan gizleyebilirsiniz [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)].