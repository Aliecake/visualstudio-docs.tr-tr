---
title: 'CA2220: Sonlandırıcılar taban Sonlandırıcıları çağırmalıdır | Microsoft Docs'
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
- CA2220
- FinalizersShouldCallBaseClassFinalizer
helpviewer_keywords:
- CA2220
- FinalizersShouldCallBaseClassFinalizer
ms.assetid: 48329f42-170d-45ee-a381-e33f55a240c5
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0489cce326dc74f790a5eb43caf464792733ec67
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223944"
---
# <a name="ca2220-finalizers-should-call-base-class-finalizer"></a>CA2220: Sonlandırıcılar taban tür sonlandırıcıları çağırmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|FinalizersShouldCallBaseClassFinalizer|
|CheckId|CA2220|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Geçersiz kılan bir tür <xref:System.Object.Finalize%2A?displayProperty=fullName> arama <xref:System.Object.Finalize%2A> temel sınıfındaki yöntemi.

## <a name="rule-description"></a>Kural Tanımı
 Sonlandırılma, devralma hiyerarşisi aracılığıyla gönderilmelidir. Bunu sağlamak için kendi temel sınıf türleri çağırmalıdır <xref:System.Object.Finalize%2A> yönteminden kendi içinde <xref:System.Object.Finalize%2A> yöntemi. C# derleyicisi, temel sınıf Sonlandırıcı çağrısını otomatik olarak ekler.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için temel türün çağrı <xref:System.Object.Finalize%2A> yönteminden, <xref:System.Object.Finalize%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Ortak dil çalışma zamanını hedefleyen bazı derleyiciler, Microsoft Ara diline (MSIL) temel türün Sonlandırıcısı için bir çağrı ekleyin. Bu kuraldan bir uyarıyı bildirilirse, derleyici arama eklemez ve kod eklemeniz gerekir.

## <a name="example"></a>Örnek
 Aşağıdaki Visual Basic örnek, bir tür gösterir `TypeB` doğru çağrılarının <xref:System.Object.Finalize%2A> temel sınıfındaki yöntemi.

 [!code-vb[FxCop.Usage.IDisposableBaseCalled#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.IDisposableBaseCalled/vb/FxCop.Usage.IDisposableBaseCalled.vb#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Dispose Deseni](http://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)



