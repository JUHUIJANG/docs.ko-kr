---
title: ICorProfilerCallback::ExceptionUnwindFunctionEnter 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionUnwindFunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter method [.NET Framework profiling]
- ExceptionUnwindFunctionEnter method [.NET Framework profiling]
ms.assetid: ea3dc625-5650-4bf4-8e67-01e42be065b1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0451ceac3018a3bab697a8ac82f5ef84f1026c6d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150789"
---
# <a name="icorprofilercallbackexceptionunwindfunctionenter-method"></a>ICorProfilerCallback::ExceptionUnwindFunctionEnter 메서드
예외 처리의 해제 단계는 함수를 해제 하려면 시작 되었음을 프로파일러에 알립니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT ExceptionUnwindFunctionEnter(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a>매개 변수  
 `functionId`  
 [in] ID가 위치 하는 함수입니다.  
  
## <a name="remarks"></a>설명  
 가비지 수집을 허용 하는 상태가 스택의 되었을 수 있으므로이 메서드의 구현에서 프로파일러 차단 되지 않아야 하 고 따라서 preemptive 가비지 수집을 사용할 수 없습니다. 프로파일러 여기 차단 하는 경우 가비지 수집을 시도 하 고, 런타임이이 콜백에서 반환 될 때까지 차단 됩니다.  
  
 이 메서드 구현은 프로파일러의 관리 되는 메모리 할당에서 또는 관리 코드를 호출 하지 않습니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorProf.idl, CorProf.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [ICorProfilerCallback 인터페이스](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ExceptionUnwindFunctionLeave 메서드](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfunctionleave-method.md)
