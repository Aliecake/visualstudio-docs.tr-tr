---
title: Receive etkinlik Tasarımcısı | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.ServiceModel.Activities.Receive.UI
ms.assetid: f58d3c70-944d-4bb4-90a7-e68c103caddc
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: c2ccae6d53a44704aeb770fb60e5e2a0c9aecd3f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49287241"
---
# <a name="receive-activity-designer"></a>Receive Etkinlik Tasarımcısı
**Alma** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.ServiceModel.Activities.Receive> etkinlik. A <xref:System.ServiceModel.Activities.Receive> etkinlik dışı bir yerleşik bir tür gibi olabilir bir ileti aldığı etkinlik <xref:System.ServiceModel.Channels.Message>, <xref:System.IO.Stream> veya <xref:System.Xml.Linq.XElement>, veya bir uygulama tarafından tanımlanan veri anlaşması, ileti anlaşması veya seri hale getirilebilir XML sınıfı.  
  
## <a name="the-receive-activity"></a>Etkinlik alma  
 <xref:System.ServiceModel.Activities.Receive> Etkinlik, tek bir öğeyi alabilir veya birden çok öğe türüne bağlı olarak kullanılan içerik alırsınız. A <xref:System.ServiceModel.Activities.SendReply> etkinlik bağlanabilir bir <xref:System.ServiceModel.Activities.Receive> istek/yanıt ileti değişim deseni hizmetinde bir parçası olarak bir ileti aldığı etkinlik.  
  
### <a name="using-the-receive-activity-designer"></a>Kullanarak Receive etkinlik Tasarımcısı  
 **Alma** etkinlik Tasarımcısı bulunabilir **Mesajlaşma** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Alma** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir. Bu, oluşturur bir <xref:System.ServiceModel.Activities.Receive> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> alma. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **alma** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
 Oluşturmak için bir <xref:System.ServiceModel.Activities.SendReply> etkinlik ve seçili bağlama <xref:System.ServiceModel.Activities.Receive> etkinliği sağ tıklatın **alma** etkinlik Tasarımcısı tıklayın **SendReply oluşturma** bağlam menüsü öğesini ve **SendReplyToReceive** Tasarımcısı aşağıda görünür **alma** Tasarımcısı. <xref:System.ServiceModel.Activities.SendReply> Yanıt iletisi, istek/yanıt ileti değişim deseni hizmetinde bir parçası olarak gönderen bir etkinlik bir etkinliktir. İle yapılandırılabilir **SendReplyToReceive** Tasarımcısı.  
  
 Alternatif olarak, **ReceiveAndSendReply** şablonu Tasarımcısı'nda **Mesajlaşma** kategorisi **araç kutusu** önceden yapılandırılmış çiftioluşturmakiçinkullanılan<xref:System.ServiceModel.Activities.Receive>ve <xref:System.ServiceModel.Activities.SendReply> etkinlik. [!INCLUDE[crabout](../includes/crabout-md.md)] kullanımını **ReceiveAndSendReply** ve **SendReplyToReceive** şablonu görmek [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md) konu.  
  
### <a name="the-receive-activity-properties"></a>Etkinlik özelliklerini alma  
 Aşağıdaki tabloda <xref:System.ServiceModel.Activities.Receive> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikleri Özellikler kılavuzu veya Cihazınızda düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzeyi. Yalnızca gerekli özellik <xref:System.ServiceModel.Activities.Receive.OperationName%2A> özelliği.  
  
