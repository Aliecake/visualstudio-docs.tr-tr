---
title: 'Nasıl yapılır: Visio belgelerini program aracılığıyla kapatma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], closing Visio documents
- Visio [Office development in Visual Studio], closing Visio documents
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: e27b0a19005b7076629f2848f95c8cb5749c096f
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "35677769"
---
# <a name="how-to-programmatically-close-visio-documents"></a>Nasıl yapılır: Visio belgelerini program aracılığıyla kapatma
  Etkin Microsoft Office Visio belgesini kullanarak kapatabilirsiniz `Microsoft.Office.Interop.Visio.Document.Close` yöntemi.  
  
 Bu yöntem hakkında daha fazla ayrıntı için VBA başvuru belgelerine bakın [Microsoft.Office.Interop.Visio.Document.Close](http://msdn.microsoft.com/library/office/ff767415.aspx) yöntemi.  
  
## <a name="close-the-active-document"></a>Etkin belgeyi Kapat  
  
### <a name="to-close-the-active-document"></a>Etkin belgeyi kapatmak için  
  
-   Çağrı `Microsoft.Office.Interop.Visio.Document.Close` etkin belgeyi Kapat için yöntemi.  
  
     Aşağıdaki kod örneğinde kullanmak amacıyla içinde çalıştırın `ThisAddIn` Visio için VSTO eklenti projesinde sınıfı.  
  
     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#7](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#7)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#7](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#7)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visio çözümleri](../vsto/visio-solutions.md)   
 [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md)   
 [Nasıl yapılır: program aracılığıyla yeni Visio belgeleri oluşturma](../vsto/how-to-programmatically-create-new-visio-documents.md)   
 [Nasıl yapılır: program aracılığıyla Visio belgelerini açma](../vsto/how-to-programmatically-open-visio-documents.md)   
 [Nasıl yapılır: program aracılığıyla Visio belgelerini kaydetme](../vsto/how-to-programmatically-save-visio-documents.md)   
 [Nasıl yapılır: program aracılığıyla Visio belgelerini yazdırma](../vsto/how-to-programmatically-print-visio-documents.md)  
  
  