---
title: -Çalıştır (devenv.exe)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- /run Devenv
- run Devenv switch
- applications [Visual Studio], running
- /r Devenv switch
- Devenv, /run switch
- r Devenv switch (/r)
ms.assetid: b1f22f9d-39a5-4918-8a2a-4b5c1e872665
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9e10b12729ed8f547c2658c0f4ce6ece84a12dbe
ms.sourcegitcommit: fe5a72bc4c291500f0bf4d6e0778107eb8c905f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33704635"
---
# <a name="run-devenvexe"></a>/Run (devenv.exe)
Derler ve belirtilen proje ve çözüm çalıştırır.

## <a name="syntax"></a>Sözdizimi

```cmd
devenv {/run|/r} {SolutionName|ProjectName}
```

## <a name="arguments"></a>Arguments
 `SolutionName`

 Gerekli. Tam yol ve çözüm dosya adı.

 `ProjectName`

 Gerekli. Proje dosyası adını ve tam yolu.

## <a name="remarks"></a>Açıklamalar
 Derler ve belirtilen proje ve çözüm etkin çözüm yapılandırması için belirtilen ayarlara göre çalıştırır. Bu anahtar tümleşik geliştirme ortamını (IDE) başlatır ve sonra projeyi etkin bırakır veya çözüm çalıştırma tamamlandı.

-   Çift tırnak işaretleri boşluk dizeler alın.

-   Hatalar dahil olmak üzere Özet bilgileri görüntülenebilir **komutu** penceresinde veya ile belirtilen herhangi bir günlük dosyasını `/out` geçin.

## <a name="example"></a>Örnek
 Bu örnek çözümü çalıştıran `MySolution` etkin Dağıtım Yapılandırması'nı kullanarak.

```cmd
devenv /run "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln"
```

## <a name="see-also"></a>Ayrıca Bkz.

- [Devenv Komut Satırı Anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Runexit (devenv.exe)](../../ide/reference/runexit-devenv-exe.md)
- [/ Yapı (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ Out (devenv.exe)](../../ide/reference/out-devenv-exe.md)