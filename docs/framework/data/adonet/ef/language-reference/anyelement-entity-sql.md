---
title: ANYELEMENT(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 475a9ad6-8c8d-4f49-9970-af273e5360f1
ms.openlocfilehash: ff79417008b7807fbf206d4bcb65b4e5ea1cc576
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59296136"
---
# <a name="anyelement-entity-sql"></a>ANYELEMENT(Entity SQL)
다중값 컬렉션에서 요소를 추출합니다.  
  
## <a name="syntax"></a>구문  
  
```  
ANYELEMENT ( expression )  
```  
  
## <a name="arguments"></a>인수  
 `expression`  
 요소를 추출할 컬렉션을 반환하는 유효한 쿼리 식입니다.  
  
## <a name="return-value"></a>반환 값  
 컬렉션의 단일 요소 또는 임의 요소(컬렉션에 여러 요소가 있는 경우)를 반환하거나 컬렉션이 비어 있는 경우 `null`을 반환합니다. 하는 경우 `collection` 형식의 컬렉션인 `Collection<T>`, 한 다음 `ANYELEMENT(collection)` 형식의 인스턴스를 생성 하는 유효한 식입니다 `T`합니다.  
  
## <a name="remarks"></a>설명  
 ANYELEMENT는 다중값 컬렉션에서 임의의 요소를 추출합니다. 예를 들어, 다음 예제에서는 `Customers`집합에서 singleton 요소를 추출하려고 시도합니다.  
  
```  
ANYELEMENT(Customers)  
```  
  
## <a name="example"></a>예제  
 다음 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 쿼리에서는 ANYELEMENT 연산자를 사용하여 다중값 컬렉션에서 요소를 추출합니다. 쿼리는 AdventureWorks Sales 모델을 기반으로 합니다. 이 쿼리를 컴파일하고 실행하려면 다음 단계를 수행하세요.  
  
1. 절차에 따라 [방법: StructuralType 결과 반환 하는 쿼리 실행](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)합니다.  
  
2. 다음 쿼리를 `ExecuteStructuralTypeQuery` 메서드에 인수로 전달합니다.  
  
 [!code-csharp[DP EntityServices Concepts 2#ANYELEMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#anyelement)]  
  
## <a name="see-also"></a>참고자료

- [엔터티 SQL 참조](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [null 허용 구조적 형식](../../../../../../docs/framework/data/adonet/ef/language-reference/nullable-structured-types-entity-sql.md)
