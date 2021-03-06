---
title: EBindPolicyLevels 열거형
ms.date: 03/30/2017
api_name:
- EBindPolicyLevels
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EBindPolicyLevels
helpviewer_keywords:
- EBindPolicyLevels enumeration [.NET Framework hosting]
ms.assetid: a9e00b4f-b6d0-4257-bd88-4fe9af97b8fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8f2b08662e719a3308a62ab5b60f5dc490f2a6a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142209"
---
# <a name="ebindpolicylevels-enumeration"></a>EBindPolicyLevels 열거형
어셈블리 정책 적용 또는 수정 하는 수준을 지정 하는 플래그를 제공 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef enum {  
    ePolicyLevelNone         = 0x0,  
    ePolicyLevelRetargetable = 0x1,  
    ePolicyUnifiedToCLR      = 0x2,  
    ePolicyLevelApp          = 0x4,  
    ePolicyLevelPublisher    = 0x8,  
    ePolicyLevelHost         = 0x10,  
    ePolicyLevelAdmin        = 0x20  
    ePolicyPortability       = 0x40  
} EBindPolicyLevels;  
```  
  
## <a name="members"></a>멤버  
  
|멤버|설명|  
|------------|-----------------|  
|`ePolicyLevelAdmin`|관리자 수준에서 정책이 적용 수를 지정 합니다.|  
|`ePolicyLevelApp`|응용 프로그램 수준 정책이 적용 수를 지정 합니다.|  
|`ePolicyLevelHost`|호스트 수준 정책이 적용 수를 지정 합니다.|  
|`ePolicyLevelNone`|없는 정책 수준 플래그를 지정합니다.|  
|`ePolicyLevelPublisher`|게시자 수준의 정책이 적용 수를 지정 합니다.|  
|`ePolicyLevelRetargetable`|변수 수준에서 정책을 적용할 수 해야 지정 합니다.|  
|`ePolicyPortability`|정책에.NET Framework 어셈블리의 구현 간에 이식성을 지원 해야 한다고 지정 합니다. 참조 된 [ \<supportPortability >](../../../../docs/framework/configure-apps/file-schema/runtime/supportportability-element.md) 구성 파일 요소입니다.|  
|`ePolicyUnifiedToCLR`|정책에 통합 된 CLR (공용 언어 런타임) 하도록 지정 합니다.|  
  
## <a name="remarks"></a>설명  
 이 열거형의 메서드에 전달 되는 [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) 인터페이스 응용 프로그램 정책에서 변경 내용을 지정 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.h  
  
 **라이브러리:** MSCorEE.dll  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [ICLRAssemblyIdentityManager 인터페이스](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [호스팅 열거형](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
