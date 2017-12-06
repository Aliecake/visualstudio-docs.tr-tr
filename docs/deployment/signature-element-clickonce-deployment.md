---
title: "&lt;İmza&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-deployment
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords: <Signature> element [ClickOnce deployment manifest]
ms.assetid: c99b07ad-e8ba-43f2-b0d6-3745e7a7c8b3
caps.latest.revision: "13"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: a60156c77dfc33475d3913c3fed2e30159f03959
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2017
---
# <a name="ltsignaturegt-element-clickonce-deployment"></a>&lt;İmza&gt; öğesi (ClickOnce dağıtımı)
Bu dağıtım bildirimini dijital olarak imzalamak için gerekli bilgileri içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
  
      <Signature>   
   XML signature information   
</Signature>  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bir zarf imzası kullanarak dağıtım bildirimi imzalama isteğe bağlıdır ancak önerilir. XML imzalama hakkında daha fazla bilgi için bkz dosyalarını World Wide Web Konsorsiyumu konusunda açıklandığı öneri, "XML imzası sözdizimi ve işleme," [http://www.w3.org/TR/xmldsig-core/](http://www.w3.org/TR/xmldsig-core/).  
  
 Bildiriminizi imzalamak istiyorsanız, tüm dosyalar için karmaları sağlanmalıdır. Kullanıcılar dosyaların içeriğini doğrulayamaz doğrulayamadığı için bir bildirim karma olmayan dosyalarla imzalanamaz.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği gösterilmektedir bir `Signature` kullanılan bir dağıtım bildirimi öğesinde bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] dağıtım.  
  
```  
<Signature xmlns="http://www.w3.org/2000/09/xmldsig#">  
  <SignedInfo>  
    <CanonicalizationMethod Algorithm=  
           "http://www.w3.org/TR/2001/REC-xml-c14n-20010315" />  
    <SignatureMethod Algorithm=  
           "http://www.w3.org/2000/09/xmldsig#rsa-sha1" />  
    <Reference URI="">  
      <Transforms>  
        <Transform Algorithm=  
           "http://www.w3.org/2000/09/xmldsig#enveloped-signature" />  
      </Transforms>  
      <DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
      <DigestValue>d2z5AE...</DigestValue>  
    </Reference>  
  </SignedInfo>  
  <SignatureValue>  
4PHj6SaopoLp...  
  </SignatureValue>  
  <KeyInfo>  
    <X509Data>  
      <X509Certificate>  
MIIHnTCCBoWgAwIBAgIKJY9+nwAHAAB...  
      </X509Certificate>  
    </X509Data>  
  </KeyInfo>  
</Signature>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md)