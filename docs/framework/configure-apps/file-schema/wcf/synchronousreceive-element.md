---
title: <synchronousReceive> 요소
ms.date: 03/30/2017
ms.assetid: cc070387-3d11-4b02-a952-bc08ad2df05a
ms.openlocfilehash: 20390f747c8beaccba1cfea7a9ea0ed366037ecb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166545"
---
# <a name="synchronousreceive-element"></a>\<synchronousReceive > 요소
이 구성 요소는 서비스 또는 클라이언트 응용 프로그램에서 메시지 수신을 위한 런타임 동작을 지정하는 데 사용됩니다. 이 구성 요소에는 특성이나 자식 요소가 없습니다.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<synchronousReceive>  
  
## <a name="syntax"></a>구문  
  
```xml  
<synchronousReceive />
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|엔드포인트 동작을 지정합니다.|  
  
## <a name="remarks"></a>설명  
 채널 수신기에 기본값(비동기) 대신 동기 수신을 사용하도록 지시하려면 이 동작을 사용합니다. Windows Communication Foundation (WCF)를 수락 된 각 채널에 대해 공급할 새 스레드를 발급 합니다. 채널이 많은 경우 스레드가 부족할 수 있습니다.  
  
## <a name="see-also"></a>참고자료

- <xref:System.ServiceModel.Configuration.SynchronousReceiveElement>
- <xref:System.ServiceModel.Description.SynchronousReceiveBehavior>
