---
title: Gelişmiş Derleme Ayarları İletişim Kutusu (C#)
ms.date: 06/20/2017
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- cs.AdvancedBuildSettings
helpviewer_keywords:
- Build options [C#], advanced
ms.assetid: 141f2dee-1563-4ce6-ba37-32920b082519
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: c39e68c05f438b787bb7a0930f2ad0ba6a324ee1
ms.sourcegitcommit: 0bf2aff6abe485e3fe940f5344a62a885ad7f44e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37057547"
---
# <a name="advanced-build-settings-dialog-box-c"></a>Gelişmiş Derleme Ayarları İletişim Kutusu (C#)

Kullanım **Gelişmiş derleme ayarları** iletişim kutusunun **Proje Tasarımcısı** Proje yapı yapılandırma özelliklerini Gelişmiş belirtmek için. Bu iletişim kutusunu uygulandığı [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] yalnızca projeleri.

## <a name="general"></a>Genel

 Aşağıdaki seçenekler, genel Gelişmiş ayarları ayarlamanıza olanak verir.

 **Dil sürümü** kullanacağı dilin sürümünü belirtir. Bu seçenek yalnızca bir alt kümesini uygulanan özellikler izin vermek veya yalnızca mevcut bir standardı ile uyumlu özellikleri etkinleştirmek için derleyici zorlamak için kullanılabilmesi için özellik kümesi her sürümünde farklıdır. Bu ayar, aşağıdaki seçenekler vardır:

 - **default**

   Geçerli sürüm hedefler.

- **ISO-1** ve **ISO-2**

  ISO-1 ve 2 ISO standart özellikler sırasıyla hedefler.

- **C# [sürüm numarası]**

 Belirli bir C# sürümünü hedefler. Daha fazla bilgi için bkz: [/langversion (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/langversion-compiler-option).


 **İç derleyici hatası raporlama** derleyici hataları Microsoft'a belirtir. Varsa kümesine **istemi** bir iç derleyici hatası oluşursa (varsayılan), bir ileti bir hata raporu elektronik olarak Microsoft'a gönderme seçeneği sunar alacaksınız. Varsa kümesine **Gönder**, bir hata raporu otomatik olarak gönderilir. Varsa kümesine **sıra**, hata raporlarını sıraya alınmış. Varsa kümesine **hiçbiri**, yalnızca derleyicinin metin çıktısı hata bildirilir. Daha fazla bilgi için bkz: [/errorreport (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/errorreport-compiler-option).

 **Denetlemek için aritmetik taşma/underflow** bir tamsayı aritmetiği deyimi kapsamında olmayan olup olmadığını belirtir [işaretli](/dotnet/csharp/language-reference/keywords/checked) veya [denetlenmeyen](/dotnet/csharp/language-reference/keywords/unchecked) anahtar sözcükleri ve, sonuçları bir değer veri aralığının dışında türü bir çalışma zamanı özel durumuna neden olur. Daha fazla bilgi için bkz: [/ checked (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/checked-compiler-option).

 **Mscorlib.dll başvurmadığından** mscorlib.dll tüm tanımlama, programa içe olup olmadığını belirtir <xref:System> ad alanı. Tanımlayın veya kendi oluşturmak istiyorsanız bu kutuyu <xref:System> ad alanı ve nesneleri. Daha fazla bilgi için bkz: [/nostdlib (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/nostdlib-compiler-option).

## <a name="output"></a>Çıkış

 Aşağıdaki seçenekler, Gelişmiş çıktı seçenekleri belirtmenize olanak verir.

 **Hata ayıklama bilgileri** derleyici tarafından oluşturulan hata ayıklama bilgi türünü belirtir. Bir uygulamanın hata ayıklama performansını yapılandırma hakkında daha fazla bilgi için bkz: [bir görüntü Debug kolaylaştırma](/dotnet/framework/debug-trace-profile/making-an-image-easier-to-debug). Bu ayar, aşağıdaki seçenekler vardır:

- **Yok**

  Hiçbir hata ayıklama bilgilerini oluşturulacağını belirtir.

- **Tam**

  Bir hata ayıklayıcısı çalışan programa eklemeyi mümkün kılar.

- **pdbonly**

  Kaynak kodu program hata ayıklayıcısı'ndaki başladı, ancak çalışan program hata ayıklayıcıya eklendiğinde yalnızca assembler görüntülenir, hata ayıklama sağlar.
- **Taşınabilir**

  Üreten bir. PDB dosyası, diğer araçlar sağlayan bir platforma özgü olmayan ve taşınabilir simgesi özellikle hata ayıklayıcıları, ne hakkında bilgi ana yürütülebilir dosyanın ve nasıl üretilmiştir. Bkz: [taşınabilir PDB](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md) daha fazla bilgi için.

- **Katıştırılmış**

  Taşınabilir sembol bilgileri derleme içine katıştırır. Hiçbir dış. PDB dosyası oluşturulur.

Daha fazla bilgi için bkz: [/Debug (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/debug-compiler-option).

**Dosya Hizalama** çıktı dosyasında bölümlerin boyutunu belirtir. Geçerli değerler **512**, **1024**, **2048**, **4096**, ve **8192**. Bu değerleri bayt cinsinden ölçülür. Her bölüm çıkış dosyasının boyutunu etkileyen bu değeri olan bir sınır ile hizalanır. Daha fazla bilgi için bkz: [/filealign (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/filealign-compiler-option).

**Kitaplık taban adresi** tercih edilen temel adrese DLL yükleneceği belirtir. Bir DLL için varsayılan taban adresi belirlediği [!INCLUDE[dnprdnshort](../../code-quality/includes/dnprdnshort_md.md)] ortak dil çalışma zamanı. Daha fazla bilgi için bkz: [/baseaddress (C# Derleyici Seçenekleri)](/dotnet/csharp/language-reference/compiler-options/baseaddress-compiler-option).

## <a name="see-also"></a>Ayrıca Bkz.

- [C# Derleyici Seçenekleri](/dotnet/csharp/language-reference/compiler-options/index)
- [Derleme Sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-page-project-designer-csharp.md)