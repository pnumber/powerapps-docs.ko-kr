---
title: "규칙 만들기 | Microsoft Docs"
description: "규칙을 만들어 앱 논리를 빌드하기 위한 단계별 지침"
services: 
suite: PowerApps
documentationcenter: na
author: karthik-1
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/14/2017
ms.author: karthikb
ms.openlocfilehash: c6b7141c20591c1fdbb5278b1fe4d75bfb6a4ebb
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2017
---
# <a name="create-a-rule-in-powerapps"></a>PowerApps에서 규칙 만들기
지정된 조건에 따라 앱을 자동으로 수정하는 규칙을 만듭니다. 예를 들어 상태에 따라 빨강, 노랑 또는 녹색으로 목록 항목을 표시하거나 특정 사용자(예: 관리자)에 대한 승인 단추를 표시합니다.

다양한 컨트롤에 규칙을 추가할 수 있습니다. **슬라이더** 컨트롤의 값이 70보다 큰 경우 이 항목에서 **레이블** 컨트롤의 텍스트 색을 변경하는 규칙을 추가합니다.

## <a name="add-a-rule"></a>규칙 추가
1. 컨트롤을 선택하거나 컨트롤을 추가하고 선택된 상태로 둡니다.
   
    이 항목의 경우 [레이블 및 슬라이더를 추가하고](add-configure-controls.md), 레이블의 **텍스트** 속성을 **Slider1.Value**로 설정하고, 슬라이더를 선택합니다.
2. 오른쪽 패널에서 **규칙**을 클릭하거나 누르고 **새 규칙**을 클릭하거나 누릅니다.
   
    ![새 규칙 만들기](./media/working-with-rules/new-rule.png)
   
    하나 이상의 규칙이 이미 정의되어 있는 컨트롤을 선택하는 경우 클릭하거나 눌러서 편집할 수 있습니다.  

## <a name="add-a-condition"></a>조건 추가
조건은 true 또는 false로 평가되는 식입니다(예: 값이 70보다 큰지 여부). 템플릿에 따라 식을 작성하거나 처음부터 시작할 수 있습니다. 또한 UI(Intellisense)의 지침에 따라 식을 사용자 지정할 수 있습니다.

1. **조건 추가**를 클릭하거나 누르고, 템플릿 또는 **사용자 지정 조건**을 클릭합니다.
   
    이 항목의 경우 **초과**를 클릭하거나 누릅니다.
   
    ![조건 추가](./media/working-with-rules/rule-conditions.png)
2. 규칙이 적용되는 시점을 정의하는 식을 완료합니다.
   
    이 항목의 경우 다음 식을 사용합니다. <br>**Value(Slider1.Value) > 70**
   
    **참고**: 이 항목을 작성할 때 비교에 사용되는 컨트롤의 속성을 지정해야 합니다. 이후 릴리스에서 PowerApps은 컨트롤의 공용 속성(예: **텍스트** 또는 **값**)을 유추할 수 있습니다.

## <a name="add-an-action"></a>작업 추가
작업은 규칙이 적용될 때 상황을 정의합니다. PowerApps는 컨트롤에 적용한 변경 내용에 따라 자동으로 작업을 만들 수 있습니다.

1. **작업 정의**를 클릭하거나 누릅니다.
   
    ![작업 정의](./media/working-with-rules/rule-define-actions.png)
2. 확인 대화 상자에서 **Let's go**를 클릭하거나 누릅니다. 그러면 PowerApps는 다음 변경 내용을 하나 이상의 작업으로 캡처합니다.
3. 조건이 true인 경우 예상과 일치하도록 하나 이상의 컨트롤을 구성합니다.
   
    이 항목의 경우 레이블의 색을 변경합니다.
   
    ![캡처 속성](./media/working-with-rules/rule-capture-properties.png)
4. (선택 사항) **작업 표시**를 클릭하거나 눌러서 변경 내용을 검토합니다.
   
    ![작업 검토](./media/working-with-rules/rule-review-actions.png)
5. 작업 추가를 마치면 **완료**를 클릭하거나 누릅니다.
6. 규칙에 대한 조건 및 작업을 검토한 다음 **완료**를 클릭하거나 눌러서 저장합니다.
   
    ![규칙 검토](./media/working-with-rules/rule-review.png)

## <a name="test-the-rule"></a>규칙 테스트
1. F5 키를 눌러 (또는 오른쪽 위 모서리의 재생 단추를 클릭하여) 앱을 미리 봅니다.
   
    ![미리 보기 열기](./media/working-with-rules/open-preview.png)
2. 지정한 조건을 true로 설정하고 작업이 예상 대로 작동하는지 확인합니다.
   
    이 항목의 경우 슬라이더를 70보다 큰 값으로 설정하고 레이블 텍스트가 색을 변경하는지 확인합니다.

## <a name="known-limitations"></a>알려진 제한 사항
이 항목을 작성할 때:

* 규칙 이름을 바꿀 수 없습니다.
* 양식이나 갤러리의 **ThisItem** 속성을 조건의 일부로 지정할 수 없습니다.
