---
title: WPF 애플리케이션 배포(WPF)
ms.date: 03/30/2017
helpviewer_keywords:
- WPF applications [WPF], deployment
- deployment [WPF], applications
ms.assetid: 12cadca0-b32c-4064-9a56-e6a306dcc76d
ms.openlocfilehash: 0ffd4fb05a5a409d74f8a9401a5fb021db0cd99b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59320654"
---
# <a name="deploying-a-wpf-application-wpf"></a>WPF 애플리케이션 배포(WPF)
Windows Presentation Foundation (WPF) 응용 프로그램을 빌드한 후 배포 해야 합니다. [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] 및.NET Framework에는 여러 가지 배포 기술을 포함 합니다. [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램을 배포하는 데 사용되는 배포 기술은 응용 프로그램 종류에 따라 달라집니다. 이 항목에서는 각 배포 기술과 해당 기술이 각 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 애플리케이션 종류의 배포 요구 사항과 함께 사용되는 방법에 대해 간략하게 설명합니다.  

<a name="Deployment_Technologies"></a>   
## <a name="deployment-technologies"></a>배포 기술  
 [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] 및.NET Framework를 비롯 한 여러 가지 배포 기술을 다음과 같습니다.  
  
-   XCopy 배포.  
  
-   [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] 배포.  
  
-   [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] 배포.  
  
<a name="XCopy_Deployment"></a>   
### <a name="xcopy-deployment"></a>XCopy 배포  
 XCopy 배포는 XCopy 명령줄 프로그램을 사용하여 한 위치에서 다른 위치로 파일을 복사하는 방법을 나타냅니다. XCopy 배포는 다음과 같은 경우에 적합합니다.  
  
-   애플리케이션이 독립적이며, 실행하기 위해 클라이언트를 업데이트할 필요가 없습니다.  
  
-   빌드 위치(로컬 디스크, [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)] 파일 공유 등)에서 게시 위치(웹 사이트, [!INCLUDE[TLA2#tla_unc](../../../../includes/tla2sharptla-unc-md.md)] 파일 공유 등)로 이동하는 경우처럼 한 위치에서 다른 위치로 애플리케이션 파일을 이동해야 합니다.  
  
-   애플리케이션에 셸 통합(시작 메뉴 바로 가기, 데스크톱 아이콘 등)이 필요하지 않습니다.  
  
 XCopy는 간단한 배포 시나리오에 적합하지만 좀더 복잡한 배포 기능이 필요한 경우 제한됩니다. 특히 XCopy를 사용하면 강력한 방식으로 배포를 관리하기 위한 스크립트를 작성, 실행 및 유지 관리하는 오버헤드가 자주 발생합니다. 또한 XCopy는 버전 관리, 제거 또는 롤백을 지원하지 않습니다.  
  
<a name="Windows_Installer"></a>   
### <a name="windows-installer"></a>Windows Installer  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하면 클라이언트에 쉽게 배포하고 실행할 수 있는 자체 포함 실행 파일로 응용 프로그램을 패키지할 수 있습니다. 또한 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]는 [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)]와 함께 설치되며 데스크톱, 시작 메뉴 및 프로그램 제어판과의 통합을 가능하게 합니다.  
  
 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]에서는 응용 프로그램의 설치 및 제거가 간단하지만 설치된 응용 프로그램이 버전 관리 관점에서 최신 버전으로 유지되도록 보장하는 기능은 제공하지 않습니다.  
  
 Windows Installer에 대 한 자세한 내용은 참조 하세요. [Windows Installer 배포](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-desktop)합니다.
  
<a name="ClickOnce_Deployment"></a>   
### <a name="clickonce-deployment"></a>ClickOnce 배포  
 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]에서는 비 웹 응용 프로그램에 대해 웹 스타일 응용 프로그램 배포를 사용할 수 있습니다. 애플리케이션이 웹 또는 파일 서버에서 게시되고 배포됩니다. [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)] 설치 응용 프로그램처럼 전체 범위의 클라이언트 기능을 지원하지는 않지만 다음을 포함하는 하위 기능은 지원합니다.  
  
-   시작 메뉴 및 프로그램 제어판과의 통합.  
  
-   버전 관리, 롤백 및 제거.  
  
