---
title: 링크 요청
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security [.NET Framework], demands
- demanded permissions
- permissions [.NET Framework], demands
- granting permissions, demands
- code access security, demands
- user demands for permission
- caller security checks
- link demands
ms.assetid: a33fd5f9-2de9-4653-a4f0-d9df25082c4d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2ba3172b1a82c0a9f624a49eb63a193dd29faac1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166993"
---
# <a name="link-demands"></a>링크 요청
[!INCLUDE[net_security_note](../../../includes/net-security-note-md.md)]  
  
 링크 요청으로 인해 Just-In-Time 컴파일 동안 보안 검사를 수행하며 코드의 직접 호출 어셈블리만 검사합니다. 연결은 함수 포인터 참조 및 메서드 호출을 포함하여 코드가 형식 참조에 바인딩된 경우에 발생합니다. 호출 어셈블리에 코드에 연결할 권한이 없는 경우 링크가 허용되지 않으며 코드가 로드 및 실행될 때 런타임 예외가 발생합니다. 코드에서 상속하는 클래스에서 링크 요청을 재정의할 수 있습니다.  
  
 이 형식의 요청에서는 전체 스택 워크가 수행되지 않으며 코드가 여전히 보안 공격에 취약합니다. 예를 들어 어셈블리 A의에서 메서드가 링크 요청으로 보호 되 면 어셈블리 B에에서 있는 직접 호출자가 평가 어셈블리 B의 권한에 따라  그러나 링크 요청을 평가 하지 않습니다 어셈블리 C에 있는 메서드를 호출 하는 경우 직접 메서드를 사용 하 여 메서드 2. 어셈블리의 어셈블리에 링크 요청이 있는 권한만 있으면 직접 호출자가 직접 호출 어셈블리에 코드에 연결 해야 합니다. 지정 합니다. 모든 호출자가 코드를 실행하는 데 필요한 권한은 지정하지 않습니다.  
  
 <xref:System.Security.CodeAccessPermission.Assert%2A>, <xref:System.Security.CodeAccessPermission.Deny%2A> 및 <xref:System.Security.CodeAccessPermission.PermitOnly%2A> 스택 워크 한정자는 링크 요청의 평가에 영향을 주지 않습니다.  링크 요청은 스택 워크를 수행하지 않으므로 스택 워크 한정자가 링크 요청에 영향을 주지 않습니다.  
  
 링크 요청으로 보호 되는 메서드를 통해 액세스 하는 경우 [리플렉션](../../../docs/framework/reflection-and-codedom/reflection.md), 리플렉션을 통해 액세스 하는 코드의 직접 실행 호출자를 검사 합니다. 이는 리플렉션을 사용하여 수행된 메서드 호출 및 메서드 검색 둘 다에 적용됩니다. 예를 들어, 코드 리플렉션을 사용 하 여 반환 된 <xref:System.Reflection.MethodInfo> 링크 요청으로 보호 되 고 다음 전달 하는 메서드를 나타내는 개체 **MethodInfo** 개체를 사용 하 여 원래 메서드를 호출 하는 다른 코드로 개체입니다. 이 경우 링크 요청 검사가 두 번 발생: 반환 하는 코드에 한 번씩 합니다 **MethodInfo** 개체에 대해 한 번씩 호출 하는 코드입니다.  
  
> [!NOTE]
>  정적 생성자는 응용 프로그램 코드 실행 경로 외부의 시스템에서 호출되므로 정적 클래스 생성자에서 수행되는 링크 요청은 생성자를 보호하지 않습니다. 따라서 링크 요청이 전체 클래스에 적용되는 경우 클래스의 나머지 부분은 보호하지만 정적 생성자에 대한 액세스를 보호할 수 없습니다.  
  
 다음 코드 조각에서는 `ReadData` 메서드에 연결하는 코드에 `CustomPermission` 권한이 있어야 함을 선언적으로 지정합니다. 이 권한은 가상의 사용자 지정 권한이며 .NET Framework에 존재하지 않습니다. 전달 하 여 요청 됩니다는 **SecurityAction.LinkDemand** 플래그는 `CustomPermissionAttribute`합니다.  
  
```vb  
<CustomPermissionAttribute(SecurityAction.LinkDemand)> _  
Public Shared Function ReadData() As String  
    ' Access a custom resource.  
End Function    
```  
  
```csharp  
[CustomPermissionAttribute(SecurityAction.LinkDemand)]  
public static string ReadData()  
{  
    // Access a custom resource.  
}  
```  
  
## <a name="see-also"></a>참고자료

- [특성](../../../docs/standard/attributes/index.md)
- [코드 액세스 보안](../../../docs/framework/misc/code-access-security.md)
