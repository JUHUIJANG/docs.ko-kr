---
title: 이 컨텍스트에서는 nullable 형식을 유추할 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 9f7f878649d8b96f050b56d5b878eb3d67e027ff
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819244"
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a>이 컨텍스트에서는 nullable 형식을 유추할 수 없습니다.
값 형식 및 구조는 nullable 선언할 수 있습니다.  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 그러나 nullable 선언 형식 유추와 함께에서 사용할 수 없습니다. 다음 예제에서는이 오류가 발생 합니다.  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **오류 ID:** BC36629  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
-   사용 하 여는 `As` 절 null 허용으로 변수를 선언 합니다.  
  
## <a name="see-also"></a>참고자료

- [Nullable 값 형식](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [지역 형식 유추](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
