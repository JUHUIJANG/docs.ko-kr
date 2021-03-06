---
title: ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.SetEnterLeaveFunctionHooks2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::SetEnterLeaveFunctionHooks2
helpviewer_keywords:
- ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 method [.NET Framework profiling]
- SetEnterLeaveFunctionHooks2 method [.NET Framework profiling]
ms.assetid: 3c26b3e7-f72b-48a5-bf8c-edc122523a4b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b9f95a404ce7124a76ee527cdc70ccccf103838b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076798"
---
# <a name="icorprofilerinfo2setenterleavefunctionhooks2-method"></a>ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 메서드
업데이트 된 버전의 "입력", "유지" 및 "tailcall" 후크 관리 되는 함수에서 호출 되는 프로파일러 구현 함수를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT SetEnterLeaveFunctionHooks2(  
    [in] FunctionEnter2    *pFuncEnter,  
    [in] FunctionLeave2    *pFuncLeave,  
    [in] FunctionTailcall2 *pFuncTailcall);  
```  
  
## <a name="parameters"></a>매개 변수  
 `pFuncEnter`  
 [in] 로 사용할 구현에 대 한 포인터를 [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md) 콜백 합니다.  
  
 `pFuncLeave`  
 [in] 로 사용할 구현에 대 한 포인터를 [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md) 콜백 합니다.  
  
 `pFuncTailcall`  
 [in] 로 사용할 구현에 대 한 포인터를 [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) 콜백 합니다.  
  
## <a name="remarks"></a>설명  
 합니다 `SetEnterLeaveFunctionHooks2` 메서드는 비슷합니다는 [icorprofilerinfo:: Setenterleavefunctionhooks](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setenterleavefunctionhooks-method.md) 메서드. Enter/leave/tailcall 콜백 되 고 후자의 최신 버전으로 enter/leave/tailcall 콜백의 이전 버전으로 사용할 함수를 지정 하는 데 사용할 함수를 지정 하는 전자를 사용 합니다.  
  
 한 번에 하나의 집합만 콜백 active 수 있습니다. 따라서 프로파일러 둘 다 호출 하는 경우 `ICorProfilerInfo::SetEnterLeaveFunctionHooks` 하 고 `SetEnterLeaveFunctionHooks2`, `SetEnterLeaveFunctionHooks2` 사용 됩니다.  
  
 합니다 `SetEnterLeaveFunctionHooks2` 프로파일러의 에서만 메서드를 호출할 수 있습니다 [icorprofilercallback:: Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) 콜백 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorProf.idl, CorProf.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [ICorProfilerInfo 인터페이스](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [ICorProfilerInfo2 인터페이스](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
