---
title: Etki alanına özgü diller hakkında | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Domain-Specific Language
ms.assetid: 29e5b6f2-ece4-4f3b-ab08-5f957418702f
caps.latest.revision: 28
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 0a9d3b89e91e0540766621f0889a12482291740a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49175272"
---
# <a name="about-domain-specific-languages"></a>Etki Alanına Özgü Diller Hakkında
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

C# veya UML gibi genel amaçlı bir dil, bir etki alanına özgü dil (DSL), belirli bir sorun alanı veya etki alanı deyimlerinde express için tasarlanmıştır.  
  
 İyi bilinen DSL'ler normal ifadeler ve SQL içerir. Her DSL kendi kapsamı dışındaki fikirleri tanımlamak için metin dizelerini veya bir veritabanı, ancak çok daha da kötüsü işlemleri tanımlamak için genel amaçlı bir dil daha çok daha iyidir. Tek tek sektörler kendi DSL'ler de vardır. Örneğin, telekomünikasyon sektörün dilleri yaygın bir telefon aramasıyla durumları dizisini belirtin ve sektör havada seyahat için kullanılan açıklama DSL uçuş kayıtları tanımlamak için kullanılan standart bir çağırın.  
  
 İşletmenizi ve projenize DSL ile açıklanan kavramlar özel kümeleri de ilgilidir. Örneğin, bu uygulamaların biri için bir DSL tanımlayabilirsiniz:  
  
-   Bir Web sitesinde gezinti yolları planı.  
  
-   Bağlantı şemaları elektronik bileşenleri için.  
  
-   Taşıyıcı bantları bagaj havaalanı ekipman işleme ve ağlar.  
  
 Bir DSL tasarlarken, tanımladığınız bir *etki alanı sınıfı* her etki alanında, bir Web sayfası, lamp veya havaalanı iade masasına gibi önemli kavramları. Tanımladığınız *etki alanı ilişkileri* köprü, hat üzeri ya da kavramları birbirine bağlamak için bir taşıyıcı bandı gibi.  
  
 Kullanıcılar, DSL'nin oluşturma *modelleri.* Modelleri *örnekleri* , DSL. Örneğin, bunlar belirli bir Web sitesi ya da belirli bir cihaz ya da belirli bir Havalimanı sistemindeki işleme bagaj kablolama açıklanmaktadır.  
  
 Kullanıcıların bir modeli bir diyagram veya bir Windows form olarak görüntüleyebilirsiniz. Modelleri, XML olarak nasıl depolandığını olduğu de görüntülenebilir. Bir DSL tanımlarken, her bir etki alanı sınıfı ve ilişki örnekleri kullanıcının ekranda görüntülenme şeklini tanımlar. Tipik bir DSL simgeleri veya dikdörtgenler oklarla bağlı koleksiyonu olarak görüntülenir.  
  
 Aşağıdaki şekilde grafiksel bir DSL içinde küçük bir modeli gösterilmektedir:  
  
 ![Tudor Aile Ağacı Modeli](../modeling/media/tudor-familytreemodel.png "Tudor_FamilyTreeModel")  
  
