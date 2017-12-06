---
title: "Visual Studio'da renk temasını ve yazı tipleri ayarlama | Microsoft Docs"
ms.custom: 
ms.date: 11/20/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: quickstart
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7adb1ec7badaefceb8430d0fcacd8e54e7404ea7
ms.sourcegitcommit: eb954434c34b4df6fd2264266381b23ce9e6204a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2017
---
# <a name="quickstart-personalize-the-visual-studio-ide-and-editor"></a>Hızlı Başlangıç: Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme

Bu 5-10 dakika quickstart Biz Visual Studio renk temasını ve iki metin renkleri Metin Düzenleyicisi'nde özelleştirme.

## <a name="set-the-color-theme"></a>Renk temasını ayarlayın

Visual Studio 2017 için varsayılan renk temasını adlı **mavi**. Kendisine değiştirelim **koyu**.

1. Menü çubuğunda seçin **Araçları**, **seçenekleri**.

1. Üzerinde **ortam**, **genel** seçenekler sayfası, değişiklik **renk temasını** seçimi **koyu**ve ardından **Tamam** .

   Tüm IDE renk temasını değiştirilir **koyu**.

   ![VS koyu tema içinde](media/quickstart-personalize-dark-theme.png)

> [!TIP]
> Yükleyerek önceden tanımlanmış ek temalar yükleyebilirsiniz **Visual Studio renkli tema Düzenleyicisi** gelen [Visual Studio Market'te](https://marketplace.visualstudio.com/items?itemName=VisualStudioProductTeam.VisualStudio2017ColorThemeEditor). Bu aracı yükledikten sonra ek renk temaları renk temasını aşağı açılan listede görüntülenir.

## <a name="change-text-color"></a>Metin rengi değiştirme

Şimdi biz bazı metin renkleri Düzenleyicisi özelleştirmek. İlk olarak, varsayılan renkleri görmek için bir XML dosyası açalım.

1. Menü çubuğundan seçin **dosya**, **yeni**, **dosya...** .

1. İçinde **yeni dosya** iletişim kutusunda **genel** kategorisi seçin **XML dosyası**ve ardından **açık**.

1. Aşağıdaki XML içeren satırı altına yapıştırın `<?xml version="1.0" encoding="utf-8"?>`.

   ```xml
   <Catalog>
     <Book id="bk101">
     <Author>Garghentini, Davide</Author>
     <Title>XML Developer's Guide</Title>
     <Genre>Computer</Genre>
     <Price>44.95</Price>
     <PublishDate>2000-10-01</PublishDate>
     <Description>
       An in-depth look at creating applications with XML.
     </Description>
   </Book>
   <Book id="bk102">
     <Author>Garcia, Debra</Author>
     <Title>Midnight Rain</Title>
     <Genre>Fantasy</Genre>
     <Price>5.95</Price>
     <PublishDate>2000-12-16</PublishDate>
     <Description>
       A former architect battles corporate zombies, an evil
       sorceress, and her own childhood to become queen of the world.
     </Description>
   </Book>
   </Catalog>
   ```

   Satır numaralarını Turkuaz mavi bir renk, ve xml öznitelikleri açık bir mavi renk olduğundan dikkat edin. Bu öğeler metin rengini değiştirmek olacak.

   ![XML dosyası yazı tipi rengi](media/quickstart-personalize-xml-file.png)

1. Açmak için **seçenekleri** Seç iletişim kutusu, menü çubuğundan **Araçları**, **seçenekleri**.

1. Altında **ortam**, seçin **yazı tiplerini ve renkleri** kategorisi.

   Dikkat altındaki metin **ayarlarını göster** diyor **metin düzenleyici** &mdash; ne istiyoruz budur. Yalnızca Burada yazı tipleri ve metin rengi özelleştirebilirsiniz yerler kapsamlı listesini görmek için açılan listeyi genişletin.

1. Satır numaraları metnin rengini değiştirmek için **görüntülemek öğeleri** listesinde, seçin **satır numarası**. İçinde **öğesi ön plan** kutusunda, seçin **Zeytin**.

   ![Seçenekler iletişim kutusu, yazı tipleri ve renkler kategorisi](media/quickstart-personalize-line-number-color.png)

1. Biz dışında iletişim kutusundan çıkmak önce de XML öznitelikleri rengini değiştirelim. İçinde **görüntülemek öğeleri** listesinde, aşağı kaydırarak **XML özniteliği** ve seçin. İçinde **öğesi ön plan** kutusunda, seçin **açık yeşil**. Seçin **Tamam** bizim seçimlerini kaydetmek ve iletişim kutusunu kapatın.

   Satır numaralarını Zeytin renkli sunulmuştur ve XML öznitelikleri açık, Limon Sarısı yeşil. Bir C++ veya C# kod dosyası gibi başka bir dosya türü açarsanız satır numaralarını da Zeytin rengi görünür görürsünüz.

   ![Yeni yazı tipi renkleri olan XML dosyası](media/quickstart-personalize-xml-file-new-colors.png)

Biz, Visual Studio renkleri özelleştirme yalnızca birkaç yolla incelediniz. Diğer özelleştirme seçeneklerinde incelenecektir umuyoruz **seçenekleri** gerçekten Visual Studio kendi yapmak için iletişim kutusu.

## <a name="see-also"></a>Ayrıca bkz.

[Hızlı Başlangıç: ilk Visual Studio IDE bakma](../ide/quickstart-ide-orientation.md)  
[Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md)  
[Düzenleyiciyi özelleştirme](../ide/customizing-the-editor.md)  
[Visual Studio IDE genel bakış](../ide/visual-studio-ide.md)