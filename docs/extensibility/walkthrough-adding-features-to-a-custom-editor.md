---
title: 'İzlenecek yol: Bir özel düzenleyiciye özellik ekleme | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], custom - add features
ms.assetid: bfe083b6-3e35-4b9c-ad4f-b30b9ff412a5
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d93861fc6238949d8666072b0bf5a5cc7efdb87b
ms.sourcegitcommit: 1c2ed640512ba613b3bbbc9ce348e28be6ca3e45
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/03/2018
ms.locfileid: "39498947"
---
# <a name="walkthrough-add-features-to-a-custom-editor"></a>İzlenecek yol: özel bir düzenleyici özellikleri ekleyin
Özel bir düzenleyici oluşturduktan sonra daha fazla özellik ekleyebilirsiniz.  
  
## <a name="to-create-an-editor-for-a-vspackage"></a>VSPackage için bir düzenleyici oluşturmak için  
  
1.  Visual Studio Paketi proje şablonunu kullanarak bir özel düzenleyici oluşturma.  
  
     Daha fazla bilgi için [izlenecek yol: özel bir düzenleyici oluşturmak](../extensibility/walkthrough-creating-a-custom-editor.md).  
  
2.  Düzenleyici tek bir görünüm veya birden çok görünüm desteklemek için istediğinize karar verin.  
  
     Destekleyen bir düzenleyici **yeni pencere** komutunu veya form görünümü ve kod görünümü, ayrı bir belge veri nesneleri ve belge görünümü nesneleri gerektirir. Yalnızca tek bir görünümde destekleyen bir düzenleyicide belge veri nesnesi ve belge view nesnesinin aynı nesne üzerinde uygulanabilir.  
  
     Birden çok görünüm örneği için bkz: [birden çok belge görünümünü desteklemek](../extensibility/supporting-multiple-document-views.md).  
  
3.  Bir düzenleyici fabrikası ayarıyla uygulamak <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory> arabirimi.  
  
     Daha fazla bilgi için [Düzenleyici fabrikaları](../extensibility/editor-factories.md).  
  
4.  Yerinde etkinleştirme kullanmak üzere istediğiniz veya Basitleştirilmiş belge görünümü nesne penceresi yönetmek için ekleme isteyip istemediğinize karar.  
  
     Yerinde etkinleştirme düzenleyici penceresinde bir ActiveX denetimi veya diğer etkin bir nesne, belge görünümü olarak sunarken bir standart belge görünümü basitleştirilmiş bir gömme Düzenleyicisi penceresini barındırır. Daha fazla bilgi için [Basitleştirilmiş ekleme](../extensibility/simplified-embedding.md) ve [yerinde etkinleştirme](../extensibility/in-place-activation.md).  
  
5.  Uygulama <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> komutları işlemek için arabirim.  
  
6.  Belge Kalıcılık ve dış dosya değişikliklere yanıt sağlar:  
  
    1.  Dosya kalıcı hale getirmek için uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2> ve <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat> Düzenleyicisi'nin belge verileri nesne üzerinde.  
  
    2.  Dış dosya değişikliklerine yanıt verme uygulamak <xref:Microsoft.VisualStudio.Shell.Interop.IVsFileChangeEx> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsDocDataFileChangeControl> Düzenleyicisi'nin belge verileri nesne üzerinde.  
  
        > [!NOTE]
        >  Çağrı `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.SVsFileChangeEx> işaretçisi almak için `IVsFileChangeEx`.  
  
7.  Belge düzenleme olaylarını kaynak kodu denetimi ile koordine edin. Aşağıdaki adımları uygulayın:  
  
    1.  Bir işaretçi alma `IVsQueryEditQuerySave2` çağırarak `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.SVsQueryEditQuerySave>.  
  
    2.  İlk düzenleme olay gerçekleştiğinde çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> yöntemi.  
  
         Bu yöntem henüz kullanıma alınmışsa, dosyayı kullanıma denetlemek için kullanıcıya sorar. "Dosyayı kullanıma alınmamış" durumu hatalarını engellemeye emin olun.  
  
    3.  Benzer şekilde, dosyayı kaydetmeden önce arama <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFile%2A> yöntemi.  
  
         Bu yöntem, kaydedilmediyse veya son kaydetme işleminden sonra değiştirdiyseniz dosyayı kaydetmek ister.  
  