## <a name="what-you-can-do-with-dsls"></a>DSL ile yapabilecekleriniz  
 Program kodu veya diğer yapıları üretmek için DSL'nin tipik bir uygulamasıdır. DSL'nizi tanımladığınızda, tanımlayabileceğiniz *metin şablonlarını* DSL modeli okumak ve metin dosyaları oluşturur.  
  
 Örneğin, bir Havalimanı planı alın ve bagaj, bazı plan açıklayan kullanıcı belgelerin yanı sıra işleme yazılımı parçası oluşturacak şablonları yazabilirsiniz.  
  
 Bir DSL tanımlandığında, kendi bilgisayarlarına yükleyebilmek için diğer kullanıcılara dağıtabilirsiniz. Kullanıcılar, DSL'nin oluşturabilir ve düzenleyebilir modellerinde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
 Menü komutları da tanımlayabilirsiniz ve kullanıcılara yardımcı olan diğer araçlar DSL DSL doğru şekilde kullanılır ve yeni örnekleri kullanıcılara yardımcı olmak ve öğe şablonları oluşturma sağlamaya yardımcı olmak için doğrulama kısıtlamaları düzenleyin. Bir veya birden çok DSL araçları ve diğer kayabilir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] uzantıları olarak tümleşik bir pakette.  
  
 Genellikle, birden çok ürünlerin benzer bir kod yazmak bir geliştirme ekibi sahip bir etki alanına özgü dil oluşturulur. Örneğin, işleme sistemlerini bagaj uzmanlaşmış bir şirket bunlar bazı yüklemeler için kod oluşturmak bagaj izleme DSL tanımlayabilirsiniz. DSL avantajları, bunu anladım, müşterileri tarafından ondan oluşturulan kodu güvenilirdir ve müşterilerin gereksinimlerinizin değişmesi durumunda sistemin hızla güncelleştirilmesi ' dir.  
  
 [!INCLUDE[dsl](../includes/dsl-md.md)] kendi grafik tasarımcı ve kendi diyagram gösterimi sahip bir etki alanına özgü dil oluşturma ve ardından her proje için uygun kaynak kodu oluşturmak için dil kullanmanıza olanak tanır.  
  
## <a name="domain-specific-development"></a>Etki alanına özgü geliştirme  
 Etki alanına özgü geliştirme etki alanına özgü bir dili kullanarak dil oluşturmak ve uygulama geliştiricilerine dağıtma modellenebilir uygulamalarınızı bölümlerini tanımlayan işlemidir. Geliştiriciler, uygulamalarına özgü modelleri, kaynak kodu oluşturmak için modelleri kullanır ve ardından uygulama geliştirmek için kaynak kodunu kullanma için etki alanına özgü dil kullanın.  
  
## <a name="aspects-of-graphical-domain-specific-development"></a>Grafik etki alanına özgü geliştirme yönleri  
 Bir grafik etki alanına özgü dil aşağıdaki özellikleri içermelidir:  
  
-   Gösterim  
  
-   Etki alanı modeli  
  
-   Yapıt oluşturma  
  
-   Serileştirme  
  
-   Visual Studio ile Tümleştirme  
  
### <a name="notation"></a>Gösterim  
 Bir etki alanına özgü dil makul küçük bir kolayca tanımlanabilir ve etki alanına özgü yapıları temsil etmek için genişletilmiş öğeler olması gerekir. Bir gösterimi öğelerini temsil eden, şekiller ve bağlayıcıları, bir grafik diyagram yüzeyinde öğeleri arasındaki ilişkileri gösteren oluşur. İçinde [!INCLUDE[dsl](../includes/dsl-md.md)], şekiller genişletilmiş ve, etki alanına özgü dil öğelerini temsil eden için iyileştirilmiştir.  
  
### <a name="domain-model"></a>Etki alanı modeli  
 Bir etki alanına özgü dil öğelerini ve bunları tutarlı dilbilgisi arasındaki ilişkileri kümesini birleştirmeniz gerekir. Öğeleri ve ilişkileri birleşimlerini geçerli olup olmadığını tanımlamalısınız. Örneğin, programlama dilleri, genellikle ikinci sınıftan türetilmiş bir sınıf ve saniye sınıfının ilk sınıfından türetilmiş döngüsel devralmaya engelleyin. Kısıtlamaları, iş mantığı ifade etmek için de kullanılabilir; örneğin, bir kişi, kendisine bağımlı bir olamaz. [!INCLUDE[dsl](../includes/dsl-md.md)] tür en etki alanına özgü diller gerektiren kısıtlamalar express için kısıtlamalar kullanır.  
  
### <a name="artifact-generation"></a>Yapıt oluşturma  
 Bir etki alanına özgü dil ana amacı, bir yapı, örneğin, kaynak kodu, bir XML dosyasına veya diğer bir kullanışlı verileri oluşturmaktır. Genellikle, modeldeki bir değişiklik yapının bir değişiklik anlamına gelir. Kullanabileceğiniz [!INCLUDE[dsl](../includes/dsl-md.md)] yapıtları oluşturmaya ve model değiştirdiğinizde bunları yeniden oluşturmak.  
  
