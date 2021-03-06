---
title: 앱 공유 | Microsoft Docs
description: 다른 사용자에게 앱 실행 또는 수정 권한을 부여하여 앱 공유
services: ''
suite: powerapps
documentationcenter: na
author: AFTOwen
manager: kfile
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/18/2018
ms.author: anneta
ms.openlocfilehash: 22950d866ed8e61dd0824701ef8af86f5bed2dc6
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="share-an-app-in-powerapps"></a>PowerApps에서 앱 공유
자신의 비즈니스 요구 사항을 해결하는 앱을 빌드하는 것이 좋지만 PowerApps의 진정한 마법은 해당 앱을 다른 사람들과 공유하는 데 있습니다. 이 토픽에서는 특정 사용자 또는 보안 그룹과 앱을 공유하는 방법을 알아보거나 전체 조직과 공유할 수 있습니다.

## <a name="specify-an-app"></a>앱 지정
1. PowerApps에 로그인한 다음, 왼쪽 가장자리 부근의 **앱**을 클릭하거나 누릅니다.

    ![앱 목록 표시](./media/share-app/file-apps.png)

1. 공유하려는 앱에 대한 줄임표(...)를 클릭하거나 누른 다음, **공유**를 클릭하거나 누릅니다.

    ![공유 화면 열기](./media/share-app/ellipsis-share.png)

## <a name="share-an-app"></a>앱 공유
1. Azure Active Directory에서 어떤 사용자 또는 보안 그룹과 앱을 공유할지와 해당 사용자에게 알림 메일을 보낼지 여부를 지정합니다.

    전체 조직과 앱을 공유하여 앱을 실행하도록 할 수도 있지만 이 경우 수정하거나 공유할 수는 없습니다.

    ![사용자 지정](./media/share-app/share-list.png)

1. 사용 권한 수준을 지정한 후 **저장**을 클릭하거나 탭합니다.

    * **사용 가능**: 사용자 또는 그룹이 앱을 실행할 수 있지만 공유할 수는 없습니다.
    * **편집 가능**: 사용자 또는 그룹은 앱을 실행하고, 사용자 지정하고, 사용자 지정된 버전을 다른 사용자와 또 공유할 수 있습니다.

        ![사용 권한 지정](./media/share-app/edit-use.png)

사용자 또는 그룹에 대한 사용 권한을 변경하려면 이 절차의 1단계를 반복한 후 해당 사용자 또는 그룹의 권한 목록에서 다른 옵션을 지정합니다. 사용자 또는 그룹에 대한 모든 사용 권한을 제거하려면 해당 사용자 또는 그룹에 대한 **x** 아이콘을 클릭하거나 탭합니다.

### <a name="send-email-notification"></a>전자 메일 알림 보내기
앱을 공유할 때 전자 메일을 통해 사용자 또는 보안 그룹에 알릴지 여부를 선택할 수 있습니다. 이 옵션을 선택하면 사용자, 사용자 그룹 또는 보안 그룹에 알리는 전자 메일을 보내게 됩니다. 전자 메일에는 앱에 액세스할 수 있는 링크가 포함됩니다. 필요한 경우 사용자에게 PowerApps에 등록하라는 메시지가 표시됩니다.

알림에는 할당하는 권한에 따라 다른 종류의 링크가 포함됩니다.

- **사용 가능** 권한으로 앱을 공유하면 이메일에 앱을 실행하는 링크가 포함됩니다.
- **편집 가능** 권한으로 앱을 공유하면 이메일에 앱을 실행하거나 편집할 수 있는 링크가 포함됩니다.

### <a name="how-do-my-users-see-the-app-i-shared"></a>내 사용자가 공유한 앱을 보려면 어떻게 해야 할까요?
하나 이상의 사용자 또는 보안 그룹과 앱을 공유한 후 앱을 볼 수 있는 방법은 앱을 공유한 권한에 따라 다릅니다.

