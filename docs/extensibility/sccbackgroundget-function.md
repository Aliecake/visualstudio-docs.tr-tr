---
title: "SccBackgroundGet işlevi | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccBackgroundGet
helpviewer_keywords: SccBackgroundGet function
ms.assetid: 69817e52-b9ac-4f4d-820b-2cc9c384f0dc
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 85b700f0cb1e3a364cae69ff6c628151ea6a7bd3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2017
---
# <a name="sccbackgroundget-function"></a>SccBackgroundGet işlevi
Kaynak denetiminden her belirtilen dosyaların kullanıcı etkileşimi olmadan bu işlevi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
SCCRTN SccBackgroundGet(  
   LPVOID  pContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LONG    dwFlags,  
   LONG    dwBackgroundOperationID  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pContext  
 [in] Kaynak Denetim eklentisi bağlam işaretçi.  
  
 nFiles  
 [in] Belirtilen dosya sayısı `lpFileNames` dizi.  
  
 lpFileNames  
 [içinde out] Alınacak dosya adlarını dizisi.  
  
> [!NOTE]
>  Adları tam yerel dosya adları olmalıdır.  
  
 dwFlags  
 [in] Komut bayrakları (`SCC_GET_ALL`, `SCC_GET_RECURSIVE`).  
  
 dwBackgroundOperationID  
 [in] Bu işlemle ilişkili benzersiz bir değerdir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürmek için bu işlevi kaynak denetimi eklenti uyarlamasını beklenen:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|SCC_OK|İşlem başarıyla tamamlandı.|  
|SCC_E_BACKGROUNDGETINPROGRESS|Arka plan alma (yalnızca eşzamanlı toplu işlemleri desteklemiyorsa, eklenti kaynak denetimi bu döndürmelidir) sürüyor.|  
|SCC_I_OPERATIONCANCELED|İşlem tamamlandı önce iptal edildi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işlev, kaynak denetim eklentisi yüklü olandan farklı bir iş parçacığı üzerinde her zaman çağrılır. Bu işlev tamamlanıncaya kadar döndürmek için beklenmiyor; Ancak, birden çok kez dosyalarının, tümü aynı anda birden çok listeleriyle çağrılabilir.  
  
 Kullanımını `dwFlags` bağımsız değişkeni aynı olup [SccGet](../extensibility/sccget-function.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetim eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)   
 [SccGet](../extensibility/sccget-function.md)