---
title: ICorDebugProcess2::GetThreadForTaskID 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.GetThreadForTaskID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::GetThreadForTaskID
helpviewer_keywords:
- ICorDebugProcess2::GetThreadForTaskId method [.NET Framework debugging]
- GetThreadForTaskID method [.NET Framework debugging]
ms.assetid: 32d54a5b-8ad3-405b-a1b9-0936a3b49d1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa1f6852544dddcdf514b14710ade3949818c93e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487315"
---
# <a name="icordebugprocess2getthreadfortaskid-method"></a>ICorDebugProcess2::GetThreadForTaskID 메서드
지정한 식별자를 가진 태스크를 실행 하는 스레드를 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetThreadForTaskID (  
    [in]  TASKID            taskid,  
    [out] ICorDebugThread2  **ppThread  
);  
```  
  
## <a name="parameters"></a>매개 변수  
 `taskid`  
 [in] 작업의 식별자입니다.  
  
 `ppThread`  
 [out] 검색할 스레드를 나타내는 ICorDebugThread2 개체의 주소에 대 한 포인터입니다.  
  
## <a name="remarks"></a>설명  
 호스트를 사용 하 여 작업 식별자를 설정할 수는 [iclrtask:: Settaskidentifier](../../../../docs/framework/unmanaged-api/hosting/iclrtask-settaskidentifier-method.md) 메서드.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorDebug.idl, CorDebug.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
