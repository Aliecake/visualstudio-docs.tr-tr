---
title: 'Hata: Kerberos kimlik doğrulaması başarısız oldu. | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.callback_kerberos_auth_failed
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 085b120974ee23d0d7e3712cdbb0a8f7f7021e83
ms.sourcegitcommit: 0bf2aff6abe485e3fe940f5344a62a885ad7f44e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37056863"
---
# <a name="error-kerberos-authentication-failed"></a>Hata: Kerberos Kimlik Doğrulaması Başarısız
Uzaktan hata ayıklama yapın denediğinizde aşağıdaki hata iletisini alabilirsiniz:  
  
```cmd
Error: The Visual Studio Remote Debugger on the target computer cannot connect back to this computer. Kerberos authentication failed.  
```  
  
 Visual Studio uzaktan hata ayıklama İzleyicisi yerel sistem veya ağ hizmeti hesabı altında çalışıyorsa, bu hata oluşur. Bu hesaplardan birini altında uzaktan hata ayıklayıcı geri Visual Studio hata ayıklayıcısı ana bilgisayara iletişim kurmak için Kerberos kimlik doğrulaması bağlantı oluşturmanız gerekir.  
  
 Kerberos kimlik doğrulaması Bu koşullar altında kullanılabilir değil:  
  
-   Hedef bilgisayar ya da hata ayıklayıcı ana bilgisayar bir etki alanı yerine bir çalışma grubunda olan  
  
     \- veya -  
  
-   Kerberos etki alanı denetleyicisinde devre dışı bırakıldı.  
  
 Kerberos kimlik doğrulaması kullanılabilir durumda değilse, Visual Studio uzaktan hata ayıklama İzleyicisi çalıştırmak için kullanılan hesabı değiştirin. Yordamı için bkz: [hata: hedef bilgisayardaki Visual Studio uzaktan hata ayıklayıcı hizmeti geriye bu bilgisayara bağlanamıyor](../debugger/error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md).  
  
 Her iki bilgisayar aynı etki alanına bağlı ve bu iletiyi almaya devam, hedef bilgisayarda DNS hata ayıklayıcı ana bilgisayar adı doğru biçimde çözümleyemiyor doğrulayın. Aşağıdaki yordama bakın.  
  
### <a name="to-verify-that-dns-on-the-target-computer-is-correctly-resolving-the-debugger-host-computer-name"></a>Hedef bilgisayarda DNS hata ayıklayıcı ana bilgisayar adı doğru biçimde çözümleyemiyor doğrulamak için  
  
1.  Hedef bilgisayarda açın **Başlat** menüsündeki **Donatılar** ve ardından **komut istemi**.  
  
2.  İçinde **komut istemi** penceresinde, türü:  
  
    ```cmd
    ping <debugger_host_computer_name>  
    ```  
  
3.  İlk satırı `ping` tam bilgisayar adı ve IP adresi belirtilen bilgisayar için DNS tarafından döndürülen yanıt gösterir.  
  
4.  Hata ayıklayıcı ana bilgisayarda açık bir **komut istemi** penceresini açın ve Çalıştır `ipconfig`.  
  
5.  IP adresi değerlerini karşılaştırın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan hata ayıklama](../debugger/remote-debugging.md)
