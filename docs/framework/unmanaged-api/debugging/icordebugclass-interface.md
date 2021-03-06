---
title: ICorDebugClass 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass
helpviewer_keywords:
- ICorDebugClass interface [.NET Framework debugging]
ms.assetid: 03a6facb-f12f-49be-9839-e73b9c791cd5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e1ad830e728fbe764085a5808a48e4cacedc595
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133629"
---
# <a name="icordebugclass-interface"></a>ICorDebugClass 인터페이스

기본 또는 복합(즉, 사용자 정의) 형식을 나타냅니다. 형식이 제네릭이면 `ICorDebugClass`는 인스턴스화되지 않은 제네릭 형식을 나타냅니다.  
  
## <a name="methods"></a>메서드  
  
|메서드|설명|  
|------------|-----------------|  
|[GetModule 메서드](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-getmodule-method.md)|이 클래스를 정의 하는 모듈을 가져옵니다.|  
|[GetStaticFieldValue 메서드](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-getstaticfieldvalue-method.md)|지정된 된 정적 필드의 값을 가져옵니다.|  
|[GetToken 메서드](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-gettoken-method.md)|가져옵니다는 `TypeDef` 이 클래스에 대 한 메타 데이터 토큰입니다.|  
  
## <a name="remarks"></a>설명  
 `ICorDebugClass` 인터페이스는 인스턴스화되지 않은 제네릭 형식을 나타냅니다. ICorDebugType 인터페이스 인스턴스화된 제네릭 형식을 나타냅니다. 예를 들어 `Hashtable<K, V>` 나타납니다 `ICorDebugClass`인 반면 `Hashtable<Int32, String>` 을 표시 `ICorDebugType`합니다.  
  
 제네릭이 아닌 형식은 둘 다 표시 됩니다 `ICorDebugClass` 고 `ICorDebugType`입니다. 두 번째 인터페이스 형식 인스턴스화를 사용 하 여 처리 하는.NET Framework 버전 2.0에서에서 도입 되었습니다.  
  
> [!NOTE]
>  이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** CorDebug.idl, CorDebug.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [디버깅 인터페이스](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
