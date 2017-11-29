---
title: "엔터티 이해 | Microsoft Docs"
description: "엔터티, 필드, 관계 및 데이터베이스를 소개합니다."
services: powerapps
documentationcenter: na
author: clwesene
manager: kfend
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/24/2017
ms.author: kfend
ms.openlocfilehash: 9078daccfd3d72ab5cbf3b26a67ffc2a27af1332
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2017
---
# <a name="understand-entities-in-the-common-data-service"></a>Common Data Service의 엔터티 이해
[!VIDEO nb:cid:UUID:beec68e8-1541-41fb-8fc6-28714ccaca68]


Common Data Service를 통해 표준 및 사용자 지정 엔터티 집합 내에서 데이터를 안전하게 저장하고 관리할 수 있습니다. 엔터티는 데이터베이스 내의 테이블과 유사한 데이터를 저장하는 데 사용되는 필드의 집합입니다. 데이터가 저장된 후 데이터를 사용하여 다양한 응용 프로그램을 빌드하는 데 Microsoft PowerApps를 사용할 수 있습니다.

* 표준 또는 사용자 지정 엔터티로 데이터를 가져옵니다.
* 시나리오 및 응용 프로그램을 지원하도록 사용자 지정 엔터티를 만듭니다.
* 추가 정보가 필요한 표준 엔터티에 사용자 지정 필드를 추가합니다.
* 개발 중인 하나의 앱에 표준 및 사용자 지정 엔터티를 다른 원본의 데이터처럼 쉽게 통합합니다.
* 생산성 추가 기능을 활용하여 Microsoft Excel 및 Outlook에서 데이터에 액세스합니다.
* 표준 및 사용자 지정 엔터티에 대해 역할 기반 보안을 사용하여 조직 내에서 데이터를 보호합니다.
* 국가, 인사말 또는 통화와 같은 미리 정의된 데이터의 선택 목록을 포함합니다.
* 엔터티 및 필드 이름의 번역을 활용하여 데이터 및 응용 프로그램에 대한 세계화된 지원 기능을 제공합니다.

각 엔터티에는 사용자가 만들고 읽고 업데이트하고 삭제할 수 있는 레코드 집합이 포함되어 있습니다. 다른 엔터티의 레코드를 기반으로 하나의 엔터티에 대한 정보를 볼 수 있도록 엔터티 간의 관계를 만들 수 있습니다. 예를 들어, 고객이 참석한 이벤트를 추적하는 사용자 지정 엔터티를 만들 수 있습니다. 사용자 지정 엔터티에 조회 필드로 고객을 추가하여 앱 및 보고에서 활용할 수 있는 두 엔터티 간의 관계를 설정합니다.

Common Data Service 사용을 위한 계획 구매에 대한 자세한 내용은 [가격 책정 정보](pricing-billing-skus.md)를 참조하세요.

## <a name="why-use-entities"></a>엔터티를 사용하는 이유는 무엇인가요?
Common Data Service 내에서 두 표준 및 사용자 지정 엔터티는 데이터를 위한 안전한 클라우드 기반 저장소 옵션을 허용합니다. 엔터티를 통해 앱 내에서 사용할 데이터의 비즈니스 중심 정의를 만들 수 있습니다. 엔터티를 사용하는 것이 가장 적합한 방법인지 확신이 들지 않는다면 이러한 이점을 고려해보세요.

