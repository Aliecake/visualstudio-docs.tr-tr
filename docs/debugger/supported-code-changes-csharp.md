---
title: "Desteklenen kod değişiklikleri (C# ve Visual Basic) | Microsoft Docs"
ms.custom: 
ms.date: 10/11/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [C#], supported code changes
- Edit and Continue [Visual Basic], supported code changes
ms.assetid: c7a48ea9-5a7f-4328-a9d7-f0e76fac399d
caps.latest.revision: "27"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9a0a7d55b19455e22836d4750c0842a47816ee86
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2017
---
# <a name="supported-code-changes-c-and-visual-basic"></a>Desteklenen kod değişiklikleri (C# ve Visual Basic)
Düzenle ve devam et türlerinin çoğunu kod değişiklikleri yöntem gövdeleri içinde işler. Yöntem gövdeleri dışında çoğu değişiklikler ve yöntem gövdeleri içinde bazı değişiklikler, ancak hata ayıklama sırasında uygulanamaz. Desteklenmeyen bu değişiklikleri uygulamak için hata ayıklamayı durdurun ve kod yeni bir sürümü ile yeniden başlatmanız gerekir.

## <a name="supported-changes-to-code"></a>Desteklenen kod değişiklikleri

Aşağıdaki tablo, C# ve Visual Basic kodu için hata ayıklama oturumu sırasında oturumu yeniden başlatmanıza gerek kalmadan yapılabilir değişiklikleri gösterir.

|Dil öğesi/özelliği|Desteklenen düzenleme işlemi|Sınırlamalar|
|-|-|-|
|Türler|Ekleme yöntemleri, alanları, Oluşturucular, et al|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Yineleyiciler|Ekleme veya değiştirme|Hayır|
|zaman uyumsuz ve bekleme ifadeleri|Ekleme veya değiştirme|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|Dinamik nesneler|Ekleme veya değiştirme|Hayır|
|lambda ifadeleri|Ekleme veya değiştirme|[Evet](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|
|LINQ ifadeleri|Ekleme veya değiştirme|[Lambda ifadeleri aynı](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits)|

> [!NOTE]
> Dize ilişkilendirme ve null-conditional işleçleri gibi daha yeni dil özellikleri genellikle Düzenle ve devam et tarafından desteklenir. En güncel bilgiler için bkz: [Çözücü desteklenen düzenler](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits) sayfası.

## <a name="unsupported-changes-to-code"></a>Desteklenmeyen kod değişiklikleri
 Aşağıdaki değişiklikler için C# ve Visual Basic kodu bir hata ayıklama oturumu sırasında uygulanamaz:  
  
-   Geçerli deyimi veya diğer etkin deyim yapılan değişiklikler.  
  
     Etkin deyimlerin geçerli ifadesine almak için adı veriliyordu işlevleri çağrı yığınında herhangi deyimleri ekleyin.  
  
     Geçerli deyimi sarı bir arka plan kaynak penceresinde olarak işaretlenir. Diğer etkin deyimlerin gölgeli bir arka plan işaretlenir ve salt okunurdur. Bu varsayılan renkler değiştirilebilir **seçenekleri** iletişim kutusu.

- Aşağıdaki tabloda dil öğesi tarafından desteklenmeyen kodunda değişiklik yapılmasını gösterir.

|Dil öğesi/özelliği|Desteklenmeyen düzenleme işlemi|
|-|-|
|Tüm kod öğeleri|Yeniden adlandırma|
|Ad Alanları|Ekle|
|Ad alanlarını, türleri, üyeler|Sil|
|Genel Türler|Ekleme veya değiştirme|
|Arabirimler|Değiştirme|
|Türler|Soyut veya sanal bir üye eklemek için geçersiz kılma ekleyip (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Türler|Yok Edicisi ekleme|
|Üyeler|Katıştırılmış birlikte çalışma türüne başvuran bir üye değiştirme|
|Üyeler (Visual Basic)|On Error veya Resume deyimi sahip bir üye değiştirme|
|Üyeler (Visual Basic)|Bir toplama, Group By, basit katılma veya grup katılma LINQ sorgu yan tümcesi içeren bir üye değiştirme|
|Yöntemler|İmzaları değiştirme|
|Yöntemler|Bir Özet yöntem hale Özet olmayan bir yöntem gövdesi ekleyerek olun|
|Yöntemler|Yöntem gövdesi Sil|
|Öznitelikler|Ekleme veya değiştirme|
|Olayları veya özellikleri|Değiştir tür parametresi, temel türü temsilci türü ya da dönüş türü |
|Operators veya dizin oluşturucular|Değiştir tür parametresi, temel türü temsilci türü ya da dönüş türü |
|catch blokları|Etkin bir deyimi içerdiğinde değiştirme|
|try-catch-finally blokları|Etkin bir deyimi içerdiğinde değiştirme|
|using deyimleri|Ekle|
|zaman uyumsuz yöntemleri/lambdas|Bir listelenen .NET Framework 4 hedefleyen bir projede zaman uyumsuz yöntem/lambda değiştirebilir ve alt (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
|Yineleyiciler|Yineleyici .NET Framework 4 hedefleyen bir projede değiştirebilir ve alt (bkz [ayrıntıları](https://github.com/dotnet/roslyn/wiki/EnC-Supported-Edits))|
  
## <a name="unsafe-code"></a>Güvenli olmayan kod  
 Güvenli olmayan kod değişiklikleri başka bir kısıtlama ile güvenli kodunda değişiklik yapılmasını onunla aynı sınırlamalara sahiptir: Düzenle ve devam et içeren bir yöntemi içinde güvenli olmayan kod değişiklikleri desteklemiyor `stackalloc` işleci.  

## <a name="unsupported-app-scenarios"></a>Desteklenmeyen app senaryoları

Desteklenmeyen uygulamalar ve platformlar ASP.NET 5, Silverlight 5, Windows Phone ve Windows Phone öykünücüsü ve Windows 8.1 içerir.

> [!NOTE]
> Desteklenen uygulamalar dahil UWP Windows 10 ve .NET Framework 4.6 hedef x86 hem x64 uygulamaları (yalnızca masaüstü sürümü .NET Framework'dur) masaüstü veya sonraki sürümleri.
  
## <a name="unsupported-scenarios"></a>Desteklenmeyen senaryolar  
 Düzenle ve devam et aşağıdaki hata ayıklama senaryolarında kullanılabilir değil:  
  
-   Karışık mod (yerel/yönetilen) hata ayıklama.  
  
-   SQL hata ayıklama.  
  
-   Bir Dr hata ayıklama. Watson dökümü.  
  
-   İşlenmeyen bir özel durumdan sonra kod düzenleme zaman "**işlenmeyen özel durum çağrı yığınındaki bırakma**" seçeneği seçili değil.  
  
-   Katıştırılmış çalışma zamanı uygulama hata ayıklama.  
  
-   Ekleme işlemi için bir uygulama kullanarak hata ayıklama (**hata ayıklama > ekleme işlemi için**) seçerek uygulama çalıştırmak yerine **Başlat** gelen **hata ayıklama** menüsü.  
  
-   İyileştirilmiş kodda hata ayıklama.  
  
-   Derleme hataları nedeniyle oluşturmak yeni bir sürüm başarısız olduktan sonra kodunuzu eski bir sürümü hata ayıklama.
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Düzenle ve devam et (Visual C#)](../debugger/edit-and-continue-visual-csharp.md)   
 [Nasıl yapılır: Düzenle kullanın ve devam et (C#)](../debugger/how-to-use-edit-and-continue-csharp.md)