---
title: "SetEnv görevi | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.task.setenv
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), tasks
- SetEnv task (MSBuild (Visual C++))
ms.assetid: fd9e4225-68cb-4608-8b27-468b0218c936
caps.latest.revision: "6"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 0223d57cf4c16166149b1fc9e8903f563b724d20
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="setenv-task"></a>SetEnv Görevi
Ayarlar veya belirtilen ortam değişkeninin değeri siler.  
  
## <a name="parameters"></a>Parametreler  
 Aşağıdaki tabloda parametrelerinin açıklanmaktadır **SetEnv** görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|**Ad**|Gerekli **dize** parametresi.<br /><br /> Bir ortam değişkeni adı.|  
|**OutputEnvironmentVariable**|İsteğe bağlı **dize** çıkış parametresi.<br /><br /> Tarafından belirtilen ortam değişkenine atanan değeri içeren **adı** parametresi.|  
|**Önek**|Zorunlu `Boolean` parametresi.<br /><br /> Varsa `true`, değerini art arda ekler **değeri** parametresi tarafından belirtilen ortam değişkeninin değerini önce **adı** parametresi ve ardından sonucu ortama atar değişkeni. Varsa `false`, yalnızca değeri atar **değeri** ortam değişkeni parametresi.|  
|**Hedef**|İsteğe bağlı **dize** parametresi.<br /><br /> Bir ortam değişkeni depolanacağı konumu belirtir. Belirtin "`User`"veya"`Machine`".<br /><br /> Daha fazla bilgi için "EnvironmentVariableTarget numaralandırma" bakın [MSDN](http://go.microsoft.com/fwlink/?LinkId=737) Web sitesi.|  
|**Değer**|İsteğe bağlı **dize** parametresi.<br /><br /> Tarafından belirtilen ortam değişkenine atanan değeri **adı** parametresi. Varsa **değeri** boş ve değişken var, değişkeni silinir. Değişkeni yoksa, işlem gerçekleştirilemiyor olsa bile hata oluşmaz.<br /><br /> Daha fazla bilgi için "Environment::SetEnvironmentVariable yöntemi" bakın [MSDN](http://go.microsoft.com/fwlink/?LinkId=737) Web sitesi.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)