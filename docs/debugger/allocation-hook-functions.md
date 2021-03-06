---
title: Atama kanca işlevleri | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- memory allocation, logging allocation information
- insufficient memory
- debugging [C++], hook functions
- _CrtSetAllocHook function
- allocation hooks
- hooks, allocation
ms.assetid: 6bfbdb65-8cb1-4c21-8c45-7194a2b77c1e
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6c8a051641811da3658ffe556982c67649704069
ms.sourcegitcommit: 80f9daba96ff76ad7e228eb8716df3abfd115bc3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37433362"
---
# <a name="allocation-hook-functions"></a>Atama Kanca İşlevleri
Kullanarak yüklü bir ayırma kanca işlevini [_CrtSetAllocHook](/cpp/c-runtime-library/reference/crtsetallochook), bellek tahsis, bırakılan veya serbest her zaman çağrılır. Bu tür bir kanca birçok farklı amaçlar için kullanabilirsiniz. Daha sonra çözümlemek için ayırma bilgileri günlüğe kaydetmek veya nasıl bir uygulama yetersiz bellek durumları gibi ayırma desenlerini incelenmesi işleme test kullanın.  
  
> [!NOTE]
>  Kısıtlama C çalışma zamanı kitaplık işlevleri açıklandığı bir ayırma kanca işlevini kullanma hakkında bilmeniz [ayırma kancaları ve C çalışma zamanı bellek ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md).  
  
 Bir ayırma kanca işlevini, aşağıdaki örnekte olduğu gibi bir prototipe sahip olmalıdır:  
  
```cpp
int YourAllocHook(int nAllocType, void *pvData,  
        size_t nSize, int nBlockUse, long lRequest,  
        const unsigned char * szFileName, int nLine )  
```  
  
 Geçirdiğiniz işaretçiyi [_CrtSetAllocHook](/cpp/c-runtime-library/reference/crtsetallochook) türünde **_CRT_ALLOC_HOOK**CRTDBG içinde tanımlanan gibi. Y:  
  
```cpp
typedef int (__cdecl * _CRT_ALLOC_HOOK)  
    (int, void *, size_t, int, long, const unsigned char *, int);  
```  
  
 Çalışma zamanı kitaplığı, kanca çağırdığında *nAllocType* bağımsız değişkeni hangi ayırma gösterir işlemdir hakkında yapılacak (**_HOOK_ALLOC**, **_HOOK_REALLOC**, veya **_HOOK_FREE**). Ücretsiz veya bir reallocation `pvData` kullanıcı makaleyi serbest bırakılacak bloğunun bir işaretçiye sahiptir. Ancak bir ayırma için ayırma oluştuğundan henüz Bu işaretçi null. Kalan bağımsız değişkenleri ayırmanın boyutu söz konusu, blok türü ve dosya adı için bir işaretçi ile ilişkili ardışık istek numarasını içerir. Varsa, bağımsız değişkenlerin de ayırma yapıldığı satır numarasını içerir. Hangi analizi kanca işlevini gerçekleştirir ve diğer görevler, yazar istediği sonra ya da döndürmelidir **TRUE**, ayırma işlemi devam edebilir, gösteren veya **FALSE**gösteren, işlem başarısız olmalıdır. Bu tür bir basit kanca şimdiye ayrılan bellek miktarını denetleyin ve dönüş **FALSE** bu kadar küçük bir sınır aşılırsa. Uygulama türü yalnızca kullanılabilir bellek düşük olduğunda, normalde oluşacak ayırma hatalarının ardından deneyimleyeceği. Daha karmaşık kancaları ayırma desenlerini izlemek, bellek kullanımını analiz etme veya özel durumlar oluştuğunda bildirin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Atama kancaları ve C çalışma zamanı bellek ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md)   
 [Hata ayıklama kanca işlevi yazma](../debugger/debug-hook-function-writing.md)   
