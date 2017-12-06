---
title: "Hata ayıklama Visual C++'ta özelliklerini etkinleştirme (-D_DEBUG) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- /D_DEBUG compiler option [C++]
- debugging [C++], enabling debug features
- debugging [MFC], enabling debug features
- assertions, enabling debug features
- D_DEBUG compiler option
- MFC libraries, debug version
- debug builds, MFC
- _DEBUG macro
ms.assetid: 276e2254-7274-435e-ba4d-67fcef4f33bc
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b762f34df693ac3b5992d0b1e9c2ba4fa6fb8cb8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="enabling-debug-features-in-visual-c-ddebug"></a>Visual C++'de Hata Ayıklama Özelliklerini Etkinleştirme (/D_DEBUG)
İçinde [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)], simgenin programınızla derlediğinizde onaylar etkinleştirilen gibi hata ayıklama özellikleri **_DEBUG** tanımlanmış. Tanımlayabileceğiniz **_DEBUG** iki yoldan biriyle:  
  
-   Belirtin **# _DEBUG define** kaynak kodunuzdaki veya  
  
-   Belirtin **/D_DEBUG** derleyici seçeneği. (Sihirbazları, Visual Studio, projenizin oluşturursanız **/D_DEBUG** hata ayıklama yapılandırmasını da otomatik olarak tanımlanır.)  
  
 Zaman **_DEBUG** olan tanımlanan derleyici tarafından çevrelenen kodun bölümlerini derler **#ifdef _DEBUG** ve `#endif`.  
  
 Bir MFC programı hata ayıklama yapılandırmasını MFC kitaplığını hata ayıklama sürümü ile bağlamanız gerekir. MFC başlık dosyaları doğru olan bağlamak için MFC kitaplık tanımladığınız, gibi simgeleri temel sürümünü **_DEBUG** ve **_UNICODE**. Ayrıntılar için bkz [MFC kitaplık sürümleri](/cpp/mfc/mfc-library-versions).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)