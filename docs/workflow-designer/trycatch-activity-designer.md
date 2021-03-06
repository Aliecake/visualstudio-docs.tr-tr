---
title: İş Akışı Tasarımcısı - TryCatch etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.TryCatch.UI
- System.Activities.Statements.Catch`1.UI
ms.assetid: 02a326c2-4009-442f-b7cb-e42121fd2992
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 26985893ae5a6431743564e28793957ecf0f9e01
ms.sourcegitcommit: 30f653d9625ba763f6b58f02fb74a24204d064ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/25/2018
ms.locfileid: "36756820"
---
# <a name="trycatch-activity-designer"></a>TryCatch Etkinlik Tasarımcısı

**TryCatch** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.TryCatch> etkinlik.

## <a name="the-trycatch-activity"></a>TryCatch etkinliği
 <xref:System.Activities.Statements.TryCatch> Etkinlik içeren bir <xref:System.Activities.Statements.TryCatch.Try%2A> etkinliği, bir koleksiyonu **Catch\<TException >** ve <xref:System.Activities.Statements.TryCatch.Finally%2A> etkinlik. A <xref:System.Activities.Statements.Catch%601> türü **TException** içeren bir <xref:System.Activities.Statements.Catch%601.ExceptionType%2A> ve bir <xref:System.Activities.Statements.Catch%601.Action%2A>. Birlikte bunlar işleme mekanizması tipik bir özel durum tabanlı hata uygulamak için kullanılır. A <xref:System.Activities.Statements.TryCatch> etkinlik çalıştığında yürütmek kendi <xref:System.Activities.Statements.TryCatch.Try%2A> etkinlik. Varsa <xref:System.Activities.Statements.TryCatch.Try%2A> etkinlik tüm özel durumları oluşturur <xref:System.Activities.Statements.TryCatch> etkinliği kullanan kendi **Catch < TException\>**  özel eşleşmesi için koleksiyonu. Bir eşleşme varsa sonra <xref:System.Activities.Statements.Catch%601.Action%2A> ilgili **Catch\<TException >** , özel durum için mantığı işleme hatası olarak hizmet veren yürütülür. Varsa etkinlikler <xref:System.Activities.Statements.TryCatch.Try%2A> bölümü başarıyla tamamlandı veya etkinlikler <xref:System.Activities.Statements.TryCatch.Catches%2A> başarıyla tamamlanması <xref:System.Activities.Statements.TryCatch> etkinlik yürütür kendi <xref:System.Activities.Statements.TryCatch.Finally%2A> etkinlik. Daha fazla bilgi için bkz: [Windows iş akışı özel durumları](/dotnet/framework/windows-workflow-foundation/exceptions).

### <a name="using-the-trycatch-activity-designer"></a>TryCatch etkinlik Tasarımcısı'nı kullanarak

Erişim **TryCatch** etkinlik Tasarımcısı'nda **işleme hatası** kategorisini **araç**.

**TryCatch** gelen etkinlik Tasarımcısı sürüklenebilir **araç** ve etkinlikleri genellikle yerleştirilir olduğunda, örneğin olarak içinde açın iş akışı Tasarımcısı yüzeyini bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu oluşturur bir <xref:System.Activities.Statements.TryCatch> varsayılan etkinlik <xref:System.Activities.Activity.DisplayName%2A> TryCatch biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üstbilgisinde düzenlenebilir **TryCatch** etkinlik Tasarımcısı veya **DisplayName** ve özellik ızgarasının kutusu. Diğer özellikler yüzeyine düzenlenmesi **TryCatch** etkinlik Tasarımcısı.

Sağ üst köşesindeki genişletme düğmeyi tıklatın **TryCatch** görmek için tasarımcı **deneyin**, **yakalar**, ve **son** kutusu Genişletilmiş Görünüm. Bir catch eklemek için tıklatın **yeni yakalama eklemek** düğmesini **TryCatch** Tasarımcısı. Tür birleşik giriş kutusu düğmesine dönüşür. Bir özel durum türü seçin ve yakalama eklemek için ENTER tuşuna basın. Ekledikten sonra bir **Catch**, catch alanı genişler ve yürütme mantığını yakalama tanımlamak için yakalama içine bir etkinlik bırakılabilir. Genişletilmiş catch alanı sağ tarafta bir metin kutusu olduğuna dikkat edin. Bu metin kutusunu kullanarak özel durum değişken adı verebilirsiniz. Özel durum değişken yalnızca aynı içindeki etkinlikler için kullanılabilir **Catch**.

**TryCatch** Tasarımcısı düzenleme desteklemiyor **Catch**. Özel durum türünü değiştirmek istiyorsanız, silmeniz gerekir **Catch** ve yeni bir tane ekleyin. A **Catch** seçip silerek veya kullanarak silinebilir **silmek** menüsünde sağ tıklayarak erişilen bağlamı.

### <a name="the-trycatch-properties"></a>TryCatch özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.TryCatch>özellikleri ve bunların Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik adı|Gerekli|Kullanım|
|-------------------|--------------|-----------|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.TryCatch> etkinlik. TryCatch varsayılandır.|
|<xref:System.Activities.Statements.TryCatch.Try%2A>|False|Etkinlik ilk yürütülmesi <xref:System.Activities.Statements.TryCatch> yürütür.|
|<xref:System.Activities.Statements.TryCatch.Catches%2A>|False|Koleksiyonu **Catch** zaman denetlenecek öğeler <xref:System.Activities.Statements.TryCatch.Try%2A> etkinliği bir özel durum oluşturur.<br /><br /> En az bir etkinlikte eklemeniz gerekir <xref:System.Activities.Statements.TryCatch.Catches%2A> veya bir etkinlikte <xref:System.Activities.Statements.TryCatch.Finally%2A> bloğu.|
|<xref:System.Activities.Statements.TryCatch.Finally%2A>|False|Etkinlik zaman yürütülecek <xref:System.Activities.Statements.TryCatch.Try%2A> ve gerekli tüm etkinlikleri <xref:System.Activities.Statements.TryCatch.Catches%2A> koleksiyonu tam yürütme.<br /><br /> En az bir etkinlikte eklemeniz gerekir <xref:System.Activities.Statements.TryCatch.Catches%2A> veya bir etkinlikte <xref:System.Activities.Statements.TryCatch.Finally%2A> bloğu.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [yeniden oluşturma](../workflow-designer/rethrow-activity-designer.md)
- [throw](../workflow-designer/throw-activity-designer.md)