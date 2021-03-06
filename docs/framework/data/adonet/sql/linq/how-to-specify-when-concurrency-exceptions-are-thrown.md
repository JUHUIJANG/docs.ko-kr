---
title: '방법: 동시성 예외가 throw되는 시기 지정'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 344ae068-ff63-4a2e-8b00-af22e143675f
ms.openlocfilehash: 30dd83c68472ecd3244cfc87b6df97b948b9a84f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182990"
---
# <a name="how-to-specify-when-concurrency-exceptions-are-thrown"></a>방법: 동시성 예외가 throw되는 시기 지정
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]에서 <xref:System.Data.Linq.ChangeConflictException> 예외는 낙관적 동시성 충돌 때문에 개체가 업데이트되지 않는 경우 throw됩니다. 자세한 내용은 참조 하세요. [낙관적 동시성: 개요](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md)합니다.  
  
 변경 내용을 데이터베이스에 전송하기 전에 동시성 예외가 throw되는 시점을 지정할 수 있습니다.  
  
-   첫 번째 실패 시 예외를 Throw합니다(<xref:System.Data.Linq.ConflictMode.FailOnFirstConflict>).  
  
-   모든 업데이트 시도를 완료하고 모든 실패를 누적하여 예외에 누적된 실패를 보고합니다(<xref:System.Data.Linq.ConflictMode.ContinueOnConflict>).  
  
 Throw되면 <xref:System.Data.Linq.ChangeConflictException> 예외에서 <xref:System.Data.Linq.ChangeConflictCollection> 컬렉션에 대한 액세스를 제공합니다. 이 컬렉션에서는 <xref:System.Data.Linq.ObjectChangeConflict.MemberConflicts%2A> 컬렉션에 대한 액세스를 포함하여 실패한 단일 업데이트 시도에 매핑된 각 충돌에 대한 자세한 내용을 제공합니다. 각 멤버 충돌은 동시성 확인에 실패한 업데이트의 단일 멤버에 매핑됩니다.  
  
## <a name="example"></a>예제  
 다음 코드에서는 두 값의 예제를 보여 줍니다.  
  
 [!code-csharp[System.Data.Linq.ConflictModeEnumeration#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.conflictmodeenumeration/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ConflictModeEnumeration#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.conflictmodeenumeration/vb/module1.vb#1)]  
  
## <a name="see-also"></a>참고자료

- [방법: 변경 내용 충돌 관리](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
- [데이터 변경 및 변경 내용 전송](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
