---
title: <providerOption> 요소
ms.date: 03/30/2017
f1_keywords:
- provideroption
helpviewer_keywords:
- <provideroption> element
- providerOptions
- provideroption element
ms.assetid: 014f2e0b-c0b5-4fc4-92d3-73f02978b2a1
ms.openlocfilehash: 9c69ea7bf95b311a796ec29d90410a77b748c3c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59229786"
---
# <a name="provideroption-element"></a>\<providerOption > 요소
언어 공급자에 대 한 컴파일러 버전 특성을 지정합니다.  
  
 \<구성 요소 >  
\<system.codedom Element>  
\<compilers 요소 >  
\<컴파일러 > 요소  
\<providerOption > 요소  
  
## <a name="syntax"></a>구문  
  
```xml  
<providerOption  
  name="option-name"  
  value="option-value"  
/>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|`name`|필수 특성입니다.<br /><br /> 옵션의 이름을 지정합니다. 예를 들어, "CompilerVersion"가 있습니다.|  
|`value`|필수 특성입니다.<br /><br /> 옵션의 값을 지정합니다. 예를 들어, "v3.5"가 있습니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<configuration> 요소](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.|  
|[\<system.codedom > 요소](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|사용 가능한 언어 공급자에 대한 컴파일러 구성 설정을 지정합니다.|  
|[\<컴파일러 > 요소](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|컴파일러 구성 요소에 대 한 컨테이너 0 개 이상 포함 `<compiler>` 요소입니다.|  
|[\<compiler> 요소](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|언어 공급자에 대한 컴파일러 구성 특성을 지정합니다.|  
  
## <a name="remarks"></a>설명  
 .NET Framework 버전 3.5에서 코드 문서 개체 모델 (CodeDOM) 코드 공급자를 지원할 수 있습니다 공급자별 옵션 사용 하 여는 `<providerOption>` 요소입니다.  
  
 .NET Framework 3.5는 업데이트 된.NET Framework 2.0 어셈블리를 포함 하 고 새 형식을 포함 하는 새 버전 3.5 어셈블리를 제공 합니다. Microsoft C# 및 Visual Basic 코드 공급자를.NET Framework 2.0 어셈블리에 포함 되어 있지만 버전 3.5 컴파일러를 지원 하도록 업데이트 되었습니다. 기본적으로 업데이트 된 코드 공급자는 버전 2.0 컴파일러에 대 한 코드를 생성합니다. 사용할 수는 `<providerOption>` 3.5를 대상 컴파일러 버전을 변경 하는 요소입니다. 이 작업을 수행 하려면 "CompilerVersion"를 지정 하는 `name` 특성과 "v3.5"에 대 한는 `value` 특성입니다. 소문자 "v"를 사용 하 여 버전 번호를 빨라야 합니다.  
  
 가능 버전 사양을 전역 추가 하 여는 `<providerOption>` .NET Framework 2.0 Machine.config 또는 루트 Web.config 파일에는 요소입니다. 3.5 합니다 Machine.config 파일의 기본 컴파일러 버전을 업데이트 하는 경우 변경할 수 있습니다 2.0 응용 프로그램 기준으로 사용 하 여는 `<providerOption>` 응용 프로그램 구성 파일의 요소입니다.  
  
 CodeDOM 코드 공급자 구현자는 생성자를 제공 하 여 사용자 지정 옵션을 처리할 수는 `providerOptions` 형식의 매개 변수 <xref:System.Collections.Generic.IDictionary%602>합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 C# 코드 공급자의 버전 3.5를 사용할지를 지정 하는 방법에 설명 합니다.  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler  
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,   
          Version=2.0.3600.0, Culture=neutral,   
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions="/optimize"  
        warningLevel="1" >  
          <providerOption  
            name="CompilerVersion"  
            value="v3.5" />  
      </compiler>  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a>참고자료

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [구성 파일 스키마](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [\<컴파일러 > 요소](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)
- [정규화된 형식 이름 지정](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)
- [컴파일 (ASP.NET 설정 스키마)에 대 한 컴파일러에 대 한 compiler 요소](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/a15ebt6c(v=vs.100))
