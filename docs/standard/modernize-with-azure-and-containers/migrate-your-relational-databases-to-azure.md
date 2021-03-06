---
title: 관계형 데이터베이스를 azure로 마이그레이션
description: Azure 클라우드와 Windows 컨테이너를 사용하여 기존 .NET 응용 프로그램 최신화 | 관계형 데이터베이스를 azure로 마이그레이션
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 600c47b6b0ccaf704c8e7b638c759e990acaaacf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61812785"
---
# <a name="migrate-your-relational-databases-to-azure"></a>관계형 데이터베이스를 azure로 마이그레이션

Vision: Azure는 가장 포괄적인 데이터베이스 마이그레이션은 제공합니다.

Azure에서 IaaS VM(순수한 리프트 앤 시프트)에 직접 데이터베이스 서버를 마이그레이션하거나, 추가적인 이득을 얻기 위해 Azure SQL Database로 마이그레이션할 수 있습니다. Azure SQL Database에서는 관리되는 인스턴스와 서비스 형태의 전체 데이터베이스(DBaaS) 옵션을 제공합니다. 그림 3-1에서는 Azure에서 사용할 수 있는 다양한 관계형 데이터베이스 마이그레이션 경로를 보여 줍니다.

![Azure에서 데이터베이스 마이그레이션 경로](./media/image3-1.png)

> **그림 3-1.** Azure에서 데이터베이스 마이그레이션 경로

## <a name="when-to-migrate-to-azure-sql-database-managed-instance"></a>Azure SQL Database Managed Instance로 마이그레이션할 시기

대부분의 경우 Azure로 데이터를 마이그레이션할 때 Azure SQL Database Managed Instance는 생각할 수 있는 가장 좋은 선택입니다. SQL Server 데이터베이스를 마이그레이션할 때 응용 프로그램을 다시 작성하거나 데이터 또는 데이터에 액세스하는 코드를 거의 변경하지 않아도 된다는 것을 100% 보장해야 하는 경우 Azure SQL Database의 Managed Instance 기능을 선택하십시오.

Azure SQL Database Managed Instance는 표준 Azure SQL 데이터베이스(단일 데이터베이스 모델)에서 제공되는 기능을 넘어선 격리 요구 사항이나 SQL Server 인스턴스 수준의 기능에 대한 추가적인 요구 사항이 있는 경우 최상의 옵션입니다. 마지막은 PaaS 중심의 선택이지만 기존 SQL 서버와 동일한 기능을 제공하지는 않습니다. 마이그레이션은 마찰을 일으킬 수 있습니다.

예를 들어, SQL Server 기능 인스턴스 수준에서에서 심층 투자에 조직에서 SQL Managed Instance로 마이그레이션 도움이 되는 경우 인스턴스 수준 SQL Server 기능의 예제는 SQL 공용 언어 런타임 (CLR) 통합, SQL Server 에이전트 및 데이터베이스 간 쿼리 있습니다. 이러한 기능에 대 한 지원이 표준 Azure SQL Database (단일 데이터베이스 모델)에서 사용할 수 없는 경우

규제가 엄격한 산업에서 운영되고 보안 목적으로 격리를 유지해야하는 조직은 SQL Managed Instance 모델을 선택하면 도움이 될 수 있습니다.

Azure SQL Database에서 관리되는 인스턴스는 다음과 같은 특징이 있습니다.

- Azure Virtual Network를 통한 보안 격리

- 응용 프로그램 노출 호환성, 이러한 기능을 사용 하 여:

  - SQL Server 에이전트 및 SQL Server Profiler

  - 데이터베이스 간 참조 및 쿼리를 SQL CLR, 복제, 변경 데이터 캡처 (CDC) 및 Service Broker

- 데이터베이스 크기 최대 35TB

- 이러한 기능을 사용 하 여 최소 가동 중지 시간 마이그레이션:

  - Azure Database Migration Service

  - 기본 백업 및 복원, 로그 전달

이러한 기능을 사용 하 여 Azure SQL Database에 기존 응용 프로그램 데이터베이스를 마이그레이션하는 경우 관리 되는 인스턴스 모델 제공 PaaS의 이점 중 거의 100% SQL Server에 대 한 합니다. 관리 되는 인스턴스는 인스턴스 수준 기능을 사용 하 여 응용 프로그램 디자인을 변경 하지 않고 계속 하면 SQL Server 환경입니다.

