---
title: '방법: 복사 생성자 작성 - C# 프로그래밍 가이드'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: 169bdfc53d0c30ffc14e5a9525920679a94fbf23
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56982143"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a>방법: 복사 생성자 작성(C# 프로그래밍 가이드)
C#에서는 개체에 대한 복사 생성자를 제공하지 않지만 직접 작성할 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 예제에서 `Person`[클래스](../../../csharp/language-reference/keywords/class.md)는 `Person` 인스턴스를 해당 인수로 사용하는 복사 생성자를 정의합니다. 인수의 속성 값이 `Person`의 새 인스턴스 속성에 할당됩니다. 코드에는 복사하려는 인스턴스의 `Name` 및 `Age` 속성을 클래스의 인스턴스 생성자에 보내는 대체 복사 생성자가 포함되어 있습니다.  
  
 [!code-csharp[csProgGuideObjects#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#16)]  
  
## <a name="see-also"></a>참고 항목

- <xref:System.ICloneable>
- [C# 프로그래밍 가이드](../../../csharp/programming-guide/index.md)
- [클래스 및 구조체](../../../csharp/programming-guide/classes-and-structs/index.md)
- [생성자](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [종료자](../../../csharp/programming-guide/classes-and-structs/destructors.md)
