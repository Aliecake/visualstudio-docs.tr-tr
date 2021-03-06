---
title: 'CA1821: Boş sonlandırıcıları kaldırın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- RemoveEmptyFinalizers
- CA1821
helpviewer_keywords:
- CA1821
ms.assetid: 3f4855a0-e4a0-46e6-923c-4c3b7074048d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c67cd83f8487b67c580d544fd2d350612dfb48a8
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45549644"
---
# <a name="ca1821-remove-empty-finalizers"></a>CA1821: Boş sonlandırıcıları kaldırın
|||
|-|-|
|TypeName|RemoveEmptyFinalizers|
|CheckId|CA1821|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir tür boş, yalnızca temel tür Sonlandırıcı çağırır veya yöntemleri koşullu olarak yayınlanan yalnızca çağıran sonlandırıcıyı uygular.

## <a name="rule-description"></a>Kural açıklaması
 Güncelleştirirken, nesne kullanım süresini izleme söz konusu olduğunda ek performans yükü nedeniyle sonlandırıcılardan kaçının. Nesne topladığı önce çöp toplayıcının sonlandırıcıyı çalışacak. Başka bir deyişle, iki koleksiyon nesnesi toplamak için gerekli olacaktır. Boş Sonlandırıcı eklenen yükü hiçbir avantajı bu artmasına neden olur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Boş Sonlandırıcı kaldırın. Bir sonlandırıcı hata ayıklama için gereklidir, içindeki tüm Sonlandırıcı içine `#if DEBUG / #endif` yönergeleri.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural bir iletiden bastırmayın. Sonlandırma bastırmak için hata performansınızın ve hiçbir avantaj sağlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kaldırılacak boş Sonlandırıcı, içinde içine alınması bir sonlandırıcıyı gösterir `#if DEBUG / #endif` yönergeleriyle birlikte kullanan bir sonlandırıcı `#if DEBUG / #endif` yönergeleri doğru.

 [!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../code-quality/codesnippet/CSharp/ca1821-remove-empty-finalizers_1.cs)]