관리 되는 인스턴스는 현재 SQL Server를 사용 중인 및 클라우드에서 네트워크 보안에 유연성이 필요한는 기업에 가장 적합 한 것입니다. SQL database에 대 한 개인 가상 네트워크를 것과 같습니다.

## <a name="when-to-migrate-to-azure-sql-database"></a>Azure SQL Database로 마이그레이션할 시기

언급 했 듯이 표준 Azure SQL Database는 완전히 관리 되는 관계형 DBaaS 합니다. SQL Database는 현재 전 세계 38 데이터 센터에서 수백만 개의 프로덕션 데이터베이스를 관리합니다. 광범위 한 응용 프로그램 및 글로벌 규모로 고급 데이터 처리를 필요로 하는 데이터를 가장 많이 사용 하는 중요 업무용 응용 프로그램을 이끌어내기 위해 간단한 트랜잭션 데이터 관리에서 워크 로드를 지원 합니다.

해당 전체 PaaS 기능으로 인해 보다 나은 가격-궁극적으로 비용을 절감 하 고-있다면 응용 프로그램을 사용 하 여 기본, 표준 SQL database 인스턴스 추가 기능이 없습니다 "기본적으로 선택한"으로 표준 Azure SQL Database로 이동 해야 합니다. 표준 Azure SQL Database에서 SQL CLR 통합, SQL Server 에이전트 및 데이터베이스 간 쿼리와 같은 SQL Server 기능을 사용할 수 없습니다. 이러한 기능은 Azure SQL Database Managed Instance 모델 에서만 사용할 수 있습니다.

Azure SQL Database는 앱 개발자를 위한 기본 제공 되는 지능형 클라우드 데이터베이스 서비스입니다. 즉석에서 다중 테 넌 트 앱을 효율적으로 제공 하는 데 가동 중지 시간 없이 크기가 조정 되는 유일한 클라우드 데이터베이스 서비스 이기도 합니다. 궁극적으로 Azure SQL Database를 혁신 하는 데 더 오래 유지 및 출시 시간 가속화 합니다. 보안 앱을 빌드하고 원하는 플랫폼과 언어를 사용 하 여 SQL database에 연결할 수 있습니다.

Azure SQL Database는 다음과 같은 이점을 제공합니다.

- 학습 및 적응 응용 프로그램에 기본 제공 인텔리전스 (기계 학습)

- 요청 시 데이터베이스 프로 비전

- 모든 워크 로드에 대 한 제품의 범위

- 99.99% 가용성 SLA, 0 개 유지 관리

- 데이터 보호에 대 한 지역에서 복제 및 복원 서비스

- Azure SQL Database 지정 시간 복원 기능

- SQL Server 2016에서는 하이브리드 및 마이그레이션을 비롯 한 호환성

표준 Azure SQL Database 보다 더 가까운 PaaS로 Azure SQL Database Managed Instance. 관리 되는 클라우드에서 많은 혜택을 얻게 되므로 표준 Azure SQL Database를 선호 합니다. 그러나 Azure SQL Database 일반에서 몇 가지 주요 차이점이 있으며 온-프레미스 SQL Server 인스턴스. 기존 응용 프로그램의 데이터베이스 요구 사항 및 enterprise 요구 사항 및 정책에 따라 아닐 최상의 클라우드로 마이그레이션을 계획할 때.

## <a name="when-to-move-your-original-rdbms-to-a-vm-iaas"></a>원래 RDBMS에 VM (IaaS)으로 이동 하는 경우

마이그레이션 옵션 중 하나에 원래 관계형 데이터베이스 관리 시스템 (RDBMS), Oracle, IBM DB2, MySQL, PostgreSQL 또는 SQL Server를 포함 하 여 Azure VM에서 실행 되는 유사한 서버로 이동 하는 것입니다. 최소한의 변경 내용 또는 변경 없이 클라우드에서 가장 빠른 마이그레이션에 필요한 기존 응용 프로그램에 있는 경우 IaaS 클라우드에서로 직접 마이그레이션하는 공정 옵션을 수 있습니다. 가장 좋은 방법은 클라우드의 모든 이점을 활용 되지 않을 수 있습니다 하지만 가장 빠른 초기 경로 것입니다.

현재까지 Microsoft Azure 지원 [331 다른 데이터베이스 서버](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/databases?page=1&subcategories=databases-all) IaaS Vm으로 배포 합니다. 여기에 SQL Server, Oracle, MySQL, PostgreSQL 및 IBM DB2와 같은 인기 있는 RDBMS MongoDB, Cassandra, DataStax, MariaDB, 및 Cloudera와 같은 다른 많은 NoSQL 데이터베이스 포함 됩니다.

