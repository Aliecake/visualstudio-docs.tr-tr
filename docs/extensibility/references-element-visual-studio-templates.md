---
title: "Başvuran öğesi (Visual Studio şablonları) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/vstemplate/2005#References
helpviewer_keywords:
- <References> element [Visual Studio Templates]
- References element [Visual Studio Templates]
ms.assetid: 1969146d-46bf-422d-8d46-0e9493925003
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 436b5f745dc9b3b8c135ad111e6e708bbd391b4e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="references-element-visual-studio-templates"></a>References Öğesi (Visual Studio Şablonları)
Şablon projelerine ekler derleme başvurularını gruplandırır.  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<Başvuruları >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<References>  
    <Reference>... </Reference>  
    <Reference>... </Reference>  
    ...  
</References>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Aşağıdaki bölümlerde öznitelik, alt öğeler ve üst öğeler açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Başvuru](../extensibility/reference-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Öğe bir projeye eklendiğinde eklemek için derleme başvurusu belirtir. Bir veya daha fazla olmalıdır `Reference` öğelerinde bir `References` öğesi.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Şablon içeriğini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 `References`bir isteğe bağlı bir alt öğenin `TemplateContent`.  
  
 `Reference` Ve `References` öğeleri sahip .vstemplate dosyaları yalnızca kullanılabilir bir `Type` öznitelik değerini `Item`.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek gösterilmektedir `TemplateContent` bir öğe şablonu öğesidir. Bu XML System.dll ve System.Data.dll derleme başvurularını ekler.  
  
```  
<TemplateContent>  
    <References>  
        <Reference>  
            <Assembly>  
                System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
        <Reference>  
            <Assembly>  
                System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
    </References>  
    ...  
</TemplateContent>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)