---
title: '방법: WebRequest와 일치하는 프로토콜 관련 WebResponse 검색'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: fee2b725afbceef45b9651a7cd88a61b37952e32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59087380"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a>방법: WebRequest와 일치하는 프로토콜 관련 WebResponse 검색
이 예제에서는 WebRequest와 일치하는 프로토콜별 WebResponse를 검색하는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
WebResponse resp = req.GetResponse();  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com")  
Dim resp As WebResponse = req.GetResponse()  
```  
  
## <a name="compiling-the-code"></a>코드 컴파일  
 이 예제에는 다음 사항이 필요합니다.  
  
-   **System.Net** 네임스페이스에 대한 참조.  
  
## <a name="see-also"></a>참고 항목

- [데이터 요청](../../../docs/framework/network-programming/requesting-data.md)
