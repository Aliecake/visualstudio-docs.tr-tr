---
title: Visual Studio'da bir yerel değişken ekleme
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: d028d89f149a2fe444508d09086f6bec2408889e
ms.sourcegitcommit: 206e738fc45ff8ec4ddac2dd484e5be37192cfbd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/03/2018
ms.locfileid: "39511007"
---
# <a name="introduce-a-local-variable-in-visual-studio"></a>Visual Studio'da bir yerel değişken ekleme

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** hemen var olan bir ifade değiştirmek için bir yerel değişken oluşturmanıza olanak tanır.

**Ne zaman:** yerel bir değişkende olsaydı, kolayca daha sonra yeniden kullanılabilen kodlarla koda sahip.

**Neden:** kopyalayın ve sonra işlemi gerçekleştirmek, sonucu yerel bir değişkende depolar ve yerel bir değişken boyunca kullanmanız daha iyi ancak kodu çeşitli konumlarda kullanmak için birden çok kez yapıştırın.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Yeni bir yerel değişkene atamak istediğiniz ifade vurgulayın.

   - C# İÇİN:

    ![Vurgulanmış kodu C#](media/local-highlight-cs.png)

   - Visual Basic:

    ![Vurgulanmış kodu VB](media/local-highlight-vb.png)

1. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
     - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
     - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
     - &nbsp; ![Ampul](media/bulb-cs.png) kırmızı dalgalı çizgi içeren satırda metin imleci ise, sol kenar boşluğunda görünür simge.

   ![Yerel Önizleme Ekle](media/local-preview-cs.png)

1. Seçin **(tüm örnekleri için) bir yerel değişken Ekle '*ifade*'** aşağı açılan menüden.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** Önizleme pencerenin alt kısmındaki bağlantı [tüm değişiklikleri görmek için](../../ide/preview-changes.md) , oluşturulacak, seçim yapmadan önce.

   Yerel değişken, kullanımdan çıkarılan türü ile oluşturulur. Yeni yerel değişkeni, yeni bir ad verin.

   - C# İÇİN:

      ![C# arabirimi sonucu uygulayın](media/local-result-cs.png)

   - Visual Basic:

      ![Uygulama arabirimi sonucu VB](media/local-result-vb.png)

   > [!NOTE]
   > Kullanabileceğiniz **.. .all tekrarlarını...**  menü seçeneğini seçili ifadesi, yalnızca özellikle vurgulanmış bir her örneğini değiştirin.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)