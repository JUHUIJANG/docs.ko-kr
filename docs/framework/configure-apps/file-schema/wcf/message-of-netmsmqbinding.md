---
title: <netMsmqBinding>의 <message>
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: c623b7daf1e91c9c1800b9653525cd51b1087506
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58890568"
---
# <a name="message-of-netmsmqbinding"></a>\<message> of \<netMsmqBinding>

이 `netMsmqBinding` 바인딩에 대한 SOAP 메시지 보안 설정을 정의합니다.

```xml
<system.ServiceModel>
  <bindings>
    <netMsmqBinding>
      <binding>
        <security>
          <message>
```

## <a name="syntax"></a>구문

```xml
<netMsmqBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
    </security>
  </binding>
</netMsmqBinding>
```

## <a name="attributes-and-elements"></a>특성 및 요소

다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.

### <a name="attributes"></a>특성

|특성|설명|
|---------------|-----------------|
|algorithmSuite|MSMQ 전송을 통해 전송되는 메시지에 메시지 기반 보안을 적용하는 데 사용되는 메시지 암호화 및 키 랩 알고리즘을 설정합니다.<br /><br /> 기본값은 `Aes256`입니다. 이 특성은 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> 형식입니다.|
|clientCredentialType|MSMQ 전송을 통해 전송되는 메시지에 대해 클라이언트 인증을 수행할 때 사용되는 자격 증명의 형식을 지정합니다. 유효한 값은 다음과 같습니다.<br /><br /> -None. 이를 통해 서비스와 익명 클라이언트가 상호 작용할 수 있습니다. 서비스와 클라이언트 모두 자격 증명이 필요하지 않습니다.<br />-   Windows: 이 통해 Windows 자격 증명의 인증 된 컨텍스트에서 SOAP 교환이 이루어지도록 합니다. 이 설정은 항상 Kerberos 기반 인증을 수행합니다.<br />-   UserName: 이 필요 하도록 서비스를 통해 클라이언트가 UserName 자격 증명을 사용 하 여 인증할 수 있습니다. 자격 증명을 사용 하 여 지정 해야이 경우에 `clientCredentials` 동작 **주의 해야 합니다.**  Windows Communication Foundation (WCF)는 암호 다이제스트를 보내거나 암호를 사용 하 고 메시지 보안에 이러한 키를 사용 하 여 키를 파생를 지원 하지 않습니다. 따라서 WCF 사용자 이름 자격 증명을 사용 하는 경우 교환에 보안을 적용 합니다. 이 모드에서는 `clientCredential` 동작 및 `serviceCertificate`를 사용하여 클라이언트에 서비스 인증서를 지정해야 합니다. <br /><br /> -인증서: 이 필요 하도록 서비스를 통해 인증서를 사용 하 여 클라이언트 인증입니다. 이 경우 `clientCredentials` 동작을 사용하여 클라이언트 자격 증명을 지정해야 합니다. 이 경우 `clientCredentials`를 지정하여 `serviceCertificate` 동작을 통해 서비스 자격 증명을 지정해야 합니다.<br />-CardSpace 합니다. 필요 하도록 서비스를 사용 하면이 클라이언트는 CardSpace를 사용 하 여 인증할 수 있습니다. `serviceCertificate` 동작에 `clientCredential`가 제공되어야 합니다.<br /><br /> 기본값은 `Windows`입니다. 이 특성은 <xref:System.ServiceModel.MessageCredentialType> 형식입니다.|

### <a name="child-elements"></a>자식 요소

없음

### <a name="parent-elements"></a>부모 요소

|요소|설명|
|-------------|-----------------|
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|바인딩에 대한 보안 설정을 정의합니다.|

## <a name="see-also"></a>참고자료

- <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>
- <xref:System.ServiceModel.MessageSecurityOverMsmq>
- [WCF의 큐](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [서비스 및 클라이언트에 보안 설정](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [바인딩](../../../../../docs/framework/wcf/bindings.md)
- [시스템 제공 바인딩 구성](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [바인딩을 사용하여 서비스 및 클라이언트 구성](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
