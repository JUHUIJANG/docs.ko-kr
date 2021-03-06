---
title: GetType 연산자(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.GetType
helpviewer_keywords:
- GetType operator [Visual Basic]
- GetType keyword [Visual Basic]
ms.assetid: 4f733297-2503-4607-850c-15eba65fff90
ms.openlocfilehash: 34ab192814583db5cdc0d0183c73cc22b8633e9c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58840323"
---
# <a name="gettype-operator-visual-basic"></a>GetType 연산자(Visual Basic)
반환 된 <xref:System.Type> 지정 된 형식의 개체입니다. <xref:System.Type> 개체는 해당 속성, 메서드 및 이벤트와 같은 유형에 대 한 정보를 제공 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
GetType(typename)  
```  
  
## <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---|---|  
|`typename`|이름 정보를 원하는 형식입니다.|  
  
## <a name="remarks"></a>설명  
 합니다 `GetType` 연산자를 반환 합니다 <xref:System.Type> 지정 된 개체 `typename`합니다. 에 정의 된 형식의 이름을 전달할 수 있습니다 `typename`합니다. 여기에는 다음과 같은 사항이 포함됩니다.  
  
-   와 같은 모든 Visual Basic 데이터 형식 `Boolean` 또는 `Date`합니다.  
  
-   모든.NET Framework 클래스, 구조체, 모듈 또는 인터페이스와 같은 <xref:System.ArgumentException?displayProperty=nameWithType> 또는 <xref:System.Double?displayProperty=nameWithType>합니다.  
  
-   모든 클래스, 구조체, 모듈 또는 응용 프로그램에서 정의 된 인터페이스입니다.  
  
-   응용 프로그램에서 정의한 모든 배열입니다.  
  
-   응용 프로그램에서 정의한 모든 대리자입니다.  
  
-   Visual Basic,.NET Framework 또는 응용 프로그램에 정의 된 모든 열거형입니다.  
  
 개체 변수의 형식 개체를 가져오려는 경우 사용 된 <xref:System.Type.GetType%2A?displayProperty=nameWithType> 메서드.  
  
 `GetType` 연산자는 다음과 같은 경우에 유용할 수 있습니다.  
  
-   런타임 시 형식에 대 한 메타 데이터에 액세스 해야 합니다. <xref:System.Type> 개체 형식 멤버 및 배포 정보 같은 메타 데이터를 제공 합니다. 해야이 예를 들어, 어셈블리를 반영 합니다. 자세한 내용은 <xref:System.Reflection?displayProperty=nameWithType>을 참조하세요.  
  
-   두 개체 참조는 동일한 형식의 인스턴스를 참조 하는 경우를 비교 하려고 합니다. 이렇게 되 면 `GetType` 동일에 대 한 참조를 반환 합니다. <xref:System.Type> 개체입니다.  
  
## <a name="example"></a>예제  
 다음 예제에 나온은 `GetType` 연산자를 사용에서 합니다.  
  
 [!code-vb[VbVbalrOperators#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#26)]  
  
## <a name="see-also"></a>참고자료

- [Visual Basic에서의 연산자 우선 순위](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [기능별 연산자 목록](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [연산자 및 식](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
