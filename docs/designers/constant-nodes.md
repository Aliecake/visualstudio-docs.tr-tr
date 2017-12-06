---
title: "Sabit düğüm | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-designers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2c798a50-a2d7-459b-9879-ad4ad8290c9b
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a47eb4e129ac90e8a397c936922a8cc3aeb80277
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="constant-nodes"></a>Sabit Düğümler
Gölgelendirici Tasarımcısı'nda sabit düğümleri değişmez değerleri temsil eder ve köşe öznitelikleri piksel gölgelendirici hesaplamalarda Ara değerli. Köşe öznitelikleri ilişkilendirileceğini çünkü — ve bu nedenle, her bir piksel için farklı — her piksel gölgelendirici örneği sabiti farklı bir sürümünü alır. Bu her piksel benzersiz bir görünümünü sağlar.  
  
## <a name="vertex-attribute-interpolation"></a>Köşe özniteliği ilişkilendirme  
 Nesne sayısı matematiksel dönüştürerek bir oyun ya da uygulama 3B Sahne görüntüsü yapılan — köşeleri, köşe öznitelikleri ve temel tanımları tarafından tanımlanan — içine ekrandaki piksel. Tüm bir piksel benzersiz görünümünü sağlamak için gerekli olan bilgileri oluşturan farklı köşeleri piksel yakınlığını göre birlikte karıştırılan köşe öznitelikleri aracılığıyla sağlanmaktadır kendi *ilkel*. Basit bir tür bir temel işleme öğedir; diğer bir deyişle, basit bir noktası, bir satırı veya bir üçgen gibi şekil. Bu köşe neredeyse aynıdır sabitleri çok yalnızca biri köşeleri yakın bir piksel alır ancak bu köşeleri ortalaması olan sabitleri tüm köşe ilkel arasında eşit aralıklı bir piksel alır. Grafik programlamaya piksel alma sabitleri yereldir *Ara değerli*. Bu şekilde piksel sabit verileri sağlayan çok iyi bir görsel kalite oluşturur ve aynı anda bellek kaplama alanı ve bant genişliği gereksinimlerini azaltır.  
  
 Her piksel gölgelendirici örneği yalnızca bir sabit değerleri kümesi alır ve bu değerleri değiştiremezsiniz, ancak farklı piksel gölgelendirici örnekleri farklı sabit veri kümelerinin alırsınız. Bu tasarım basit her piksel için farklı bir renk bir çıktı oluşturmak bir gölgelendirici programı sağlar.  
  
## <a name="constant-node-reference"></a>Sabit düğüm başvurusu  
  
|Düğüm|Ayrıntılar|Özellikler|  
|----------|-------------|----------------|  
|**Kamera vektör**|Kameraya dünya uzayındaki geçerli piksel genişletir vektörü.<br /><br /> Dünya uzayındaki yansımaları hesaplamak için bunu kullanabilirsiniz.<br /><br /> **Çıktı**<br /><br /> `Output`: `float3`<br /> Geçerli piksel öğesinden kameraya.|Yok.|  
|**Renk sabiti**|Bir sabit renk değeri.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Renk değeri.|**Çıktı**<br /> Renk değeri.|  
|**Sabit**|Sabit skaler bir değer.<br /><br /> **Çıktı**<br /><br /> `Output`: `float`<br /> Sayı değeri.|**Çıktı**<br /> Sayı değeri.|  
|**2B sabiti**|İki bileşen vektör sabit.<br /><br /> **Çıktı**<br /><br /> `Output`: `float2`<br /> Vektör değeri.|**Çıktı**<br /> Vektör değeri.|  
|**3B sabiti**|Üç bileşeni vektör sabit.<br /><br /> **Çıktı**<br /><br /> `Output`: `float3`<br /> Vektör değeri.|**Çıktı**<br /> Vektör değeri.|  
|**4D sabiti**|Dört bileşen vektör sabit.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Renk değeri.|**Çıktı**<br /> Vektör değeri.|  
|**Normalleştirilmiş konumu**|Normalleştirilmiş aygıt koordinatları olarak ifade edilen geçerli piksel konumu.<br /><br /> X ekseni ve y koordinatını aralığında değerlere sahip [-1, 1], z koordinatı aralığında bir değere sahip [0, 1] ve görünüm alanı; noktası derinlik değerini w bileşeni içerir w normalleştirilmiş değil.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Geçerli piksel konumu.|Yok.|  
|**Nokta rengi**|Malzeme dağıtma renk ve köşe renk öznitelikleri birleşimi geçerli piksel dağıtma rengi.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Geçerli piksel dağıtma rengi.|Yok.|  
|**Noktası derinliği**|Görünüm alanında geçerli piksel derinliği.<br /><br /> **Çıktı**<br /><br /> `Output`: `float`<br /> Geçerli piksel derinliği.|Yok.|  
|**Normalleştirilmiş noktası derinliği**|Normalleştirilmiş aygıt koordinatları olarak ifade edilen geçerli piksel derinliği.<br /><br /> Sonuç aralığında bir değere sahip [0, 1].<br /><br /> **Çıktı**<br /><br /> `Output`: `float`<br /> Geçerli piksel derinliği.|Yok.|  
|**Ekran konumu**|Ekran koordinatları olarak ifade edilen geçerli piksel konumu.<br /><br /> Ekran koordinatları geçerli görünüm penceresinin üzerinde temel alır. X ve y bileşenleri içeren ekran koordinatları, z bileşeni için bir aralığı normalleştirilmiş derinliği içerir [0, 1] ve görünüm boşluk derinliği değeri w bileşeni içerir.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Geçerli piksel konumu.|Yok.|  
|**Yüzey Normal**|Nesne alanı geçerli piksel yüzey normal.<br /><br /> Aydınlatma Katkıları ve yansımalarını boşlukta hesaplamak için bunu kullanabilirsiniz.<br /><br /> **Çıktı**<br /><br /> `Output`: `float3`<br /> Geçerli piksel yüzey normal.|Yok.|  
|**Eğim alanı kamera vektör**|Kameraya Eğim alanda geçerli piksel genişletir vektörü.<br /><br /> Eğim alanda yansımaları hesaplamak için bunu kullanabilirsiniz.<br /><br /> **Çıktı**<br /><br /> `Output`: `float3`<br /> Geçerli piksel öğesinden kameraya.|Yok.|  
|**Eğim alanı hafif yönü**|Açık, geçerli piksel Eğim alanındaki ışık kaynağından dönüştürüldüğüne yönü tanımlar vektörü.<br /><br /> Eğim alanı aydınlatma ve aynasal katkı hesaplamak için bunu kullanabilirsiniz.<br /><br /> **Çıktı:**<br /><br /> `Output`: `float3`<br /> Geçerli piksel öğesinden ışık kaynağına.|Yok.|  
|**Dünya Normal**|Dünya uzayındaki geçerli piksel yüzey normal.<br /><br /> Aydınlatma katılımlar ve dünya uzayındaki yansımaları hesaplamak için bunu kullanabilirsiniz.<br /><br /> **Çıktı**<br /><br /> `Output`: `float3`<br /> Geçerli piksel yüzey normal.|Yok.|  
|**Dünya konumu**|Konumu geçerli piksel world alanı.<br /><br /> **Çıktı**<br /><br /> `Output`: `float4`<br /> Geçerli piksel konumu.|Yok.|