* **손쉬운 관리** - 메타데이터와 데이터는 모두 클라우드에 저장됩니다. 저장 방법에 대한 자세한 내용은 신경쓰지 않아도 됩니다.
* **손쉬운 공유** - PowerApps에서 권한을 관리하기 때문에 동료와도 데이터를 쉽게 공유할 수 있습니다.
* **손쉬운 보안** - 사용자가 액세스 권한을 부여받은 경우에만 볼 수 있도록 데이터가 안전하게 저장됩니다. 역할 기반 보안을 통해 조직 내에서 여러 사용자의 엔터티에 대한 액세스를 제어할 수 있습니다.
* **풍부한 메타데이터** - PowerApps에서 데이터 형식과 관계를 직접 활용합니다. 예를 들어 필드 형식 URL을 정의하면 데이터가 앱 내에서 하이퍼링크로 표시됩니다.
* **생산성 도구** - Microsoft Excel 및 Outlook용 추가 기능에서 엔터티를 사용하여 생산성을 높이고 데이터에 액세스할 수 있도록 합니다.
* **선택 목록** - 다양한 표준 선택 목록 집합에서 선택 목록을 포함하여 엔터티와 앱 내에서 드롭다운을 빠르게 제공합니다.

## <a name="standard-and-custom-entities"></a>표준 및 사용자 지정 엔터티
앱 개발 시 표준 엔터티, 사용자 지정 엔터티, 또는 두 가지 모두를 사용할 수 있습니다. 앱에서 특정 목적을 제공할 수 있는 표준 엔터티인 경우 동일한 작업을 수행하는 사용자 지정 엔터티를 개발하는 것보다 그냥 사용하는 것이 더 좋습니다. 해당 목적에서 일부만 변경된 표준 엔터티의 경우 필요에 맞게 필드를 추가할 수 있습니다. 

