---
title: "Deyimi değerlendir komutu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: debug.evaluatestatement
helpviewer_keywords:
- Debug.EvaluateStatement command
- Evaluate Statement command
ms.assetid: 032039bc-9477-4f93-9b9d-66d4be0e90f4
caps.latest.revision: "12"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 46c80a49d0e043d7cdbffbc74698a29e10ab4795
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="evaluate-statement-command"></a>Deyimi Değerlendir Komutu
Değerlendirir ve belirli deyim görüntüler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Debug.EvaluateStatement text   
```  
  
## <a name="arguments"></a>Arguments  
 `text`  
 Gerekli. Değerlendirilecek ifade.  
  
## <a name="remarks"></a>Açıklamalar  
 Girmek için kullanılan penceresi **EvaluateStatement** komutu belirleyen bir eşittir işareti (=) bir karşılaştırma işleci veya atama işleci olarak yorumlanır.  
  
 İçinde **komutu** penceresinde, bir eşittir işareti (=) bir karşılaştırma işleci yorumlanır. Örneğin, bunu, değişkenlerin değerleri `a` ve `b` farklı, sonra komutu  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 bir değeri döndürür `false`.  
  
 İçinde **hemen** penceresinde, buna karşın bir eşittir işareti (=) atama işleci yorumlanır. Bu nedenle, örneğin, komutu  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 değişkene atar `a` değişkenin değerini `b`.  
  
## <a name="example"></a>Örnek  
  
```  
>Debug.EvaluateStatement(a+b)  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yazdır komutu](../../ide/reference/print-command.md)   
 [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)   
 [Komut penceresi](../../ide/reference/command-window.md)   
 [Bul/komut kutusu](../../ide/find-command-box.md)   
 [Visual Studio komut diğer adları](../../ide/reference/visual-studio-command-aliases.md)