##### <a name="if-you-shared-an-app-with-user-permission"></a>*사용자* 권한으로 앱을 공유한 경우
앱을 공유한 사용자는 앱 공유 화면에서 해당 확인란을 선택하면 전자 메일 알림을 받게 됩니다. 전자 메일에서 링크를 클릭하거나 탭하여 [Dynamics 365](http://home.dynamics.com)에서 앱을 실행할 수 있습니다. 곧 유니버설 링크를 지원할 예정입니다. 즉, PowerApps Studio 또는 PowerApps Mobile이 설치되어 있는 경우 이 앱은 PowerApps Studio 또는 PowerApps Mobile에서 열립니다.

또한 사용자는 [Dynamics 365](http://home.dynamics.com)의 AppSource에서 앱을 발견할 수도 있습니다(예: 전자 메일을 보내지 않은 경우). 사용자가 AppSource를 통해 앱을 얻을 수 있는 방법에 대해 [자세히 알아보세요](../../user/app-source.md).

##### <a name="if-you-shared-an-app-with-contributor-permission"></a>'참가자' 권한으로 앱을 공유한 경우
앱을 공유한 사용자는 앱 공유 화면에서 해당 확인란을 선택하면 전자 메일 알림을 받게 됩니다. 전자 메일에서는 웹용 PowerApps Studio를 사용하여 편집하기 위해 직접 앱을 여는 링크를 클릭하거나 탭할 수 있습니다. [Dynamics 365](http://home.dynamics.com)에서 앱을 실행하기 위한 링크도 있습니다. 곧 유니버설 링크를 지원할 예정입니다. 즉, PowerApps Studio 또는 PowerApps Mobile이 설치되어 있는 경우 이 앱은 PowerApps Studio 또는 PowerApps Mobile에서 열립니다.

또한 사용자는 [powerapps.com](http://web.powerapps.com)에서 앱을 발견할 수 있습니다(예: 이메일을 보내지 않은 경우). 이는 앱 작성자가 자신이 만들었거나 **참가자** 권한으로 공유된 모든 앱을 탐색하는 홈입니다. 반면 [Dynamics 365](http://home.dynamics.com)는 사용자가 PowerApps 및 기타 비즈니스 앱에서 앱을 빠르게 실행할 수 있는 곳입니다.

## <a name="other-things-to-know"></a>알아야 할 기타 사항
* 앱을 공유하려면 로컬이 아닌 클라우드에 저장해야 합니다.
* 앱을 공유하기 전에 공유할 사용자 및 보안 그룹과 각각에 적용하려는 역할(예: **편집 가능** 또는 **사용 가능**)을 고려해야 합니다. 그룹과 앱을 공유한 경우 그룹의 기존 회원 및 가입하는 모든 회원이 지정된 사용 권한을 받습니다. 그룹을 떠난 사람은 액세스가 있는 다른 그룹의 회원이거나 명시적으로 사용 권한이 지정된 경우가 아니면 사용 권한을 잃게 됩니다.
* 그룹의 모든 구성원은 앱에 대해 전체 그룹과 동일한 권한을 갖습니다. 하지만 해당 그룹의 한 명 또는 그 이상의 회원에게 더 많은 사용 권한을 지정하여 더 많은 액세스를 허용할 수 있습니다. 예를 들어 보안 그룹 A에 **사용 가능** 권한을 제공할 수 있지만 해당 그룹에 속한 사용자 B에게 **편집 가능** 권한을 제공할 수 있습니다. 보안 그룹의 모든 구성원은 앱을 실행할 수 있지만 사용자 B만 편집할 수 있습니다. 보안 그룹 A에 **편집 가능** 권한을, 사용자 B에게 **사용 가능** 권한을 제공할 경우, 해당 사용자는 여전히 앱을 편집할 수 있습니다.
* 전체 조직과 앱을 공유할 수 있지만 모든 사람이 앱에 액세스해야 하는지를 신중하게 고려해야 합니다.
* 공유 앱에 대한 모든 변경 내용은 저장하는 즉시 공유한 사람들에게 전달됩니다. 앱을 개선하면 모든 사용자가 혜택을 봅니다. 앱을 중단하면 모든 사용자에게 영향이 있습니다.
* 앱을 공유하기 전에 앱에 의미 있는 이름과 설명을 지정하면 사람들이 어떤 앱인지 알 수 있고 목록에서 쉽게 선택할 수 있습니다. PowerApps Studio의 **파일** 메뉴에서 **앱 설정**을 클릭하거나 탭한 다음 설명을 입력합니다.

### <a name="app-sharing-and-the-resources-the-app-uses"></a>앱 공유 및 앱에서 사용하는 리소스
대부분의 앱은 다음 중 적어도 하나의 형식의 리소스에 의존합니다.

* 데이터 원본에 연결
* 온-프레미스 데이터 게이트웨이
* 사용자 지정 커넥터
* Excel 통합 문서 또는 기타 서비스
* 흐름

사용자와 참가자에게는 앱에서 사용하는 모든 데이터 연결 및 게이트웨이에 대한 권한이 필요합니다. 일부 권한은 앱과 함께 암시적으로 제공되지만, 다른 권한은 명시적으로 부여되어야 합니다. 자세한 정보는 [앱 리소스 공유](share-app-resources.md)를 참조하세요.

이전 버전의 Common Data Service를 사용하는 앱을 공유하는 경우 Common Data Service에 대한 런타임 권한을 별도로 공유해야 합니다. 이 작업을 수행할 수 있는 권한이 없으면 환경 관리자에게 문의하세요. Common Data Service의 가장 최신 버전을 사용하는 앱을 공유하는 경우 사용자 지정 역할을 만들고 여기에 사용자를 할당해야 합니다. Common Data Service 보안에 대해 [자세히 알아보세요](../../administrator/database-security.md).

### <a name="what-isnt-supported"></a>지원되지 않는 사항
* 보안 그룹에 있지만 메일 그룹에는 공유할 수 없습니다.
* 조직의 사용자와 앱을 공유할 수 있지만, 다른 테넌트의 사용자와는 공유할 수 없습니다.
* 해당 앱에 대한 **편집 가능**(**사용 가능** 아님) 권한이 있는 경우 앱을 다시 공유할 수 있습니다.