-   항상 배포 위치에서 애플리케이션을 시작하는 온라인 설치 모드.  
  
-   새 버전이 릴리스되는 경우 자동 업데이트.  
  
-   파일 확장명 등록.  
  
 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]에 대한 자세한 내용은 [ClickOnce 보안 및 배포](/visualstudio/deployment/clickonce-security-and-deployment)를 참조하세요.  
  
<a name="Deploying_WPF_Applications"></a>   
## <a name="deploying-wpf-applications"></a>WPF 애플리케이션 배포  
 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램에 대한 배포 옵션은 응용 프로그램 종류에 따라 달라집니다. 배포 측면에서 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)]는 세 가지 중요한 애플리케이션 종류를 제공합니다.  
  
-   독립 실행형 애플리케이션.  
  
-   마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 애플리케이션.  
  
-   [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)].  
  
<a name="Deploying_Standalone_Applications"></a>   
### <a name="deploying-standalone-applications"></a>독립 실행형 애플리케이션 배포  
 독립 실행형 애플리케이션은 [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)] 또는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 배포됩니다. 두 방법 모두 독립 실행형 애플리케이션을 실행하려면 완전 신뢰가 필요합니다. 완전 신뢰는 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 배포되는 독립 실행형 애플리케이션에 자동으로 부여됩니다. [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]를 사용하여 배포되는 독립 실행형 응용 프로그램에는 완전 신뢰가 자동으로 부여되지 않습니다. 대신 [!INCLUDE[TLA2#tla_clickonce](../../../../includes/tla2sharptla-clickonce-md.md)]는 사용자가 동의해야 독립 실행형 애플리케이션이 설치되는 보안 경고 대화 상자를 표시합니다. 동의하면 독립 실행형 애플리케이션이 설치되고 완전 신뢰가 부여됩니다. 동의하지 않으면 독립 실행형 애플리케이션이 설치되지 않습니다.  
  
<a name="Deploying_Markup_Only_XAML_Applications"></a>   
### <a name="deploying-markup-only-xaml-applications"></a>마크업 전용 XAML 애플리케이션 배포  
 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 일반적으로 [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)] 페이지 같은 웹 서버에 게시되며 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)]를 사용하여 볼 수 있습니다. 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 인터넷 영역 권한 설정에 정의된 제한 사항이 있는 부분 신뢰 보안 샌드박스 내에서 실행됩니다. 또한 [!INCLUDE[TLA2#tla_html](../../../../includes/tla2sharptla-html-md.md)] 기반 웹 애플리케이션과 동일한 보안 샌드박스를 제공합니다.  
  
 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 애플리케이션의 보안에 대한 자세한 내용은 [보안](../security-wpf.md)을 참조하세요.  
  
 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지는 XCopy나 [!INCLUDE[TLA2#tla_wininstall](../../../../includes/tla2sharptla-wininstall-md.md)]를 사용하여 로컬 파일 시스템에 설치할 수 있습니다. 이러한 페이지를 사용 하 여 볼 수 있습니다 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)] 또는 Windows 탐색기입니다.  
  
 XAML에 대한 자세한 내용은 [XAML 개요(WPF)](../advanced/xaml-overview-wpf.md)를 참조하세요.  
  
<a name="Deploying_XAML_Browser_Applications"></a>   
### <a name="deploying-xaml-browser-applications"></a>XAML 브라우저 애플리케이션 배포  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 배포하려면 다음과 같은 파일 세 개가 필요한 컴파일된 응용 프로그램입니다.  
  
-   *ApplicationName*.exe: 실행 가능한 어셈블리 응용 프로그램 파일입니다.  
  
-   *ApplicationName*.xbap: 배포 매니페스트 합니다.  
  
-   *ApplicationName*.exe.manifest: 애플리케이션 매니페스트입니다.  
  
> [!NOTE]
>  배포 및 애플리케이션 매니페스트에 대한 자세한 내용은 [WPF 애플리케이션 만들기](building-a-wpf-application-wpf.md)를 참조하세요.  
  
 이러한 파일은 [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)]가 빌드될 때 생성됩니다. 자세한 내용은 [방법: 새 WPF 브라우저 응용 프로그램 프로젝트 만들기](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb628663(v=vs.100))합니다. 마크업 전용 [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] 페이지처럼 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 일반적으로 웹 서버에 게시되며 [!INCLUDE[TLA2#tla_iegeneric](../../../../includes/tla2sharptla-iegeneric-md.md)]를 사용하여 볼 수 있습니다.  
  
 [!INCLUDE[TLA2#tla_xbap#plural](../../../../includes/tla2sharptla-xbapsharpplural-md.md)]는 배포 기술 중 하나를 사용하여 클라이언트에 배포할 수 있습니다. 그러나 다음과 같은 기능을 제공하는 [!INCLUDE[TLA#tla_clickonce](../../../../includes/tlasharptla-clickonce-md.md)]가 권장됩니다.  
  
1. 새 버전이 게시될 때 자동 업데이트.  
  
2. 완전 신뢰로 실행되는 [!INCLUDE[TLA2#tla_xbap](../../../../includes/tla2sharptla-xbap-md.md)]에 대한 권한 상승.  
  
 기본적으로 ClickOnce는 .deploy 확장명을 사용하여 애플리케이션 파일을 게시합니다. 그러면 문제가 될 수 있지만 사용하지 않도록 설정할 수 있습니다. 자세한 내용은 [ClickOnce 배포 시 서버 및 클라이언트 구성 문제](/visualstudio/deployment/server-and-client-configuration-issues-in-clickonce-deployments)를 참조하세요.  
  
 [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] 배포에 대한 자세한 내용은 [WPF XAML 브라우저 애플리케이션 개요](wpf-xaml-browser-applications-overview.md)를 참조하세요.  
  
<a name="Installing__NET_Framework_3_0"></a>   
## <a name="installing-the-net-framework"></a>.NET Framework 설치  
 실행 하는 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 응용 프로그램을 클라이언트에서 Microsoft.NET Framework를 설치 합니다. [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] .NET Framework를 사용 하 여 클라이언트가 설치 되어 있는지 여부를 자동으로 검색 하면 [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] 브라우저에서 호스팅되는 응용 프로그램이 표시 됩니다. .NET Framework 설치 되어 있지 않으면 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] 사용자 설치 하 라는 메시지가 표시 됩니다.  
  
 .NET Framework 설치 되어 있는지를 검색할 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] 는 대체 (fallback)로 등록 된 부트스트래퍼 응용 프로그램이 [!INCLUDE[TLA#tla_mime](../../../../includes/tlasharptla-mime-md.md)] 확장명이 포함 된 콘텐츠 파일에 대 한 처리기:.xaml,.xps,.xbap 및.application입니다. 이러한 파일 형식으로 이동 하 고.NET Framework 클라이언트에 설치 되어 있지는 부트스트래퍼 응용 프로그램 설치 권한을 요청 합니다. 사용 권한을 제공 하지 않으면.NET Framework도 아니고 응용 프로그램이 설치 됩니다.  
  
 권한이 부여 되 면 [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] 다운로드 하 고 사용 하 여.NET Framework 설치는 [!INCLUDE[TLA#tla_bits](../../../../includes/tlasharptla-bits-md.md)]합니다. .NET Framework를 설치 하 고 나면 처음에 요청한 파일이 새 브라우저 창에서 열립니다.  
  
 .NET framework 자동 검색은에서 사용할 수 있습니다 [!INCLUDE[TLA#tla_longhorn](../../../../includes/tlasharptla-longhorn-md.md)], [!INCLUDE[TLA#tla_winxpsp2](../../../../includes/tlasharptla-winxpsp2-md.md)], 및 [!INCLUDE[TLA#tla_winnetsvrfamsp1](../../../../includes/tlasharptla-winnetsvrfamsp1-md.md)] 포함 하는 클라이언트 [!INCLUDE[TLA2#tla_ie7](../../../../includes/tla2sharptla-ie7-md.md)] 이상이 설치 되어 있습니다.  
  
 자세한 내용은 [.NET Framework 및 애플리케이션 배포](../../deployment/index.md)를 참조하세요.  
  
## <a name="see-also"></a>참고자료

- [WPF 응용 프로그램 빌드](building-a-wpf-application-wpf.md)
- [보안](../security-wpf.md)
