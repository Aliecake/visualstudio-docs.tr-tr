---
title: Visual Studio'da TextTransform yardımcı programı ile dosya oluşturma
ms.date: 03/22/2018
ms.topic: conceptual
helpviewer_keywords:
- text templates, TextTransform utility
- TextTransform.exe
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 6ca9fd11e56631061d86c35f9e6bd686b8750b50
ms.sourcegitcommit: ad5fb20f18b23eb8bd2568717f61edc6b7eee5e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47859386"
---
# <a name="generate-files-with-the-texttransform-utility"></a>TextTransform yardımcı programı ile dosya oluşturma

TextTransform.exe bir metin şablonu dönüştürmek için kullanabileceğiniz bir komut satırı aracıdır. TextTransform.exe çağırdığınızda, bağımsız değişken olarak bir metin şablonu dosyasının adını belirtin. TextTransform.exe metin dönüştürme motoru çağırır ve metin şablonu işler. TextTransform.exe genellikle betiklerin çağrılır. Visual Studio'da ya da yapı işleminde metin dönüştürme gerçekleştirmek için ancak, bu genellikle gerekli değildir.

> [!NOTE]
> Bir yapı işleminin parçası olarak metin dönüştürme gerçekleştirmek istiyorsanız, MSBuild metin dönüştürme görevi kullanılarak göz önünde bulundurun. Daha fazla bilgi için [derleme sürecinde kod oluşturma](../modeling/code-generation-in-a-build-process.md). Visual Studio'nun yüklü olduğu bir makine, bir uygulama ya da metin şablonlarını dönüştürmek Visual Studio uzantısı da yazabilirsiniz. Daha fazla bilgi için [özel konak kullanarak metin şablonlarını işleme](../modeling/processing-text-templates-by-using-a-custom-host.md).

 TextTransform.exe şu dizinde bulunur:

 **\Program Files (x86)\Microsoft Visual Studio\2017\Professional\Common7\IDE**

Professional Edition veya

 **\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\IDE**

 için Enterprise edition.

Visual Studio'nun önceki sürümlerinde, dosya şu konumda bulunur:

**\Program Files (x86)\Common Files\Microsoft Shared\TextTemplating\{version}**

Burada {version} önceki hangi sürümünün yüklü olduğunu bağlıdır.

## <a name="syntax"></a>Sözdizimi

```
TextTransform [<options>] <templateName>
```

### <a name="parameters"></a>Parametreler

|**Bağımsız değişken**|**Açıklama**|
|------------------|---------------------|
|`templateName`|Dönüştürmek istediğiniz şablon dosyasının adını tanımlar.|

|**Seçeneği**|**Açıklama**|
|----------------|---------------------|
|**-out** \<dosya adı >|Dönüşümün çıkış yazıldığı dosya.|
|**-r** \<derleme >|Derleme ve metin şablonu çalıştırmak için kullanılan derleme.|
|**-u** \<ad alanı >|Şablon derlemek için kullanılan bir ad alanı.|
|**-I** \<includedirectory >|Belirtilen metin şablonuna dahil metin şablonlarını içeren bir dizin.|
|**-P** \<referencepath >|Metin şablonu içinde belirtilen derlemeler için ya da kullanarak aramak için bir dizin **- r** seçeneği.<br /><br /> Örneğin, Visual Studio API için kullanılan derlemeler eklemek için kullanın<br /><br /> `-P "%VSSHELLFOLDER%\Common7\IDE\PublicAssemblies"`|
|**-dp** \<processorName >!\< SınıfAdı >! \<assemblyName&#124;codeBase >|Adı, tam tür adı ve özel yönergeler metin şablonu içinde işlemek için kullanılan bir yönerge işlemcisi derlemenin.|
|**-bir** [processorName]! [ directiveName]! \<parameterName >! \<parameterValue >|Bir yönerge işlemcisi için bir parametre değeri belirtin. Yalnızca parametre adı ve değeri belirtirseniz, tüm yönerge işlemcileri için parametre kullanılabilir. Bir yönerge işlemcisi belirtirseniz, yalnızca belirtilen işlemci için kullanılabilir bir parametredir. Bir yönerge adı belirtirseniz, yalnızca belirtilen yönerge işlenirken parametresi kullanılabilir.<br /><br /> Parametre değerlerini bir yönerge işlemcisi veya metin şablonundan erişmek için [ITextTemplatingEngineHost.ResolveParameterValue](https://msdn.microsoft.com/library/microsoft.visualstudio.texttemplating.itexttemplatingenginehost.resolveparametervalue.aspx). Bir metin şablonunda dahil `hostspecific` şablon yönergesinde ve ileti üzerinde çağırmak `this.Host`. Örneğin:<br /><br /> `<#@template language="c#" hostspecific="true"#> [<#= this.Host.ResolveParameterValue("", "", "parameterName") #>]`.<br /><br /> Türü her zaman '!' yönergesi adı ve isteğe bağlı işlemci bile atlarsanız işaretler. Örneğin:<br /><br /> `-a !!param!value`|
|**-h**|Yardım sağlar.|

## <a name="related-topics"></a>İlgili konular

|Görev|Konu|
|----------|-----------|
|Visual Studio çözümü içinde dosyaları oluşturur.|[T4 Metin Şablonları Kullanarak Tasarım Zamanı Kodu Oluşturma](../modeling/design-time-code-generation-by-using-t4-text-templates.md)|
|Kendi veri kaynaklarınızı dönüştürmek için yönerge işlemcileri yazın.|[T4 Metin Dönüştürmeyi Özelleştirme](../modeling/customizing-t4-text-transformation.md)|
|Kendi uygulamanızı metin şablonlarını çağırmak izin veren bir metin şablonu oluşturma barındırıcısı yazın.|[Bir Özel Konak kullanarak Metin Şablonlarını İşleme](../modeling/processing-text-templates-by-using-a-custom-host.md)|