---
title: COR_PRF_SNAPSHOT_INFO 열거형
ms.date: 03/30/2017
api_name:
- COR_PRF_SNAPSHOT_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_SNAPSHOT_INFO
helpviewer_keywords:
- COR_PRF_SNAPSHOT_INFO enumeration [.NET Framework profiling]
ms.assetid: a5906b2a-ad4a-4cc6-a421-2d7d8adf7468
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fa85fb2cebb47ecbd7b0f091cb79f6ea0936b1cb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177842"
---
# <a name="corprfsnapshotinfo-enumeration"></a>COR_PRF_SNAPSHOT_INFO 열거형
얼마나 프로파일러의 각 호출 스택의 스냅숏을 사용 하 여 다시 전달할 데이터 지정 [StackSnapshotCallback](../../../../docs/framework/unmanaged-api/profiling/stacksnapshotcallback-function.md) 함수입니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef enum _COR_PRF_SNAPSHOT_INFO {  
    COR_PRF_SNAPSHOT_DEFAULT = 0x0,  
    COR_PRF_SNAPSHOT_REGISTER_CONTEXT = 0x1,  
    COR_PRF_SNAPSHOT_X86_OPTIMIZED = 0X2  
} COR_PRF_SNAPSHOT_INFO;  
```  
  
## <a name="members"></a>멤버  
  
|멤버|설명|  
|-------------|-----------------|  
|`COR_PRF_SNAPSHOT_DEFAULT`|모든 값을 전달 해야 나타냅니다 `StackSnapshotCallback` 매개 변수를 제외 하 고는 `context` 매개 변수입니다.|  
|`COR_PRF_SNAPSHOT_REGISTER_CONTEXT`|모든 값을 전달 해야 나타냅니다 `StackSnapshotCallback` 매개 변수를 포함 하 여는 `context` 매개 변수입니다.|  
|`COR_PRF_SNAPSHOT_X86_OPTIMIZED`|간단 하 고 대체 스택 워킹 알고리즘 사용 됨을 나타냅니다.|  
  
## <a name="remarks"></a>설명  
 제공 하는 값을 `COR_PRF_SNAPSHOT_INFO` 열거형을 매개 변수로 전달 되는 [DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) 메서드.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorProf.idl, CorProf.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [DoStackSnapshot 메서드](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md)
- [프로파일링 열거형](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
