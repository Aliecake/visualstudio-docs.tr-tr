---
title: R araçlarını yükleme
description: R araçları Visual Studio 2017 ve Visual Studio 2015, çevrimdışı yüklemeleri de dahil olmak üzere nasıl yüklenir.
ms.date: 01/24/2018
ms.prod: visual-studio-dev15
ms.technology: vs-rtvs
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- data-science
ms.openlocfilehash: 1b5cc415d95377cdca0d44c31ed2c3b84cd11c5c
ms.sourcegitcommit: 4667e6ad223642bc4ac525f57281482c9894daf4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/20/2018
ms.locfileid: "36296303"
---
# <a name="how-to-install-r-tools-for-visual-studio"></a>R araçları Visual Studio için nasıl yüklenir

Bu makalede:

- [Visual Studio'nun desteklenen sürümleri](#supported-versions-of-visual-studio)
- [Visual Studio 2017 içinde RTVS yükleyin](#installing-rtvs-in-visual-studio-2017)
- [Visual Studio 2015'te RTVS yükleyin](#installing-rtvs-in-visual-studio-2015)
- [Çevrimdışı yükleme](#offline-installation-of-visual-studio-and-rtvs)

> [!Note]
> R araçları yüklendikten sonra bir en iyi duruma getirilmiş veri Bilimcisi düzeni için Visual Studio'yu yapılandırma açıklandığı gibi isteyebilirsiniz [seçenekleri](options-for-r-tools-in-visual-studio.md) makalesi.

## <a name="supported-versions-of-visual-studio"></a>Visual Studio'nun desteklenen sürümleri

R araçları için Visual Studio (RTVS) Community (ücretsiz) ile Windows desteklenir Professional ve Enterprise sürümleri hem [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ve [Visual Studio 2015 güncelleştirme 3 (veya üstü)](http://go.microsoft.com/fwlink/?LinkId=691129) (doğrudan indirme).

RTVS Visual Studio şu anda Mac için desteklenmiyor

Yalnızca Visual Studio, Visual Studio Test uzmanı ve SQL Server Management Studio gibi ürünlerle eklenen Kabuğu varsa RTVS yüklemez. Visual Studio Kabuğu RTVS için gerekli bileşenleri eksik.

## <a name="install-rtvs-in-visual-studio-2017"></a>Visual Studio 2017 içinde RTVS yükleyin

1. Visual Studio yükleyicisi çalıştırmak ve seçmek **Değiştir** seçeneği (Ayrıntılar için bkz [değiştirmek Visual Studio](../install/modify-visual-studio.md)). Visual Studio yüklüyse henüz yoksa bkz [Visual Studio yükleme](../install/install-visual-studio.md). Windows 7'de Visual Studio 2017 sürüm göstermek için yükleyici güncelleştirildiğinden emin olması *15.2 yapı 26430.12* veya sonraki bir sürümü.

1. Seçin **veri bilimi ve analitik uygulamaları** iş yükü:

    ![Veri bilimi ve VS2017 analitik uygulamaları iş yükü](media/installation-data-science-workload.png)

1. Aynı iş yükünü adla sağ tarafındaki ek seçenekleri ayarlayın. Varsayılan olarak, bu iş yükü F # içerir ve Python desteği. R için en düşük gereksinimler verilmiştir **R dil desteği**, **R geliştirmesi için çalışma zamanı desteği**, ve **Microsoft R istemci**.

RTVS yüklenir: *% ProgramFiles (x86) %\Microsoft Visual Studio\<sürüm >\<edition > Common7\IDE\Extensions\Microsoft\R araçları Visual Studio için* nerede  *\<sürüm >* genellikle `2017` ve  *\<edition >* olan `Community`, `Professional`, veya `Enterprise`.

## <a name="install-rtvs-in-visual-studio-2015"></a>Visual Studio 2015'te RTVS yükleyin

Visual Studio 2015 ile birlikte bir R yorumlayıcı ve R araçları ayrı olarak yüklemeniz gerekir.

### <a name="install-an-r-interpreter"></a>Bir R yorumlayıcıyı yükleyin

RTVS R sürüm 3.2.1 64-bit yüklemesini gerektirir ya da daha yüksek bir veya daha fazla aşağıdaki kaynaklardan gelen:

- [Microsoft R Aç](https://mran.microsoft.com/download/)
- [Microsoft R istemci](/machine-learning-server/r-client/what-is-microsoft-r-client)
- [CRAN R](https://cran.r-project.org/bin/windows/base/)

Microsoft R açık ve CRAN R her ikisini birden çok yan yana sürümleri için izin verir. Microsoft R istemci, ancak yalnızca bir sürümü destekler ve her zaman yüklü en son olanı kullanır.

### <a name="install-the-r-tools"></a>R Araçları'nı yükleme

Geçerli RTVS Visual Studio 2015'ten indirin [ https://aka.ms/rtvs-current ](https://aka.ms/rtvs-current). RTVS Visual Studio'nun uygun bir sürümünü denetler ve henüz yapmadıysanız bir R yorumlayıcı yüklemenize yardımcı olur.

> [!Note]
> Tek başına RTVS yükleyici yalnızca Visual Studio 2015 ile birlikte çalışır; Visual Studio 2017 ile R desteğini yükleme [veri bilimi ve analitik uygulamaları iş yükü](#installing-rtvs-in-visual-studio-2017) daha önce açıklandığı gibi.

Visual Studio 2015 için RTVS yüklenir: `%ProgramFiles(x86)%\Microsoft Visual Studio 14\Common7\IDE\Extensions\Microsoft\R Tools for Visual Studio`

## <a name="offline-installation-of-visual-studio-and-rtvs"></a>Visual Studio ve RTVS çevrimdışı yükleme

Çevrimdışı yükleme, Internet'e bağlı olmayan bilgisayarlar için uygundur:

1. Visual Studio sürümünüze çevrimdışı yükleyici oluşturmak için yönergeleri izleyin:

    - [Visual Studio 2017](../install/create-an-offline-installation-of-visual-studio.md)
    - [Visual Studio 2015](https://msdn.microsoft.com/library/mt706497.aspx)

1. Visual Studio 2015 için çevrimdışı RTVS yükleyicileri gelen indirme [ https://aka.ms/rtvs-current-zip ](https://aka.ms/rtvs-current-zip) ve [ https://aka.ms/rtvs-remote-zip ](https://aka.ms/rtvs-remote-zip).

1. Visual Studio ve RTVS çevrimdışı yükleyicileri yükleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [R ile çalışmaya başlama](getting-started-with-r.md)
- [R araçları örnek projeler](getting-started-samples.md)
- [R araçlarında Yardım](getting-started-help.md)
- [R Araçlar Seçenekler](options-for-r-tools-in-visual-studio.md)
- [Microsoft Machine Learning Server (önceki adıyla R Server)](/machine-learning-server/)