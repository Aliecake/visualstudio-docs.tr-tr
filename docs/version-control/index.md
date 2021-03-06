---
layout: LandingPage
title: Visual Studio'da sürüm denetimi | VSTS ve TFS
description: Sürüm denetimi Viual Studio'da ile Başlama Kılavuzu
keywords: VSTS, TFS sürüm denetimi
author: steved0x
ms.manager: douge
ms.author: sdanie
ms.date: 12/15/2017
ms.topic: landing-page
ms.prod: .net-core
ms.assetid: 2c119a5f-0272-48c0-8d6c-806196944aea
ms.workload:
- multiple
ms.openlocfilehash: e37645f8960aae54907dffeb0bcb88848d9cd63f
ms.sourcegitcommit: 28909340cd0a0d7cb5e1fd29cbd37e726d832631
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44320585"
---
# <a name="version-control-in-visual-studio"></a>Visual Studio'da sürüm denetimi

Sürüm denetimi sistemleri, zaman içinde kod değişiklikleri izlemenize yardımcı olur. Yaptığınız gibi sürüm denetimi sistemi dosyalarınızın anlık görüntüsünü alır. Sürüm denetimi sistemi ihtiyacınız varsa, bunu daha sonra başvurmanız bu anlık görüntüyü kalıcı olarak kaydeder. Visual Studio sağlar [Git](/azure/devops/repos/git/index?view=vsts) ve [Team Foundation sürüm denetimi (TFVC)](/azure/devops/repos/tfvc/index?view=vsts). İki sistem arasında karar vermek için bkz: [projeniz için doğru sürüm denetimini seçme](/azure/devops/repos/tfvc/comparison-git-tfvc?toc=/visualstudio/version-control/toc.json&bc=/azure/devops/repos/git/breadcrumb/vc/toc.json).

## <a name="git"></a>Git
Git, günümüzde en yaygın şekilde kullanılan sürüm denetimi sistemi olan ve standart sürüm denetimi için hızla büyüyor. Yerel kod kopyanızın eksiksiz sürüm denetimi deposu olduğu anlamına gelen bir dağıtılmış sürüm denetim sistemi Git var. Bu tam işlevli yerel depolar, çevrimdışı veya uzaktan çalışmayı kolaydır olun. Çalışmanızı yerel olarak işleyin ve ardından depo kopyanızı sunucudaki kopyayla eşitleyin. Bu paradigma, burada istemciler kodu bir sunucuyla yeni kod sürümleri oluşturmadan önce eşitlemelidir merkezi sürüm denetiminden farklıdır.

<ul class="panelContent cardsFTitle">
    <li>
        <a href="https://docs.microsoft.com/azure/devops/git/what-is-git">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/common/i_git-mark.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>Git kullanmayı öğrenin</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
    <li>
        <a href="/azure/devops/repos/git/share-your-code-in-git-vs-2017?toc=/visualstudio/version-control/toc.json&bc=/azure/devops/repos/git/breadcrumb/vc/toc.json">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/common/i_git-mark.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>Git ile Visual Studio ile çalışmaya başlama</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
    <li>
        <a href="/azure/devops/repos/git/clone?toc=/visualstudio/version-control/toc.json&bc=/azure/devops/repos/git/breadcrumb/vc/toc.json">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/common/i_git-mark.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>Mevcut bir Git deposunu kopyalayın</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
</ul>

## <a name="tfvc"></a>TFVC

Team Foundation Sürüm Denetimi (TFVC) merkezi sürüm denetim sistemidir. Genellikle, ekip üyeleri kendi geliştirme makinelerinde her dosyanın yalnızca bir sürümüne sahiptir. Geçmiş verisi yalnızca sunucuda tutulur. Dallar, yol tabanlıdır ve sunucuda oluşturulur.

<ul class="panelContent cardsFTitle">
    <li>
        <a href="/azure/devops/repos/tfvc/overview">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/logos/logo_visual-studio.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>TFVC öğrenin</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
    <li>
        <a href="/azure/devops/repos/tfvc/share-your-code-in-tfvc-vs?toc=/visualstudio/version-control/toc.json&bc=/azure/devops/repos/git/breadcrumb/vc/toc.json">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/logos/logo_visual-studio.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>Visual Studio'da TFVC ile çalışmaya başlama</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
   <li>
        <a href="/azure/devops/repos/tfvc/get-code-reviewed-vs?toc=/visualstudio/version-control/toc.json&bc=/azure/devops/repos/git/breadcrumb/vc/toc.json">
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardImageOuter">
                        <div class="cardImage">
                            <img width="48" height="48" alt="" src="https://docs.microsoft.com/media/logos/logo_visual-studio.svg" />
                        </div>
                    </div>
                    <div class="cardText">
                        <h3>Kodunuzu gözden geçirin</h3>
                    </div>
                </div>
            </div>
        </div>
        </a>
    </li>
</ul>


## <a name="resources"></a>Kaynaklar

- [Pro Git kitabı](https://git-scm.com/book/en/v2)
- [Git için geçişiniz planlama](https://docs.microsoft.com/azure/devops/git/centralized-to-git)
- [TFVC'den Git'e geçme](https://docs.microsoft.com/azure/devops/git/migrate-from-tfvc-to-git)