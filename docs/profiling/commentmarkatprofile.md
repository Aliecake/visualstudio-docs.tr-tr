---
title: CommentMarkAtProfile | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- CommentMarkAtProfile
- CommentMarkAtProfileA
ms.assetid: 04294ca3-bf9c-4c76-86f1-898c2140de27
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d0eaaac47470378730c526b01b2ce2b637af5cd6
ms.sourcegitcommit: f685fa5e2df9dc307bf1230dd9dc3288aaa408b5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36233704"
---
# <a name="commentmarkatprofile"></a>CommentMarkAtProfile
`CommentMarkAtProfile` Yöntemi, bir zaman damgası değeri, sayısal işareti ve bir açıklama dizesi olarak ekler. *Vsp* dosya. Zaman damgası değeri dış olayları eşitlemek için kullanılır. CommentMarkAtProfile işlevi içeriyor iş parçacığı için profil oluşturma, işareti ve eklenecek açıklama için açık olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
PROFILE_COMMAND_STATUS PROFILERAPI CommentMarkAtProfile (  
                                   __int64 dnTimestamp,  
                                   long lMarker,  
                                   LPCTSTR szComment);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dnTimestamp`  
  
 Bir zaman damgası değeri temsil eden bir 64-bit tam sayı.  
  
 `lMarker`  
  
 Eklenecek sayısal işaretçisi. İşaretin 0 (sıfır) değerine eşit veya daha büyük olmalıdır.  
  
 `szComment`  
  
 Metin dizesi eklemek için bir işaretçi. Dize NULL Sonlandırıcı dahil olmak üzere 256 karakterden kısa olmalıdır.  
  
## <a name="property-valuereturn-value"></a>Özellik değeri/dönüş değeri  
 Kullanarak işlevi başarısını veya başarısızlığını gösterir **PROFILE_COMMAND_STATUS** numaralandırması. Dönüş değeri aşağıdakilerden biri olabilir:  
  
|Numaralandırıcı|Açıklama|  
|----------------|-----------------|  
|MARK_ERROR_MARKER_RESERVED|Parametre, küçük veya 0 değerine eşit değil. Bu değerler ayrılmıştır. Açıklama ve işareti kaydedilmedi.|  
|MARK_ERROR_MODE_NEVER|Hiçbir zaman işlevi çağrıldığında profil oluşturma modu ayarlandı. Açıklama ve işareti kaydedilmedi.|  
|MARK_ERROR_MODE_OFF|İşlevi çağrıldığında profil oluşturma modu OFF olarak ayarlandı. Açıklama ve işareti kaydedilmedi.|  
|MARK_ERROR_NO_SUPPORT|Bu bağlamda işareti desteği yok. Açıklama ve işareti kaydedilmedi.|  
|MARK_ERROR_OUTOFMEMORY|Olay kaydetmek bellek yoktu. Açıklama ve işareti kaydedilmedi.|  
|MARK_TEXTTOOLONG|Dize en fazla 256 karakter aşıyor. Açıklama dizesi kesilir ve yorum ve işareti kaydedilir.|  
|MARK_OK|MARK_OK başarılı olduğunu belirtmek için döndürülür.|  
  
## <a name="remarks"></a>Açıklamalar  
 İşaretleri ve yorumları API işlevleri (CommentMarkAtProfile, CommentMarkProfile veya MarkProfile) veya işareti komutu ile yerleştirildiğinde işareti profili işlevi içeren iş parçacığı için profil oluşturma durumu olmalıdır. Profil işaretleri kapsamda geneldir. Örneğin, bir iş parçacığında eklenen bir profili işareti başlangıç ya da herhangi bir iş parçacığı .vsp dosyasındaki veri segmentinin sonunu işaretlemek için kullanılabilir.  
  
> [!IMPORTANT]
>  CommentMarkAtProfile yöntemleri yalnızca araçları ile kullanılmalıdır.  
  
## <a name="net-framework-equivalent"></a>.NET framework eşdeğeri  
 *Microsoft.VisualStudio.Profiler.dll*  
  
## <a name="function-information"></a>İşlev bilgisi  
  
|||  
|-|-|  
|**Üstbilgi**|Dahil *VSPerf.h*|  
|**Kitaplığı**|Kullanım *VSPerf.lib*|  
|**Unicode**|CommentMarkAtProfileW (Unicode) ve CommentMarkAtProfileA (ANSI) uygulanır.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod CommentMarkAtProfile genel işlev çağrısının kullanımını gösterir. Örnek Win32 dize makroların kullanılması ve kod çağrıları ANSI işlevi etkin olup olmadığını belirlemek ANSI derleyici ayarları varsayar.  
  
```cpp  
void ExerciseCommentMarkAtProfile(void)  
{  
    // Declare and initalize variables to pass to   
    // CommentMarkAtProfile.  The values of these   
    // parameters are assigned based on the needs   
    // of the code; and for the sake of simplicity  
    // in this example, the variables are assigned  
    // arbitrary values.  
    int64 timeStamp = 0x1111;  
    long markId = 01;  
    TCHAR * markText = TEXT("Exercising CommentMarkAtProfile...");  
  
    // Variables used to print output.  
    HRESULT hResult;  
    TCHAR tchBuffer[256];  
  
    // Declare MarkOperationResult Enumerator.    
    // Holds return value from call to CommentMarkAtProfile.  
    PROFILE_COMMAND_STATUS markResult;  
  
    markResult = CommentMarkAtProfile(  
        timeStamp,  
        markId,  
        markText);  
  
    // Format and print result.  
    LPCTSTR pszFormat = TEXT("%s %d.\0");  
    TCHAR* pszTxt = TEXT("CommentMarkAtProfile returned");  
    hResult = StringCchPrintf(tchBuffer, 256, pszFormat,   
    pszTxt, markResult);  
  
#ifdef DEBUG  
    OutputDebugString(tchBuffer);  
#endif  
}  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio profil oluşturucu API Başvurusu (yerel)](../profiling/visual-studio-profiler-api-reference-native.md)