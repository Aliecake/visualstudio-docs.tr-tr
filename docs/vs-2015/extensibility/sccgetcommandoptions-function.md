---
title: SccGetCommandOptions işlevi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccGetCommandOptions
helpviewer_keywords:
- SccGetCommandOptions function
ms.assetid: bbe4aa4e-b4b0-403e-b7a0-5dd6eb24e5a9
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1b3efc963c71b6dfb18a014a46ae2f3442ef2524
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49271589"
---
# <a name="sccgetcommandoptions-function"></a>SccGetCommandOptions İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu işlev, belirli bir komut için Gelişmiş Seçenekleri kullanıcıya sorar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
SCCRTN SccGetCommandOptions(  
   LPVOID pvContext,  
   HWND hWnd,  
   enum SCCCOMMAND iCommand,  
   LPCMDOPTS* ppvOptions  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pvContext  
 [in] Kaynak Denetimi Eklentisi bağlam yapısı.  
  
 hWnd  
 [in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.  
  
 ICommand'ı  
 [in] Gelişmiş Seçenekler istenir komut (bkz [komut kodu](../extensibility/command-code-enumerator.md) olası değerler için).  
  
 ppvOptions  
 [in] Seçenek yapısı (Ayrıca `NULL`).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|Başarılı.|  
|SCC_I_ADV_SUPPORT|Kaynak denetimi eklentisi komutu için Gelişmiş seçeneklerini destekler.|  
|SCC_I_OPERATIONCANCELED|Kaynak denetimi eklentinin kullanıcı iptal **seçenekleri** iletişim kutusu.|  
|SCC_E_OPTNOTSUPPORTED|Kaynak Denetimi Eklentisi bu işlemi desteklemiyor.|  
|SCC_E_ISCHECKEDOUT|Şu anda kullanıma alınmış bir dosya üzerinde bu işlemi gerçekleştiremezsiniz.|  
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|  
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|  
  
## <a name="remarks"></a>Açıklamalar  
 IDE ile ilk kez bu işlevi çağıran `ppvOptions` = `NULL` kaynak denetimi eklentisi belirtilen komut için Gelişmiş Seçenekleri özelliğini destekleyip desteklemediğini belirlemek için. Eklentinin özelliği için bu komutu da destekler, kullanıcı Gelişmiş Seçenekleri istediğinde IDE bu işlevini yeniden çağırır (genellikle olarak uygulanan bir **Gelişmiş** iletişim kutusunda bir düğme) ve içinNULLolmayanbirişaretçisağlar`ppvOptions` işaret eden bir `NULL` işaretçi. Eklenti özel bir yapı kullanıcı tarafından belirtilen tüm gelişmiş seçenekleri saklar ve o yapısına bir işaretçi döndürür `ppvOptions`. Bu yapı yapılan sonraki çağrılar dahil olmak üzere, bilmeniz gereken diğer tüm kaynak denetimi eklentisi API işlevleri geçirilerek `SccGetCommandOptions` işlevi.  
  
 Örneği bu durumda açıklamak yardımcı olabilir.  
  
 Kullanıcının **alma** komut ve IDE görüntüler bir **alma** iletişim kutusu. IDE çağrıları `SccGetCommandOptions` işleviyle `iCommand` kümesine `SCC_COMMAND_GET` ve `ppvOptions` kümesine `NULL`. Bu kaynak denetimi eklentisi soru olarak yorumlanır, "Bu komut için Gelişmiş Seçenekleri gerekiyor?" Eklenti döndürürse `SCC_I_ADV_SUPPORT`, IDE görüntüler bir **Gelişmiş** düğmesine kendi **alma** iletişim kutusu.  
  
 Kullanıcı ilk kez **Gelişmiş** düğmesi, IDE yeniden çağırır `SccGetCommandOptions` bu sefer olmayan bir işlev`NULL``ppvOptions` işaret eden bir `NULL` işaretçi. Eklenti görüntüler kendi **alma seçenekleri** iletişim kutusu, kullanıcıdan bilgi edinmek için bu bilgiyi kendi yapısında koyar ve o yapısına bir işaretçi döndürür `ppvOptions`.  
  
 Kullanıcı tıklarsa **Gelişmiş** aynı iletişim kutusunda, IDE yeniden çağırır `SccGetCommandOptions` değiştirmeden yeniden işlevi `ppvOptions`, böylece yapısı geri eklenti geçirilir. Bu eklenti, iletişim kutusu, kullanıcının daha önce ayarlamış olduğunuz değerlerle yeniden başlatmak için sağlar. Eklenti yapısı yerinde, sonuç döndürülmeden önce değiştirir.  
  
 Son olarak, kullanıcı tıkladığında **Tamam** IDE'nin içinde **alma** iletişim kutusu, IDE çağrıları [SccGet](../extensibility/sccget-function.md), iade yapısı geçirme `ppvOptions` içeren Gelişmiş Seçenekleri.  
  
> [!NOTE]
>  Komut `SCC_COMMAND_OPTIONS` IDE görüntüler kullanıldığında bir **seçenekleri** kullanıcı iletişim kutusunu tümleştirmesinin nasıl çalıştığına denetleyen tercihlerini ayarlama. Kaynak Denetimi Eklentisi, kendi Tercihleri iletişim kutusu sağlamak isterse, buradan görüntüleyebilirsiniz bir **Gelişmiş** IDE'nin Tercihleri iletişim kutusu düğmesi. Eklenti alma ve bu bilgileri kalıcı hale getirmeniz için ayarlanmasından sorumludur; IDE kullanın veya üzerinde değişiklik desteklemez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [Komut Kodu](../extensibility/command-code-enumerator.md)