* Common Data Service는 기본적으로 표준 엔터티를 제공합니다. 모범 사례에 따라 연락처, 계정, 제품 등 조직에 대한 가장 일반적인 개념을 파악할 수 있도록 설계되었습니다. 엔터티의 전체 목록은 [표준 엔터티](data-platform-intro.md#standard-entities)를 참조하세요.
* 고유한 정보를 조직에 저장하기 위해 하나 이상의 사용자 지정 엔터티를 만들어 표준 엔터티의 기능을 확장할 수 있습니다. 자세한 내용은 [사용자 지정 엔터티를 만드는 방법](data-platform-create-entity.md)을 참조하세요.

> **참고:** 가능하면 표준 엔터티를 사용합니다(필요한 경우 사용자 지정 필드를 추가하여). 이렇게 하면 나중에 이러한 엔터티를 활용하는 새로운 기능 또는 앱에서 혜택을 받을 수 있습니다.
> 
> 

## <a name="fields"></a>필드
각 필드에는 이름, 표시 이름, 데이터 형식 및 몇 가지 간단한 유효성 검사가 포함되어 있습니다. 데이터 형식은 예를 들어, **텍스트**, **날짜** 또는 **숫자**를 포함합니다. 유효성 검사를 통해 해당 엔터티에 필요할 경우, 필수 필드에 데이터가 있는지와 레코드가 고유한지 등을 확인할 수 있습니다. 모든 필드는 3가지 범주인 시스템 필드, 표준 필드, 사용자 지정 필드 중에서 하나로 분류됩니다.

### <a name="system-fields"></a>시스템 필드
모든 엔터티는 표준이든 사용자 지정이든 변경하거나, 삭제하거나, 값으로 설정할 수 없는 읽기 전용 필드의 집합으로 생성됩니다. 자세한 내용은 [시스템 및 레코드 제목 필드](data-platform-create-entity.md#system-and-record-title-fields)를 참조하세요. 다음은 가장 중요한 시스템 필드입니다.

* **Created Record Date** - 레코드를 생성한 날짜와 시간입니다.
* **Created By** - 레코드를 만든 사용자입니다.
* **Modified Record Date** - 레코드를 수정한 최근 날짜와 시간입니다.
* **Last Modified By** - 가장 최근에 레코드를 수정한 사용자입니다.

### <a name="standard-fields"></a>표준 필드
각 표준 엔터티에는 변경 또는 삭제할 수 없는 기본 필드 집합이 포함되어 있습니다. 엔터티 및 해당 필드의 목록, 선택 목록의 목록은 [표준 엔터티](https://docs.microsoft.com/common-data-service/entity-reference/standard-entities)를 참조하세요.

### <a name="custom-fields"></a>사용자 지정 필드
표준 엔터티나 사용자 지정 엔터티 중 하나에서 사용자 지정 필드를 만들 수 있습니다. 이름, 표시 이름 및 각 사용자 지정 필드의 데이터 형식을 지정해야 합니다. 지원되는 형식의 전체 목록은 [엔터티 필드 데이터 형식](https://docs.microsoft.com/en-us/common-data-service/entity-reference/field-data-types)을 참조하세요.

## <a name="lookup-relationships"></a>관계 조회
**조회** 데이터 형식의 필드로 정의된 관계가 존재하면 엔터티 내에서 레코드 간 이동이 가능합니다. 조회 관계를 만들려면 하나의 엔터티 내에서 **조회** 데이터 형식의 필드를 추가하고, 정보를 조회하려는 엔터티를 지정합니다. 자세한 내용은 [조회 필드를 통한 엔터티 관계](data-platform-entity-lookup.md)를 참조하세요.

## <a name="standard-entities"></a>표준 엔터티
엔터티 및 해당 필드의 목록, 열거형의 목록은 [표준 엔터티](https://docs.microsoft.com/common-data-service/entity-reference/standard-entities)를 참조하세요.

| 기능 그룹 | 설명 |
| --- | --- |
| 고객 서비스 |고객 서비스 엔터티는 추적, 에스컬레이션 및 문서화를 포함하여 고객의 문제를 관리합니다. |
| 기본 사항 |기본 사항 엔터티는 거의 모든 다른 엔터티 그룹과 관련된 정보를 포함합니다. 이 그룹은 주소, 통화와 같은 엔터티를 포함합니다. |
| 사용자, 조직 및 그룹 |이러한 엔터티에는 직원, 계약자, 기부자, 지원자, 팬, 동문, 가족 등을 포함해 상호 교류가 가능한 다양한 사용자와 조직으로 구성되어 있습니다. |
| 구매 |구매 엔터티로 구매 솔루션을 만들 수 있습니다. |
| 영업 |영업 엔터티를 사용하면 잠재 고객과 기회에 대한 추적에서부터 연락처를 이용한 작업 수행, 주문 접수 및 전달, 송장 발송에 이르는 종단 간 판매 솔루션을 만들 수 있습니다. |

## <a name="get-started"></a>시작
표준 엔터티를 사용하여 앱을 만들어 시도해 보거나 [사용자 지정 엔터티를 만든](data-platform-create-entity.md) 다음 [해당 엔터티를 사용하는 앱을 만듭니다](data-platform-create-app.md).

<!--TODO - Add Link for Standard entity app - Template? -->

## <a name="privacy-notice"></a>개인 정보 취급 방침
Microsoft PowerApps 공통 데이터 모델을 통해 사용자 지정 엔터티 및 필드 이름을 진단 시스템에 수집 및 저장합니다.  이 정보는 고객을 위한 공통 데이터 모델을 향상하기 위해 사용합니다. 작성자가 만드는 엔터티 및 필드 이름은 Microsoft PowerApps 커뮤니티에서 공통된 시나리오를 이해하고 조직에 관련된 스키마와 같은 서비스의 표준 엔터티 범위의 격차를 확인하는 데 도움을 줍니다. 이러한 엔터티와 연결된 데이터베이스 테이블의 데이터는 Microsoft에 의해 액세스되거나 사용되지 않고 데이터베이스가 프로비전되는 영역 외부에서 복제되지 않습니다. 단, 사용자 지정 엔터티 및 필드 이름은 지역에 걸쳐 복제될 수 있고 데이터 보존 정책에 따라 삭제될 수 있습니다. Microsoft는 [보안 센터](https://www.microsoft.com/trustcenter/Privacy/default.aspx)에서 더 자세히 설명한 것과 같이 개인 정보 보호를 위해 노력합니다.