### <a name="serialization"></a>Serileştirme  
 Bir etki alanına özgü dil düzenlendi, kaydedildi, kapalı, yeniden ve bazı biçiminde kalıcı gerekir. [!INCLUDE[dsl](../includes/dsl-md.md)] tanımlama ve alana özgü dilinizi nasıl serileştirilecek veya kalıcı özelleştirme olanak sağlayan bir XML biçimini kullanır.  
  
### <a name="integration-with-visual-studio"></a>Visual Studio ile Tümleştirme  
 Çünkü [!INCLUDE[dsl](../includes/dsl-md.md)] barındırılan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], birçok genişletir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] windows ve denetimleri. Ayrıca menü komutları, araç kutusu öğeleri ve diğer öğeleri kullanıcı arabiriminin davranışını özelleştirmenizi sağlar.  
  
 Bu gibi durumlarda, bir Model veri yolu bağdaştırıcısı Ayrıca, etki alanına özgü dil için oluşturabilirsiniz. Bu bağdaştırıcı başvuru bir model ve erişmek ve DSL örneği güncelleştirme kod yazma sağlar ve bir modeli öğeleri sağlar. Yazabileceğiniz güçlü Model veri yolu mekanizması kullanarak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] birden çok modellerle çalışmanıza uzantıları. Modellerle çalışmanıza tek başına uygulamalar da yazabilirsiniz. Daha fazla bilgi için [Visual Studio Modelbus kullanarak modelleri tümleştirme](../modeling/integrating-models-by-using-visual-studio-modelbus.md).  
  
## <a name="benefits-of-domain-specific-development"></a>Etki alanına özgü geliştirme avantajları  
 Bir etki alanına özgü dil aşağıdaki faydaları sağlayabilir:  
  
-   Sorun alanı tam olarak sığması yapıları içerir.  
  
     Genel amaçlı dillerden farklı olarak, bir etki alanına özgü dil öğeleri ve doğrudan sorun alanı mantığı temsil eden ilişkiler oluşur. Örneğin, bir sigorta ilke uygulama ilkeleri ve talep öğeler içermesi gerekir. Bir etki alanına özgü dil, uygulama ve Bul ve hataları mantığı tasarlamak kolaylaştırır.  
  
-   Geliştirici olmayan ve genel tasarımı anlama etki alanı bilmiyorsanız kişilere izin verir.  
  
     Bir grafik etki alanına özgü dili kullanarak, etki alanı görsel bir temsilini Geliştirici olmayan uygulama tasarımını kolayca anlayabilmeniz oluşturabilirsiniz.  
  
-   Son uygulama prototipini oluşturmayı kolaylaştırır.  
  
     Geliştiriciler, istemcilere göstermek bir prototip uygulaması oluşturmak için model oluşturan kodu kullanabilirsiniz.  
  
## <a name="the-process-of-domain-specific-development"></a>Etki alanına özgü geliştirme işlemi  
 Etki alanına özgü diller kullanan çoğu yazılım geliştirme takımları, oluşturmak ve modellerini kullanmak için aşağıdaki adımları izleyin:  
  
-   Takım, etki alanı bölümlerinden asla değiştirme değişkeni bölümlerini birbirinden ayırır.  
  
-   Geliştiriciler, sabit bölümleri için kod yazma ve değişken parçaları için uzantı noktaları bırakın.  
  
-   Yazılım geliştiricisi veya mimari tasarım desenlerini sabit bölümlerini etki alanı ve değişken parçaları için uzantı noktaları içeren bir etki alanına özgü dil oluşturur.  
  
-   Yazılım geliştiricisi veya Mimarı ekip oluşturan çeşitli uygulamaların geliştiricileri için etki alanına özgü dil dağıtır.  
  
-   Her geliştirici, belirli bir uygulamaya uygulanan bir model oluşturur.



