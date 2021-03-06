---
title: Menü komutunun metnini değiştirme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- menus, changing text
- text, menus
- commands, changing text
ms.assetid: 5cb676a0-c6e2-47e5-bd2b-133dc8842e46
caps.latest.revision: 26
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 00437c10fa93bb72d7579328ad22c347cdf96049
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49237451"
---
# <a name="changing-the-text-of-a-menu-command"></a>Bir Menü Komutunun Metnini Değiştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki adımları kullanarak bir menü komutu metin etiketini değiştirme Göster <xref:System.ComponentModel.Design.IMenuCommandService> hizmeti.  
  
## <a name="changing-a-menu-command-label-with-the-imenucommandservice"></a>Bir menü komutu etiket IMenuCommandService ile değiştirme  
  
1.  Adlı bir VSIX projesi oluşturun `MenuText` bir menü komutuyla adlı **ChangeMenuText**. Daha fazla bilgi için [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md).  
  
2.  .vstc dosyasına ekleyin `TextChanges` aşağıdaki örnekte gösterildiği gibi bir menü komutu için bayrak.  
  
    ```xml  
    <Button guid="guidChangeMenuTextPackageCmdSet" id="ChangeMenuTextId" priority="0x0100" type="Button">  
        <Parent guid="guidChangeMenuTextPackageCmdSet" id="MyMenuGroup" />  
        <Icon guid="guidImages" id="bmpPic1" />  
        <CommandFlag>TextChanges</CommandFlag>  
        <Strings>  
            <ButtonText>Invoke ChangeMenuText</ButtonText>  
        </Strings>  
    </Button>  
    ```  
  
3.  ChangeMenuText.cs dosyasında menü komutunu görüntülenmeden önce çağrılacak bir olay işleyicisi oluşturun.  
  
    ```csharp  
    private void OnBeforeQueryStatus(object sender, EventArgs e)  
    {  
        var myCommand = sender as OleMenuCommand;  
        if (null != myCommand)  
        {  
            myCommand.Text = "New Text";  
                    }  
    }  
    ```  
  
     Değiştirerek bu yöntemdeki menü komutunu durumunu güncelleştirebilir <xref:System.ComponentModel.Design.MenuCommand.Visible%2A>, <xref:System.ComponentModel.Design.MenuCommand.Checked%2A>, ve <xref:System.ComponentModel.Design.MenuCommand.Enabled%2A> özellikleri <xref:Microsoft.VisualStudio.Shell.OleMenuCommand> nesne.  
  
4.  ChangeMenuText oluşturucusunun içinde özgün komut başlatma ve yerleştirme kodu oluşturan kod ile değiştirin. bir <xref:Microsoft.VisualStudio.Shell.OleMenuCommand> (yerine `MenuCommand`) menü komutu temsil eder, ekler <xref:Microsoft.VisualStudio.Shell.OleMenuCommand.BeforeQueryStatus> olay işleyicisi ve menüsü sağlar menü komutu hizmeti komutu.  
  
     İşte ne gibi görünmelidir:  
  
    ```csharp  
    private ChangeMenuText(Package package)  
    {  
        if (package == null)  
        {  
            throw new ArgumentNullException(nameof(package));  
        }  
  
        this.package = package;  
  
        OleMenuCommandService commandService = this.ServiceProvider.GetService(typeof(IMenuCommandService)) as OleMenuCommandService;  
        if (commandService != null)  
        {  
            CommandID menuCommandID = new CommandID(MenuGroup, CommandId);  
            EventHandler eventHandler = this.ShowMessageBox;  
            OleMenuCommand menuItem = new OleMenuCommand(ShowMessageBox, menuCommandID);  
            menuItem.BeforeQueryStatus +=  
                new EventHandler(OnBeforeQueryStatus);  
            commandService.AddCommand(menuItem);  
        }  
    }  
    ```  
  
5.  Projeyi oluşturmak ve hata ayıklamaya başlayın. Visual Studio'nun deneysel örneğinde görünür.  
  
6.  Üzerinde **Araçları** menü adlı bir komut görmeniz **çağırma ChangeMenuText**.  
  
7.  Komutu tıklatın. İleti kutusu Duyurusu MenuItemCallback çağrıldıktan görmeniz gerekir. İleti kutusu kapatırken, Araçlar menüsünden komut adını artık olduğunu görmeniz gerekir **yeni metin**.