> [!NOTE]
> 이동 되지만 Azure VM에 사용자 RDBMS (이기 때문에 IaaS) 데이터를 클라우드로 마이그레이션에 대 한 가장 빠른 방법은 있을 수 있으며,이 방법을 사용 하려면 (데이터베이스 관리자와 IT 전문가) IT 팀에 많은 투자를 해야 합니다. 엔터프라이즈 팀 설정 하 고 고가용성, 재해 복구 및 SQL Server에 대 한 패치를 관리 해야 합니다. 이 컨텍스트는 또한 모든 관리 권한이 있는 사용자 지정된 된 환경이 필요합니다.

## <a name="when-to-migrate-to-sql-server-as-a-vm-iaas"></a>VM (IaaS)으로 SQL Server로 마이그레이션할 시기

몇 가지 계속 해야 하는 경우 일반 VM과 SQL Server로 마이그레이션에 있을 수 있습니다. 예제 시나리오는 SQL Server Reporting Services를 사용 해야 하는 경우. 대부분의 경우에서 하지만 Azure SQL Database Managed Instance 제공할 수 있도록 SQL Server VM에 대 한 마이그레이션 시도 하 여 마지막 수단으로 사용 해야 합니다. 온-프레미스 SQL server에서 마이그레이션하는 데 필요한 모든 것.

## <a name="use-azure-database-migration-service-to-migrate-your-relational-databases-to-azure"></a>Azure Database Migration Service를 사용 하 여 Azure에 관계형 데이터베이스를 마이그레이션하려면 

Azure SQL Database, Azure SQL Database 관리 되는 인스턴스 또는 Azure VM에서 SQL Server 대상 데이터베이스 인지를 Azure로 SQL Server, Oracle 및 MySQL 등의 관계형 데이터베이스를 마이그레이션하려면 Azure Database Migration Service를 사용할 수 있습니다.

평가 보고를 사용 하면 자동화 된 워크플로 데이터베이스를 마이그레이션할 수 있도록 원하는 변경 작업을 안내 합니다. 준비가 될 때 서비스에서 Azure로 원본 데이터베이스를 마이그레이션합니다.

원래 RDBMS를 변경할 때마다 다시 테스트 해야 합니다. SQL 문장이 나 테스트 결과 따라 응용 프로그램에서 개체-관계형 매핑 (ORM) 코드를 변경 해야 할 수 있습니다.

다른 데이터베이스 (예를 들어, IBM DB2) 있고 리프트 앤 시프트 방식을 선택할 경우 하려는 해당 데이터베이스를 사용 하 여 Azure에서 IaaS Vm으로 계속 더 복잡 한 데이터 마이그레이션을 수행 하려면 원치 않는 경우. 새 스키마 및 다른 프로그래밍 라이브러리를 사용 하 여 다른 데이터베이스 형식으로 마이그레이션하는 경우 때문에 더 복잡 한 데이터 마이그레이션을 노력을 해야 합니다.

Azure Database Migration Service를 사용 하 여 데이터베이스를 마이그레이션하는 방법에 알아보려면 참조 [Azure SQL Database 관리 되는 인스턴스 및 Azure Database Migration Service를 사용 하 여 더 빠르게 클라우드에](https://channel9.msdn.com/Events/Build/2017/P4008)합니다.

## <a name="additional-resources"></a>추가 자료

- **클라우드 SQL Server 옵션 선택: Azure SQL Database (PaaS) 또는 Azure VM (IaaS)에서 SQL Server**

    <https://docs.microsoft.com/azure/sql-database/sql-database-paas-vs-sql-server-iaas>

- **Azure SQL DB 관리 되는 인스턴스 및 Database Migration Service를 사용 하 여 더 빠르게 클라우드로 가져오기**

    <https://channel9.msdn.com/Events/Build/2017/P4008>

- **클라우드에서 SQL Database로 SQL Server 데이터베이스 마이그레이션**

    <https://docs.microsoft.com/azure/sql-database/sql-database-cloud-migrate>

- **Azure SQL Database**

    <https://azure.microsoft.com/services/sql-database/?v=16.50>

- **Virtual machines의 SQL Server**

    <https://azure.microsoft.com/services/virtual-machines/sql-server/>

> [!div class="step-by-step"]
> [이전](lift-and-shift-existing-apps-azure-iaas.md)
> [다음](modernize-existing-apps-to-cloud-optimized/index.md)
