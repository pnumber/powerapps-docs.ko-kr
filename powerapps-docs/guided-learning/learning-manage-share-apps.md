---
title: "앱 공유 | Microsoft Docs"
description: "동료 및 다른 사람들과 앱 공유"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: _nUU7oOy4oU
courseduration: 5m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: 67ed022be0cc4b1fc7d2d6acf7518c3526a54156
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2017
---
# <a name="share-your-apps"></a>앱 공유
자신의 비즈니스 요구 사항을 해결하는 앱을 빌드하는 것이 좋지만 PowerApps의 진정한 마법은 해당 앱을 다른 사람들과 공유하는 데 있습니다. 이제 앱을 만드는 방법을 알고 있으므로 이 항목에서는 공유하는 방법에 대해 살펴보겠습니다. 특정 사용자 또는 그룹과 앱을 공유하거나 전체 조직과 공유할 수 있습니다. 다른 사용자와 앱을 공유하면 브라우저 또는 Windows/iOS/Android용 PowerApps Mobile에서 Dynamics 365를 통해 실행할 수 있습니다. 또한 참가자 권한을 부여받은 경우 앱을 업데이트할 수도 있습니다.

## <a name="prepare-to-share-an-app"></a>앱 공유 준비
다른 사용자와 공유하려면 먼저 클라우드에 앱을 저장해야 합니다. 앱에 의미 있는 이름과 설명을 지정하면 사람들이 어떤 앱인지 알 수 있으며 목록에서 쉽게 선택할 수 있습니다. PowerApps Studio에서 **파일**을 클릭하거나 탭한 다음 설명을 입력합니다.

![앱 설명](./media/learning-manage-share-apps/app-description.png)

공유 앱에 대한 모든 변경 내용은 저장하는 즉시 공유한 사람들에게 전달됩니다. 앱을 개선하는 것은 좋지만, 기능을 제거하거나 많이 변경하면 다른 사람에게도 영향을 미칠 수 있습니다.

## <a name="share-an-app"></a>앱 공유
web.powerapps.com의 앱 타일에서 줄임표(...)를 클릭한 다음 **공유**를 클릭합니다.

![web.powerapps.com에서 앱 공유](./media/learning-manage-share-apps/share-app.png)

여기서는 앱을 공유하고, 다음 항목에서 다루게 될 앱 버전 관리도 제어할 수 있습니다. 앱을 공유할 사용자, 그룹 및 각 사용자에 부여할 역할(**사용자** 또는 **참가자**)을 지정합니다. **저장**을 클릭하거나 탭합니다.

![사용자 및 그룹 선택](./media/learning-manage-share-apps/select-users.png)

전자 메일을 통해 사용자에게 알리도록 선택하면 앱을 공유한 모든 사용자가 Dynamics 365 링크를 포함한 전자 메일을 받습니다. 또한 앱 참가자도 web.powerapps.com 링크를 받습니다.  Dynamics 365 링크를 따르지 않으면 해당 앱을 보여 주지 않습니다. AppSource에 있는 앱은 Dynamics 365에 직접 추가해야 합니다.

![Dynamics 365의 앱](./media/learning-manage-share-apps/dynamics-365.png)

## <a name="permissions-and-licensing"></a>권한 및 라이선스
권한 및 라이선스에 대해 자세히 설명하지는 않지만 공유와 관련된 몇 가지 기본 사항을 다루겠습니다.

* 사용자와 참가자에게는 공유 앱에서 사용하는 모든 데이터 연결 및 게이트웨이에 대한 권한이 필요합니다. 일부 권한은 앱과 함께 암시적으로 제공되지만, 다른 권한은 명시적으로 부여되어야 합니다.
* 앱에서 Common Data Service 엔터티를 사용하는 경우 사용자와 참가자는 Common Data Service 데이터베이스에 액세스해야 합니다. 또한 참가자가 엔터티를 직접 사용하는 경우 PowerApps "P2" 라이선스가 필요합니다.

앱을 쉽게 공유할 수 있으므로 유용하다고 판단되는 앱을 가져와서 조직 전체 사용자가 사용할 수 있게 하는 것이 좋습니다. 다음 항목에서는 앱을 사용하고 공유할 때 활성화되는 앱 버전을 제어하는 방법에 대해 설명하겠습니다.
