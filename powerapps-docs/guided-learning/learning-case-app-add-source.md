---
title: "데이터 원본 및 흐름 추가(Common Data Service) | Microsoft Docs"
description: "추가 데이터 가져오기 및 앱에서 흐름 트리거"
services: 
suite: powerapps
documentationcenter: na
author: mgblythe
manager: anneta
editor: 
tags: 
featuredvideoid: Y057qUJ2NNk
courseduration: 11m
ms.service: powerapps
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/09/2016
ms.author: mblythe
ms.openlocfilehash: 42f0d43984c88dc9a5e6ffe67ca3b7ff6cedf8b7
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2017
---
# <a name="add-a-data-source-and-flow-common-data-service"></a>데이터 원본 및 흐름 추가(Common Data Service)
지금까지 이 섹션에서는 Common Data Service에서 사례 엔터티를 기반으로 하여 앱을 생성하고, 탐색하여 결합 방법을 확인하고, 여러 가지 방식으로 사용자 지정했습니다. 이 섹션의 마지막 항목에서는 다른 표준 엔터티를 가져오고 Microsoft Flow를 사용하여 전자 메일을 보냅니다. 사례를 업데이트한 경우 앱에서 해당 사례를 연 사람에게 알리도록 흐름을 트리거합니다. 이 항목에서 특정 시나리오를 완료하지만 다양한 종류의 앱에 적용할 수 있는 기술을 습득하게 됩니다. 엔터티로 시작해 보겠습니다.

## <a name="review-entity-relationships"></a>엔터티 관계 검토
연락처 엔터티를 곧 추가하겠습니다. 하지만 사례와 연락처 엔터티가 서로 어떻게 관계되는지 먼저 살펴보겠습니다. 사례 엔터티에서 필드 중 하나가 **CurrentContact**이고 **조회** 데이터 형식임을 알 수 있습니다. 즉 이 필드는 다른 테이블과의 관계에서 사용됩니다.

![사례 엔터티 필드](./media/learning-case-app-add-source/case-fields.png)

**관계** 탭에서 관련 엔터티가 **연락처**임을 알 수 있습니다. 이 항목의 뒷부분에서 이 관계를 사용할 것이므로 이 점에 유의해야 합니다.

![사례 엔터티 관계](./media/learning-case-app-add-source/case-relationships.png)

## <a name="add-an-entity-to-the-app"></a>앱에 엔터티 추가
데이터 원본은 PowerApps에 간단하게 추가할 수 있습니다. 오른쪽 창에서 **데이터 원본**, **데이터 원본 추가**를 차례로 클릭하거나 탭합니다. 이 경우 **Common Data Service** 연결을 선택하고 **연락처** 엔터티를 선택합니다. **연결**을 클릭하거나 탭하면 항목을 앱에 추가합니다. 

![연락처 엔터티 추가](./media/learning-case-app-add-source/contact-entity.png)

이 예에서는 다른 엔터티의 데이터를 추가하지만 앱에서 여러 원본의 데이터를 결합할 수 있습니다. 

## <a name="look-up-contact-information"></a>연락처 정보 조회
이제 앱에서 연락처 엔터티 데이터에 액세스할 수 있으므로 이 데이터를 사용해 볼 때입니다. 소개에서 언급했듯이 사례가 업데이트되면 전자 메일을 보내려고 합니다. 이렇게 하려면 두 가지 수식과 흐름을 사용합니다. 첫 번째 수식은 편집 화면, 특히 저장 단추의 OnSelect 속성을 위한 것입니다.

![앱 편집 화면](./media/learning-case-app-add-source/edit-screen.png)

기본적으로 이 단추는 양식에서 데이터를 편집할 때 `SubmitForm(EditForm1)` 수식을 사용하여 업데이트를 제출합니다. 수식에 추가하여 현재 사례를 연 사람의 연락처 정보를 먼저 조회한 다음 해당 정보를 앱에 로컬로 저장해야 합니다. 

```UpdateContext({contact:LookUp(Contact, ContactId=BrowseGallery1.Selected.CurrentContact.ContactId)}); SubmitForm(EditForm1)```

예, 조금 복잡하지만 James는 비디오 재생의 2분 4초 시점에서 이 수식을 보다 자세히 설명하고 있습니다.

## <a name="trigger-a-flow-from-the-app"></a>앱에서 흐름 트리거
이제 각 사례에 대한 연락처가 누구인지를 알게 되었으므로 전자 메일을 보낼 수 있습니다. 앱에서 전자 메일을 직접 보낼 수도 있지만 이 예에서는 앱에서 흐름을 트리거하는 방법을 보여 줍니다. 흐름은 가져오기와 같이 매우 간단하게 앱에서 작업을 기반으로 하여 전자 메일을 보냅니다. 흐름에 대한 자세한 내용은 여기서 다루지 않겠지만 완전한 Microsoft Flow 학습 도우미가 준비되어 있습니다. 

![전자 메일을 보내는 흐름](./media/learning-case-app-add-source/email-flow.png)

앱으로 돌아가서 이벤트에 따라 흐름을 호출해야 합니다. 편집 양식의 OnSuccess 속성을 사용하므로 편집이 성공하면 흐름이 트리거됩니다. 편집 양식을 클릭하거나 탭한 다음 리본 메뉴에서 **작업** > **흐름**을 차례로 클릭하거나 탭합니다. 사용할 흐름을 선택합니다. 

![전자 메일을 보내는 흐름](./media/learning-case-app-add-source/add-flow-action.png)

이제 흐름이 편집 양식의 OnSuccess 이벤트와 연결되며 전자 메일에 대한 연락처를 참조할 수 있습니다. 다음 수식은 사례를 연 사람의 전자 메일 주소, 제목 줄 및 전자 메일 본문을 사용하여 흐름을 호출합니다. 

```CaseResolvedEmailConfirmation.Run(contact.EmailPrimary, "Your case has been updated", "Check it out")```

데이터 원본을 앱에 추가하고 전자 메일을 보내는 흐름을 트리거하는 수식입니다. 아직 이 섹션에서 비디오를 보지 않았다면 그렇게 해보는 것이 좋습니다. 이 비디오는 신속히 안내하면서 다양한 항목에 대해 자세히 알려줍니다.

## <a name="wrapping-it-all-up"></a>요약
이제 이 섹션의 끝에 있습니다. 즐기면서 많이 알게 되었기를 바랍니다. 엔터티에서 기본 앱을 생성하기 시작했으며, 엔터티를 결합하는 방식을 이해하기 위해 앱을 조금 살펴보았습니다. 앱 사용자 지정에 많은 시간을 들이고, 데이터 원본을 추가하고, 흐름을 트리거하는 방법을 확인했습니다. 이 섹션에서는 특정 사례 관리 앱을 빌드했지만, 여기서 습득한 기술은 다양한 종류의 앱에 적용할 수 있습니다. 이 섹션의 시작 부분에서 언급했듯이 더 복잡한 사례 관리 앱을 자세히 알아보려면 Windows용 PowerApps Studio에서 사용할 수 있는 템플릿을 확인해 보세요. 

다음으로 앱 관리로 이동합니다. 관리 섹션에서는 앱을 공유하고 버전을 지정하는 방법을 보여 주고 앱, 데이터 및 기타 리소스의 컨테이너인 환경을 소개합니다. 
