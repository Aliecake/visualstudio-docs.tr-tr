---
title: Yığın ayırma işlevleri sürümleri hata ayıklama | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.crt
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- _CRTDBG_MAP_ALLOC macro
- debugging [CRT], heap allocation functions
- debugging memory leaks, CRT debug library functions
- malloc function
- memory leaks, CRT debug library functions
- heap allocation, debug
- _malloc_dbg function
ms.assetid: 91748bdc-f4cd-4d8b-ab98-0493dab7ed0d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e426da9491c13e0d6f9377814673ca41512e5e09
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31470949"
---
# <a name="debug-versions-of-heap-allocation-functions"></a>Öbek Atama İşlevleri Hata Ayıklama Sürümleri
C çalışma zamanı kitaplığı yığın ayırma işlevleri özel hata ayıklama sürümlerini içerir. Bu işlevler yayım olarak aynı ada sahip kendisine eklenmiş _dbg sürümleriyle. Bu konuda CRT işlevi sürümünü ve _dbg sürümü arasındaki farklılıklar açıklanmıştır kullanarak `malloc` ve `_malloc_dbg` örnekler.  
  
 Zaman [_DEBUG](/cpp/c-runtime-library/debug) olan tanımlanan CRT tüm eşlemeleri [malloc](/cpp/c-runtime-library/reference/malloc) çağrılar [_malloc_dbg](/cpp/c-runtime-library/reference/malloc-dbg). Bu nedenle, kodu kullanarak yeniden gerekmez `_malloc_dbg` yerine `malloc` hata ayıklama sırasında avantajları almak için.  
  
 Çağrı isteyebilirsiniz `_malloc_dbg` açıkça, ancak. Çağırma `_malloc_dbg` açıkça bazı avantajları ekledi:  
  
-   İzleme `_CLIENT_BLOCK` ayırmaları yazın.  
  
-   Ayırma isteği gerçekleştiği kaynak dosyası ve satır numarası depolama.  
  
 Dönüştürmek istemiyorsanız, `malloc` çağrılar `_malloc_dbg`, tanımlayarak kaynak dosya bilgileri edinebilirsiniz [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc), tüm çağrıları doğrudan önişlemci harita neden `malloc` için`_malloc_dbg` çevresinde bir sarmalayıcı güvenmek yerine `malloc`.  
  
 İstemci blokları ayırma ayrı türlerini izlemek için çağırmalısınız `_malloc_dbg` doğrudan ve `blockType` parametresi `_CLIENT_BLOCK`.  
  
 _DEBUG tanımlı değil, çağrılar `malloc` değil etkilenir, çağrılar `_malloc_dbg` için çözümlendiği `malloc`, tanımını [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc) dikkate alınmaz ve kaynak için ilgili dosya bilgileri ayırma isteği sağlanmadı. Çünkü `malloc` bir blok türü parametresine sahip değilse, için istekleri `_CLIENT_BLOCK` türleri standart ayırmaları kabul edilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CRT hata ayıklama teknikleri](../debugger/crt-debugging-techniques.md)