8.  Etkinleştirme **özellikleri** Metin Düzenleyicisi'nde seçili özelliklerini görüntülemek için penceresi. Aşağıdaki adımları uygulayın:  
  
    1.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.ITrackSelection.OnSelectChange%2A> her zaman metin seçimi, geçirme uygulamanızda değişiklikleri <xref:Microsoft.VisualStudio.Shell.Interop.ISelectionContainer>.  
  
    2.  Çağrı `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.STrackSelection> bir işaretçi alma için hizmet <xref:Microsoft.VisualStudio.Shell.Interop.ITrackSelection>.  
  
9. Düzenleyici arasında öğeleri sürükleyip vermesine olanak sağlayan ve **araç kutusu**, ya da (Microsoft Word gibi) dış düzenleyicileri arasında ve **araç kutusu**. Aşağıdaki adımları uygulayın:  
  
    1.  Uygulama `IDropTarget` IDE düzenleyicinizi bir bırakma hedefi uyarmak için Düzenleyici üzerinde.  
  
    2.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsToolboxUser> düzenleyiciniz etkinleştirebilir ve öğeleri devre dışı bırakmak için Görünüm arabirimdeki **araç kutusu**.  
  
    3.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.ResetDefaults%2A> ve çağrı `QueryService` üzerinde <xref:Microsoft.VisualStudio.Shell.Interop.SVsToolbox> bir işaretçi alma için hizmet <xref:Microsoft.VisualStudio.Shell.Interop.IVsToolbox2> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsToolbox3> arabirimleri.  
  
         Bu adımlar için yeni öğeler eklemek, VSPackage etkinleştirmek **araç kutusu**.  
  
10. Herhangi bir isteğe bağlı özellikler düzenleyiciniz için istediğinize karar verin.  
  
    -   Desteklemek için düzenleyicinizi istiyorsanız bulun ve komutların yerini, uygulama <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>.  
  
    -   Bir belge Anahat araç penceresinin düzenleyicinizde kullanmak istiyorsanız, uygulama `IVsDocOutlineProvider`.  
  
    -   Durum Çubuğu Düzenleyicisi'nde kullanmak istiyorsanız, uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> ve çağrı `QueryService` için <xref:Microsoft.VisualStudio.Shell.Interop.SVsStatusbar> işaretçisi almak için `IVsStatusBar`.  
  
         Örneğin, bir düzenleyici satırı görüntüleyebilirsiniz / sütun bilgileri, seçim modu (akışı / kutusuna) ve ekleme modu (ekleme / OVERSTRIKE).  
  
    -   Desteklemek için düzenleyicinizi istiyorsanız `Undo` komutu, önerilen yöntem, OLE geri alma yöneticisi modeli kullanmaktır. Alternatif olarak, düzenleyici tanıtıcı olabilir `Undo` doğrudan komutu.  
  
11. Bilgi, GUID'leri VSPackage'ı, menüler, düzenleyici ve diğer özellikler dahil olmak üzere kayıt defteri oluşturun.  
  
     Koyabilirsiniz koduna ilişkin genel bir örnek verilmiştir, *.rgs* düzgün bir düzenleyici kaydetme göstermek için betik dosyası.  
  
    ```csharp  
    NoRemove Editors  
    {  
          ForceRemove {...guidEditor...} = s 'RTF Editor'  
          {  
             val Package = s '{...guidVsPackage...}'  
             ForceRemove Extensions  
             {  
                val rtf = d 50  
             }  
          }  
    }  
    NoRemove Menus  
    {  
          val {...guidVsPackage...} = s ',203,11'  
    }  
    ```  
  
12. Bağlama duyarlı Yardım desteği uygulayın.  
  
     Bu adım öğeleri düzenleyicinizde dinamik Yardım penceresi F1 Yardımı ve desteği sağlamak sağlar. Daha fazla bilgi için [nasıl yapılır: bağlam sağlamak için düzenleyicileri](../extensibility/how-to-provide-context-for-editors.md).  
  
13. Otomasyon nesne modeli, düzenleyicisinden uygulayarak kullanıma `IDispatch` arabirimi.  
  
     Daha fazla bilgi için [Otomasyon modeline katkıda bulunma](../extensibility/internals/contributing-to-the-automation-model.md).  
  
## <a name="robust-programming"></a>Güçlü programlama  
  
-   IDE çağırdığında Düzenleyici örneği oluşturulan <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi. Düzenleyici birden çok görünüm destekliyorsa `CreateEditorInstance` belge verileri hem belge görünümü nesneleri oluşturur. Belge veri nesnesi zaten varsa açın, null olmayan bir `punkDocDataExisting` değeri geçirilir `IVsEditorFactory::CreateEditorInstance`. Düzenleyici fabrikası uygulamanız için uygun arabirimlerde sorgulayarak var olan bir belge veri nesnesi uyumlu olup olmadığını belirlemeniz gerekir. Daha fazla bilgi için [birden çok belge görünümünü destekleme](../extensibility/supporting-multiple-document-views.md).  
  
-   Basitleştirilmiş ekleme yaklaşımını kullanırsanız, uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> arabirimi.  
  
-   Yerinde etkinleştirme kullanmaya karar verirseniz, aşağıdaki arabirim uygular:  
  
     <xref:Microsoft.VisualStudio.OLE.Interop.IOleObject>  
  
     <xref:Microsoft.VisualStudio.OLE.Interop.IOleInPlaceActiveObject>  
  
     <xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponent>  
  
    > [!NOTE]
    >  `IOleInPlaceComponent` Arabirimi OLE 2 menü birleştirme önlemek için kullanılır.  
  
     `IOleCommandTarget` Uygulama işleme komutları gibi **Kes**, **kopyalama**, ve **Yapıştır**. Uygularken `IOleCommandTarget`, düzenleyiciniz kendi gerektirip gerektirmediğini karar *.vsct* kendi komutu menüsü yapısı tanımlamak için dosya veya standart komutlar tarafından tanımlanan uygulayabilirsiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Genellikle, Düzenleyicileri kullanın ve IDE'nin menüleri genişletin ve kendi araç çubukları tanımlayın. Ancak, genellikle IDE'nin standart komut kümesi kullanmanın yanı sıra kendi özel komutları tanımlamak bir düzenleyici için gereklidir. Düzenleyici kullandığı standart komutlar bildirmeli ve ardından yeni komutlar, bağlam menüleri, üst düzey menüler ve araç çubuklarını tanımlamak bir *.vsct* dosya. Düzenleyicisi bir yerinde etkinleştirme oluşturursanız, uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponent> ve araç çubukları ve menüler Düzenleyicisi'nde tanımladığınız bir *.vsct* OLE 2 menü birleştirme kullanmak yerine dosya.  
  
-   Menü komutu kullanıcı Arabiriminde doldurmak önlemek için yeni komutlar inventing önce mevcut komutları IDE'de kullanmalısınız. Paylaşılan komutları tanımlanmış *SharedCmdDef.vsct* ve *ShellCmdDef.vsct*. Bu dosyalar VisualStudioIntegration\Common\Inc alt varsayılan olarak yüklenir, [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] yükleme.  
  
-   `ISelectionContainer` tek ve çoklu seçim ifade edebilirsiniz. Her bir seçili nesne olarak uygulanan bir `IDispatch` nesne.  
  
-   IDE uygulayan `IOleUndoManager` erişilebilir bir hizmet olarak bir <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance%2A> veya aracılığıyla oluşturulan bir nesne olarak <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance%2A>. Düzenleyici uygular `IOleUndoUnit` her arabirimi `Undo` eylem.  
  
-   İki yerde vardır özel bir düzenleyici Otomasyon nesneleri getirebilir:  
  
    -   `Document.Object`  
  
    -   `Window.Object`  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Otomasyon modeline katkıda bulunma](../extensibility/internals/contributing-to-the-automation-model.md)   
 [Nasıl yapılır: bağlam sağlamak için düzenleyicileri açma](../extensibility/how-to-provide-context-for-editors.md)