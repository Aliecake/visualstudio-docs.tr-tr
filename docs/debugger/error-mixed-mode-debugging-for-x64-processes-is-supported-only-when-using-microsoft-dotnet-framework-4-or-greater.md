---
title: 'Hata: Karışık mod hata ayıklama yalnızca Microsoft .NET Framework 4 kullanırken işlemler desteklenir x64 için veya büyük | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.interop_unsupported_x64
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: d5550383d1d5882d8824ce2d282b2035882cdcef
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31471511"
---
# <a name="error-mixed-mode-debugging-for-x64-processes-is-supported-only-when-using-microsoft-net-framework-4-or-greater"></a>Hata: x64 işlemleri için karışık modda hata ayıklama yalnızca Microsoft .NET Framework 4 veya daha yenisi kullanılırken desteklenir
64 bitlik bir işlem karışık yerel ve yönetilen kodda hata ayıklamak için bilmeniz gereken [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] sürüm 4. 64 bit işlemleri ile karışık mod hata ayıklaması [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] 4 desteklenmiyor'den önceki sürümleri.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Aşağıdaki adımlardan birini uygulayın:  
  
    -   Yükseltme, [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] sürüm 4.  
  
    -   Hata ayıklama için uygulamanızın 32-bit sürümünü oluşturun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama](../debugger/remote-debugging.md)