|Özellik adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı belirtir <xref:System.ServiceModel.Activities.Receive> etkinlik. Alma varsayılan değerdir.<br /><br /> Ancak kolay için varsayılan olmayan bir değeri kullanımını <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil gibi bir değer kullanmak için en iyi bir uygulamadır.|  
|<xref:System.ServiceModel.Activities.Receive.OperationName%2A>|Doğru|Bu tarafından uygulanan hizmet işlemi adını belirtir <xref:System.ServiceModel.Activities.Receive> etkinlik. Bu özellik için varsayılan değer oluşturmak için kullanılan **eylem** özelliği varsa **eylem** özelliği açıkça ayarlanmadı.|  
|<xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A>|False|Hizmet sözleşmesi adını belirtir. Bu özellik, bireysel hizmet sözleşmelerini grubu hizmet işlemi için kullanılır. Tüm <xref:System.ServiceModel.Activities.Receive> aynı etkinlikleri <xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A> aynı hizmet sözleşmesi (WSDL bağlantı noktası türü) gruplandırılır. Üst düzey (kök) etkinliğin tam CLR adı varsayılan değerdir.|  
|<xref:System.ServiceModel.Activities.Receive.Content%2A>|False|İleti veya parametre içeriği almak için belirtir. Ya da olabilir bir <xref:System.ServiceModel.Activities.ReceiveMessageContent> etkinlik veya <xref:System.ServiceModel.Activities.ReceiveParametersContent> etkinlik. Yanındaki üç nokta düğmesine tıklayarak bu özellik düzenleme **içerik** özellik kılavuzu veya tıklayarak alanındaki **tanımla...** yanında düğmesini **içerik** üzerinde etiket **alma** etkinlik Tasarımcı yüzeyine bırakın. Her ikisini de görüntüle **içerik tanımı** iletişim. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu kutuyu kullanmak üzere nasıl [içerik tanımı iletişim kutusunun](../workflow-designer/content-definition-dialog-box.md) konu.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A>|False|Arasında bağıntılar belirtir <xref:System.ServiceModel.Activities.Receive> hizmet işlemleri ile bir iş akışı etkinlikleri bir <xref:System.ServiceModel.MessageQuerySet> nesne. Yanındaki üç nokta düğmesini tıklayın <xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A> özelliği açmak için özellikler kılavuzundaki **definice vlastnosti Correlateson** iletişim kutusu. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu iletişim kutusunu kullanımını görmek [içerik tanımı iletişim kutusunun](../workflow-designer/content-definition-dialog-box.md) konu.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelatesWith%2A>|False|Belirtir <xref:System.ServiceModel.Activities.CorrelationHandle> uygun iş akışı örneği için ileti yönlendirmek için kullanılır.<br /><br /> Yanındaki üç nokta düğmesini tıklayın <xref:System.ServiceModel.Activities.Receive.CorrelatesWith%2A> özelliği açmak için özellikler kılavuzundaki **ifade Düzenleyicisi** iletişim kutusu. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu iletişim kutusunu kullanımını görmek [nasıl yapılır: ifade düzenleyicisini kullanma](../workflow-designer/how-to-use-the-expression-editor.md) konu.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelationInitializers%2A>|False|Koleksiyonunu belirtir <xref:System.ServiceModel.Activities.CorrelationInitializer> birden çok başlatmak nesneleri <xref:System.ServiceModel.Activities.CorrelationHandle> bu yapılandırma nesneleri <xref:System.ServiceModel.Activities.Receive> etkinlik iş akışı içinde. Yanındaki üç nokta düğmesini tıklayın <xref:System.ServiceModel.Activities.Receive.CorrelationInitializers%2A> özelliği açmak için özellikler kılavuzundaki **bağıntı başlatıcılar Ekle** iletişim kutusu. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu kutuyu bkz [Correlationınitializer iletişim kutusunu](../workflow-designer/add-correlationinitializers-dialog-box.md) konu.|  
|<xref:System.ServiceModel.Activities.Receive.CanCreateInstance%2A>|False|Yeni bir iş akışı örneği ileti var olan bir iş akışı örneğini bağıntılı olmayan, iletiyi işlemek için oluşturulup oluşturulmayacağını belirleyen bir değer belirtir. Değer ayarlanmışsa **true**, iletiyi varolan bir iş akışı örneğiyle ilişkili değil, iletiyi işlemek için yeni bir iş akışı örneği oluşturulur.|  
|<xref:System.ServiceModel.Activities.Receive.KnownTypes%2A>|False|Bu tarafından uygulanan hizmet işlemi için bilinen türleri koleksiyonu belirtir <xref:System.ServiceModel.Activities.Receive> etkinlik. Bu özellik ile birlikte kullanılması gereken <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A> özelliğini <xref:System.Runtime.Serialization.DataContractSerializer>. Varsa göz ardı edilir <xref:System.Xml.Serialization.XmlSerializer> kullanılır.<br /><br /> Yanındaki üç nokta düğmesini **KnownTypes** özellik kılavuzunda görüntülenecek alan **Editor Typu Kolekce** ilgili türleri ile ekleyebileceğiniz iletişim kutusu. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu kutuyu bkz [türü koleksiyon Düzenleyicisi iletişim kutusu](../workflow-designer/type-collection-editor-dialog-box.md) konu.|  
|<xref:System.ServiceModel.Activities.Receive.ProtectionLevel%2A>|False|Belirtir <xref:System.Net.Security.ProtectionLevel> ileti.<br /><br /> 1. <xref:System.Net.Security.ProtectionLevel> yalnızca kimlik doğrulamasını anlamına gelir.<br />2. <xref:System.Net.Security.ProtectionLevel> oturum iletilen veri bütünlüğünü sağlamaya yardımcı olmak için veri anlamına gelir.<br />3. <xref:System.Net.Security.ProtectionLevel> anlamına gelir, şifreleme ve veri gizliliği ve aktarılan veri bütünlüğünü sağlamaya yardımcı olmak için oturum açın.|  
|<xref:System.ServiceModel.Activities.Receive.SerializerOption%2A>|False|Seri hale getirici tarafından uygulanan hizmet işlemi için kullanılacak türünü belirten <xref:System.ServiceModel.Activities.Receive> etkinlik. Varsayılan değer <xref:System.Runtime.Serialization.DataContractSerializer>, serileştirir ve bir XML akışı veya sağlanan veri sözleşme kullanan bir belge bir türün bir örneği seri durumdan çıkarır. <xref:System.Xml.Serialization.XmlSerializer> Daha fazla denetim gerekliyse, XML de kullanılabilir.|  
|<xref:System.ServiceModel.Activities.Receive.Action%2A>|False|İletinin eylem üstbilgisini belirtir. Değeri açıkça ayarlanmazsa, varsayılan: https://tempuri.org/{service sözleşme ad alanı} / {hizmet sözleşmesi adı} / {işlem adı}.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Initializecorrelation](../workflow-designer/initializecorrelation-activity-designer.md)   
 [CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)   
 [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md)   
 [Gönder](../workflow-designer/send-activity-designer.md)   
 [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)   
 [TransactedReceiveScope](../workflow-designer/transactedreceivescope-activity-designer.md)