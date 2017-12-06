---
title: "Bellek sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Process properties for Windows NT
ms.assetid: a70785f2-5997-40ec-a90f-80a52449768b
caps.latest.revision: "4"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7629fd477d0eb5a2a142e48aa90bb97e4c10a152
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="memory-tab-process-properties-dialog-box"></a>Bellek Sekmesi, İşlem Özellikleri İletişim Kutusu
Kullanım **bellek** bir işlem bellek nasıl kullandığını göstermek için sekmesi. Görüntülenecek [işlem özellikleri iletişim kutusu](../debugger/process-properties-dialog-box.md), odağı taşımak bir [işlemler görünümü](../debugger/processes-view.md) penceresi. Ağaçta herhangi bir işlem düğümü seçin ve ardından **özellikleri** gelen **Görünüm** menüsü.  
  
 Aşağıdaki ayarlar kullanılabilir **bellek** sekmesi:  
  
|Giriş|Açıklama|  
|-----------|-----------------|  
|**Sanal bayt sayısı**|İşlemin kullandığı sanal adres alanının geçerli boyutunu (bayt cinsinden). Sanal adres alanının kullanılması ilgili disk veya ana bellek sayfalarının kullanımını göstermez. Ancak, sanal adres alanı sınırlıdır ve kullanarak kitaplıkları Yükleme özelliğini işleminin çok sınırlayabilir.|  
|**En yüksek sanal bayt sayısı**|İşlemin sanal adres alanının bayt sayısını herhangi bir zamanda kullandı.|  
|**Çalışma kümesi**|İşlemdeki iş parçacıkları tarafından son Kullanıla bellek sayfaları kümesidir. Bilgisayardaki boş bellek eşiğin üzerinde ise, kullanımda olmayan bile, sayfalar çalışma kümesi içinde bir işlemin kalır. Boş bellek eşiğin altına düştüğünde, sayfalar çalışma kümesinden atılır. Gerekli olurlarsa ana bellekten ayrılmadan önce çalışma kümesine geri sonradan olmaları.|  
|**En yüksek çalışma kümesi**|Bu işlem, herhangi bir noktada çalışma kümesindeki sayfaları maksimum sayısı.|  
|**Disk belleği havuzu bayt sayısı**|İşlemin ayırdığı disk belleğine alınan havuz geçerli miktarı. Disk belleği havuzu kaldırmasını görevlerini gerçekleştirmek gibi işletim sistemi bileşenleri alanı burada elde bir sistem bellek alanıdır. Disk belleği havuzu sayfaları sistem tarafından sürekli süreyle değil erişildiğinde disk belleği dosyasının faaliyetsizlikten.|  
|**Disk belleği olmayan havuz bayt sayısı**|İşlem tarafından ayrılan disk belleği olmayan havuz bayt sayısı. Disk belleği olmayan havuz burada kaldırmasını görevlerini gerçekleştirmek gibi alanı işletim sistemi bileşenleri tarafından alındığını bir sistem bellek alanıdır. Disk belleği olmayan havuz sayfaları için disk belleği dosyası faaliyetsizlikten olamaz; ayrıldıkları sürece ana bellekte kalırlar.|  
|**Özel bayt sayısı**|Geçerli bu işlemin ayırdığı bayt sayısı, diğer işlemlerle paylaşılamaz.|  
|**Boş bayt sayısı**|Bu işlemin kullanılmayan toplam sanal adres alanı.|  
|**Ayrılan bayt**|Bu işlem tarafından gelecekte kullanım için ayrılan sanal bellek miktarı.|  
|**Ücretsiz görüntü bayt**|Kullanımda olmadığından veya bu işlemi içinde görüntüleri tarafından ayrılan sanal adres alanı miktarı.|  
|**Ayrılmış görüntü bayt**|Bu işlemi içinde çalıştırılan yansımaların tarafından ayrılan sanal bellek toplamı.|