---
title: 'CA1710: Tanımlayıcılar doğru soneke sahip | Microsoft Docs'
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
- CA1710
- IdentifiersShouldHaveCorrectSuffix
helpviewer_keywords:
- IdentifiersShouldHaveCorrectSuffix
- CA1710
ms.assetid: 2b8e6dce-b4e8-4a66-ba9a-6b79be5bfe8c
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 45687b8997f66002a3ae7ae4e94a4d81c63320c8
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49305415"
---
# <a name="ca1710-identifiers-should-have-correct-suffix"></a>CA1710: Tanımlayıcıların sonekleri doğru olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|IdentifiersShouldHaveCorrectSuffix|
|CheckId|CA1710|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Tanımlayıcının doğru son ekine sahip değil.

## <a name="rule-description"></a>Kural Tanımı
 Kural gereği, belirli temel türleri genişleten veya bazı arabirimleri ya da bu türlerden türetilmiş türleri uygulayan tür adları, temel tür veya arayüzden son eke sahiptir.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

 Aşağıdaki tabloda, sonekleri ilişkilendirdiğiniz arabirimleri ve temel türleri listeler.

|Temel tür arabirimi|Son eki|
|--------------------------|------------|
|<xref:System.Attribute?displayProperty=fullName>|Öznitelik|
|<xref:System.EventArgs?displayProperty=fullName>|EventArgs|
|<xref:System.Exception?displayProperty=fullName>|Özel Durum|
|<xref:System.Collections.ICollection?displayProperty=fullName>|Koleksiyon|
|<xref:System.Collections.IDictionary?displayProperty=fullName>|Sözlük|
|<xref:System.Collections.IEnumerable?displayProperty=fullName>|Koleksiyon|
|<xref:System.Collections.Queue?displayProperty=fullName>|Koleksiyon veya kuyruk|
|<xref:System.Collections.Stack?displayProperty=fullName>|Koleksiyon veya yığını|
|<xref:System.Collections.Generic.ICollection%601?displayProperty=fullName>|Koleksiyon|
|<xref:System.Collections.Generic.IDictionary%602?displayProperty=fullName>|Sözlük|
|<xref:System.Data.DataSet?displayProperty=fullName>|DataSet|
|<xref:System.Data.DataTable?displayProperty=fullName>|Koleksiyon ya da DataTable|
|<xref:System.IO.Stream?displayProperty=fullName>|Akış|
|<xref:System.Security.IPermission?displayProperty=fullName>|İzin|
|<xref:System.Security.Policy.IMembershipCondition?displayProperty=fullName>|Koşul|
|Bir olay işletici temsilcisi.|EventHandler|

 Türleri uygulayan <xref:System.Collections.ICollection> ve sözlük, yığın ve kuyruk, izin verilen türde hedeflenen kullanım hakkında anlamlı bilgiler sağlayan adları gibi veri yapısı, genelleştirilmiş bir tür.

 Türleri uygulayan <xref:System.Collections.ICollection> ve belirli öğeleri koleksiyonu 'Collection' sözcüğü ile biten olur. Örneğin, bir koleksiyonunu <xref:System.Collections.Queue> nesneleri, 'QueueCollection' adına sahip. Bir koleksiyonun üyelerini kullanarak numaralandırılabilir 'Collection' soneki belirtir `foreach` (`For Each` içinde [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) deyimi.

 Türleri uygulayan <xref:System.Collections.IDictionary> bile türü de uygular, word 'Sözlüğü' ile biten adlarında <xref:System.Collections.IEnumerable> veya <xref:System.Collections.ICollection>. Aşağıdaki iki sabit listesi modelleri arasında ayrım yapmak kullanıcılar 'Collection' ve 'Sözlüğü' soneki adlandırma kurallarını etkinleştirin.

 Bu numaralandırma düzeni 'Collection' soneki türleriyle izleyin.

```
foreach(SomeType x in SomeCollection) { }
```

 Bu numaralandırma düzeni 'Sözlüğü' soneki türleriyle izleyin.

```
foreach(SomeType x in SomeDictionary.Values) { }
```

 A <xref:System.Data.DataSet> nesnesi bir koleksiyonunu içerir <xref:System.Data.DataTable> koleksiyonları oluşan nesneler <xref:System.Data.DataColumn?displayProperty=fullName> ve <xref:System.Data.DataRow?displayProperty=fullName> nesneleri, diğerlerinin yanı sıra. Bu koleksiyonlardaki uygulamak <xref:System.Collections.ICollection> temel aracılığıyla <xref:System.Data.InternalDataCollectionBase?displayProperty=fullName> sınıfı.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Böylece, doğru terimiyle olark türü yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Tür, genişletilmiş veya çeşitli öğeleri bir rastgele kümesini tutacak genelleştirilmiş bir veri yapısı ise 'Collection' soneki kullanmak için bir uyarıyı bastırmak güvenlidir. Bu durumda, uygulama, performans veya veri yapısının diğer özellikleri hakkında anlamlı bilgiler sağlayan bir ad (örneğin, BinaryTree) mantıklı olabilir. Sonek türü kullanarak numaralandırılabilecek belirttiğinden türü (örneğin, StringCollection) belirli bir türün koleksiyonu temsil ettiği durumlarda, bu kuraldan bir uyarıyı bastırmayın bir `foreach` deyimi.

 Diğer sonekleri için bu kuraldan bir uyarıyı bastırmayın. Sonek hedeflenen kullanım tür adından yetkisiz değiştirmeye karşı korumalı olmasını sağlar.

## <a name="related-rules"></a>İlgili kuralları
 [CA1711: Tanımlayıcıların sonekleri yanlış olmamalıdır](../code-quality/ca1711-identifiers-should-not-have-incorrect-suffix.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Öznitelikleri](http://msdn.microsoft.com/library/ee0038ef-b247-4747-a650-3c5c5cd58d8b) [NIB: olayları ve temsilciler](http://msdn.microsoft.com/en-us/d98fd58b-fa4f-4598-8378-addf4355a115)



