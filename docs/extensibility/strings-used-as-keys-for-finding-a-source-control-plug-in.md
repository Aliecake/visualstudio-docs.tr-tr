---
title: "Kaynak denetimi eklenti bulmak için anahtar olarak kullanılan dizeleri | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: source control plug-ins, strings used for finding
ms.assetid: c1e31f76-42a1-4c3d-afb2-664044ef12fd
caps.latest.revision: "15"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d2ee5e741466b7976c8b397928cd9fccd12472fe
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="strings-used-as-keys-for-finding-a-source-control-plug-in"></a>Kaynak denetimi eklenti bulmak için anahtar olarak kullanılan dizeleri
Kaynak denetimi hakkında bilgi eklenti bulmak için kayıt defteri erişim tuşları dizelerdir.  
  
 `STR_SCC_PROVIDER_REG_LOCATION`, `STR_PROVIDERREGKEY`, `STR_SCCPROVIDERPATH`, ve `STR_SCCPROVIDERNAME` kayıt defteri anahtarlarını ya da bir DLL Visual Studio için kaynak denetimi eklenti kaydetmek için kullanılan değerler.  
  
 `SCC_PROJECTNAME_KEY`, `SCC_PROJECTAUX_KEY`, `SCC_KEY, SCC_FILE_SIGNATURE`, ve `SCC_STATUS_FILE` MSSCCPRJ biçimlerinin tanımlamak için kullanılır. SCC dosyası.  
  
## <a name="string-keys-and-values"></a>Dize anahtarları ve değerleri  
  
|Anahtar|Değer|  
|---------|-----------|  
|`STR_SCC_PROVIDER_REG_LOCATION`|Software\SourceCodeControlProvider|  
|`STR_PROVIDERREGKEY`|ProviderRegKey|  
|`STR_SCCPROVIDERPATH`|SCCServerPath|  
|`STR_SCCPROVIDERNAME`|SCCServerName|  
|`STR_SCC_INI_SECTION`|Kaynak kodu denetimi|  
|`STR_SCC_INI_KEY`|SourceCodeControlProvider|  
|`SCC_PROJECTNAME_KEY`|SCC_Project_Name|  
|`SCC_PROJECTAUX_KEY`|SCC_Aux_Path|  
|`SCC_STATUS_FILE`|MSSCCPRJ. SCC|  
|`SCC_KEY`|SCC|  
|`SCC_FILE_SIGNATURE`|Kaynak kodu denetim dosyası|  
|`SCC_NSE`|Namespace uzantısı|  
|`SCC_NSE_PREFIX`|İletişim kuralı öneki|  
|`SCC_NSE_DisableOpenSCC`|DisableOpenFromSourceControl|  
|`STR_SCCHELPCOLLECTION`|HelpCollection|  
|`STR_UI_LANGUAGE`|UILanguage|  
|`STR_SRCSAFE_ROOT_KEY`|Software\Microsoft\SourceSafe|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetim Eklentileri](../extensibility/source-control-plug-ins.md)   
 [Nasıl yapılır: kaynak denetimi eklentisini yükleme](../extensibility/internals/how-to-install-a-source-control-plug-in.md)   
 [MSSCCPRJ. SCC dosyası](../extensibility/mssccprj-scc-file.md)