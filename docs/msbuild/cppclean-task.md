---
title: "CPPClean görevi | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.task.cppclean
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), CPPClean task
- CPPClean task (MSBuild (Visual C++))
ms.assetid: b62a482e-8fb5-4999-b50b-6605a078e291
caps.latest.revision: "5"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 437b4a7e6b1a8e92b4409188655dccdfcb1baf50
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="cppclean-task"></a>CPPClean Görevi
Visual C++ proje yapılandırıldığında MSBuild oluşturduğu geçici dosyaları siler. Derleme dosyaları silme işlemi olarak bilinen *Temizleme*.  
  
## <a name="parameters"></a>Parametreler  
 Aşağıdaki tabloda parametrelerinin açıklanmaktadır **CPPClean** görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|**DeletedFiles**|İsteğe bağlı `ITaskItem[]` çıkış parametresi.<br /><br /> Tüketilen ve görevler tarafından gösterilen MSBuild çıktı dosyası öğeleri dizisi tanımlar.|  
|**DoDelete**|İsteğe bağlı **Boolean** parametresi.<br /><br /> Varsa `true`, temiz geçici dosyaları derleme.|  
|**FilePatternsToDeleteOnClean**|Gerekli `String` parametresi.<br /><br /> Temiz dosyaların dosya uzantıları noktalı virgülle ayrılmış listesini belirtir.|  
|**FilesExcludedFromClean**|İsteğe bağlı `String` parametresi.<br /><br /> Değil temizlemek için dosyaların noktalı virgülle ayrılmış bir listesini belirtir.|  
|**FoldersToClean**|Gerekli `String` parametresi.<br /><br /> Temizlemeye dizinleri noktalı virgülle ayrılmış listesini belirtir. Tam veya göreli bir yol belirtin ve yolun joker karakter sembolünü içerebilir (**\***).|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)