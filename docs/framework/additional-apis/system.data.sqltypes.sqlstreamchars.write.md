---
title: SqlStreamChars.Write (Char, Int32, Int32) 메서드 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: dd9bb691f6d07f4875d684eef76d6329667003af
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221910"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a><span data-ttu-id="6a83a-102">(Char, Int32, Int32) SqlStreamChars.Write 메서드</span><span class="sxs-lookup"><span data-stu-id="6a83a-102">SqlStreamChars.Write(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="6a83a-103">파생된 클래스에서 재정의 문자의 시퀀스를 현재 스트림에 쓰고 쓴 문자 수 만큼이 스트림 내의 현재 위치를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-103">When overridden in a derived class, writes a sequence of characters to the current stream and advances the current position within this stream by the number of characters written.</span></span> <span data-ttu-id="6a83a-104">이 메서드를 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="6a83a-105">SQL Server에서 사용할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="6a83a-106">다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="6a83a-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a83a-107">Parameters</span></span>

`buffer`  
<span data-ttu-id="6a83a-108">쓸 문자 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-108">A char array to write.</span></span>

`offset`  
<span data-ttu-id="6a83a-109">원점 기준으로 하는 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-109">An offset relative to origin.</span></span>

`count`  
<span data-ttu-id="6a83a-110">현재 스트림에 쓸 문자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-110">The number of characters to be written to the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a83a-111">설명</span><span class="sxs-lookup"><span data-stu-id="6a83a-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="6a83a-112">`SqlStreamChars.Write` 메서드가 private 이며 코드에서 직접 사용할 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-112">The `SqlStreamChars.Write` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="6a83a-113">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-113">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a83a-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6a83a-114">Requirements</span></span>

<span data-ttu-id="6a83a-115">**네임스페이스:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="6a83a-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="6a83a-116">**어셈블리:** System.Data (System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="6a83a-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="6a83a-117">**.NET framework 버전:** 2.0부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-117">**.NET Framework versions:** Available since 2.0.</span></span>