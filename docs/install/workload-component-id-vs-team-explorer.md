---
title: Visual Studio Takım Gezgini 2017 iş yükü ve Bileşen kimlikleri
description: Tümleşik test araçları için genel test edicileri sağlamak için Visual Studio iş yükü ve Bileşen kimlikleri kullanın
keywords: ''
author: TerryGLee
ms.author: tglee
manager: douge
ms.date: 08/14/2018
ms.topic: reference
helpviewer_keywords:
- workload ID, Visual Studio
- component ID, Visual Studio
- install Visual Studio, administrator guide
ms.service: ''
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.assetid: c6ef9a3b-d13d-49b4-9faa-51fa06b21e1f
ms.workload:
- multiple
ms.openlocfilehash: 4fd77a40f68dcdf15868da7da9292feb05e07153
ms.sourcegitcommit: 6b092e7d466377f06913d49d183dbbdca16730f0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43139107"
---
# <a name="visual-studio-team-explorer-2017-component-directory"></a>Visual Studio Takım Gezgini 2017 bileşen dizini

Tabloları bu sayfa listesi kimliklerinin komut satırını kullanarak Visual Studio'yu yüklemek için kullanabilirsiniz veya bağımlılık VSIX bildirimi olarak belirtebilirsiniz. Visual Studio güncelleştirmeleri yayınlayabilir gibi ek bileşenler ekleyeceğiz olduğunu unutmayın.

Ayrıca sayfa hakkında aşağıdakileri unutmayın:

* Her iş yükü, izlediği iş yükü kimliği ve iş yükü için kullanılabilir olan bileşenlerin bir tablo, kendi bölümü vardır.
* Varsayılan olarak, **gerekli** bileşenleri, iş yükünü yüklediğinizde yüklenir.
* Kullanmayı tercih ederseniz de yükleyebilirsiniz **önerilen** ve **isteğe bağlı** bileşenleri.
* Her türlü iş yükü ile bağlı olmayan ek bileşenleri listeleyen bir bölüm de ekledik.

VSIX bildiriminizi bağımlılıkları oluşturduğunuzda, Bileşen kimlikleri yalnızca belirtmeniz gerekir. Tablolar, sunduğumuz en az Bileşen bağımlılıkları belirlemek için bu sayfada kullanın. Bazı senaryolarda, bir iş yükü yalnızca bir bileşenden belirttiğiniz gelebilir. Diğer senaryolarda, tek bir iş yükünü birden fazla bileşenlerini veya birden çok iş yükü birden çok bileşenlerini belirttiğiniz gelebilir. Daha fazla bilgi için bkz [nasıl yapılır: Visual Studio 2017'ye geçirme genişletilebilirlik projeleri](../extensibility/how-to-migrate-extensibility-projects-to-visual-studio-2017.md) sayfası.

Bu kimliklerinin kullanma hakkında daha fazla bilgi için bkz. [Visual Studio 2017'yi yükleme komut satırı parametreleri kullanmak](use-command-line-parameters-to-install-visual-studio.md) sayfası. Ve iş yükü ve Bileşen kimlikleri diğer ürünlere yönelik bir listesi için bkz. [Visual Studio 2017 iş yükü ve Bileşen kimlikleri](workload-and-component-ids.md) sayfası.

## <a name="visual-studio-core-editor-included-with-visual-studio-team-explorer-2017"></a>(Visual Studio Takım Gezgini 2017 ile dahil) visual Studio temel Düzenleyicisi

**ID:** Microsoft.VisualStudio.Workload.CoreEditor

**Açıklama:** söz dizimine duyarlı kod düzenleme, dahil olmak üzere Visual Studio temel Kabuk deneyimi, kaynak kodu denetimi ve iş öğesi yönetimi.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Visual Studio temel Düzenleyicisi | 15.8.27729.1 | Gerekli
Microsoft.VisualStudio.Component.StartPageExperiment.Cpp | Visual Studio başlangıç sayfasını C++ kullanıcılar | 15.0.27128.1 | İsteğe Bağlı

## <a name="unaffiliated-components"></a>Kullanıcıyla bağlantılı olmayan bileşenleri

Bu, her türlü iş yükü ile dahil edilmez, ancak tek bir bileşeni olarak seçilebilir bileşenlerdir.

Bileşen kimliği | Ad | Sürüm
--- | --- | ---
yok | yok | yok

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio iş yükü ve bileşen kimlikleri](workload-and-component-ids.md)
* [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
  * [Komut satırı parametresi örnekleri](command-line-parameter-examples.md)
* [Visual Studio’nun çevrimdışı yüklemesini oluşturma](create-an-offline-installation-of-visual-studio.md)
