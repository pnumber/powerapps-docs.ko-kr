---
title: '라디오 컨트롤: 참조 | Microsoft Docs'
description: 속성 및 예제를 포함한 라디오 컨트롤에 관한 정보
services: ''
suite: powerapps
documentationcenter: na
author: fikaradz
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/25/2016
ms.author: fikaradz
ms.openlocfilehash: 9cf051ba94e9d43b4c263d627c25affa66e6b843
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="radio-control-in-powerapps"></a>PowerApps의 라디오 컨트롤
사용자가 한 번에 하나만 선택할 수 있는 모든 옵션을 표시하는 목록입니다.

## <a name="description"></a>설명
오래 사용되어 온 **라디오** 컨트롤에는 상호 배타적인 몇 가지 옵션만 사용하는 것이 좋습니다.

## <a name="key-properties"></a>주요 속성
**[Default](properties-core.md)** – 사용자가 컨트롤을 변경하기 전의 초기 값입니다.

**[Items](properties-core.md)** – 갤러리, 목록 또는 차트와 같은 컨트롤에 표시되는 데이터 원본입니다.

[!INCLUDE [long-items](../../../includes/long-items.md)]

**[Value](properties-core.md)** – 입력 컨트롤의 값입니다.

## <a name="all-properties"></a>모든 속성
**[Align](properties-text.md)** - 컨트롤의 가로 가운데를 기준으로 한 텍스트의 위치입니다.

**[BorderColor](properties-color-border.md)** - 컨트롤의 테두리 색입니다.

**[BorderStyle](properties-color-border.md)** - 컨트롤의 테두리는 **Solid**, **Dashed**, **Dotted**, **None**입니다.

**[BorderThickness](properties-color-border.md)** - 컨트롤의 테두리 굵기입니다.

**[FocusedBorderThickness](properties-color-border.md)** - 키보드 포커스가 있을 때 컨트롤의 테두리 두께입니다.

**[Color](properties-color-border.md)** – 컨트롤의 텍스트 색입니다.

**[DisplayMode](properties-core.md)** – 컨트롤이 사용자 입력을 허용(**편집**)하거나, 데이터만 표시(**보기**)하거나 사용 안 하도록(**사용 안 함**) 설정할지 선택합니다.

**[DisabledBorderColor](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 테두리 색입니다.

**[DisabledColor](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 텍스트 색입니다.

**[DisabledFill](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 배경색입니다.

**[Fill](properties-color-border.md)** - 컨트롤의 배경색입니다.

**[Font](properties-text.md)** – 텍스트가 표시되는 글꼴의 제품군 이름입니다.

**[FontWeight](properties-text.md)** - 컨트롤의 텍스트 굵기입니다. **Bold**, **Semibold**, **Normal** 또는 **Lighter**로 설정합니다.

**[Height](properties-size-location.md)** – 컨트롤의 위쪽 및 아래쪽 가장자리 사이의 간격입니다.

**[HoverColor](properties-color-border.md)** – 사용자가 해당 컨트롤에 마우스 포인터를 올려두는 경우 컨트롤의 텍스트 색입니다.

**[HoverFill](properties-color-border.md)** – 사용자가 해당 컨트롤에 마우스 포인터를 올려두는 경우 컨트롤의 배경색입니다.

**[Italic](properties-text.md)** - 컨트롤의 텍스트를 기울임꼴로 설정할지 여부를 선택합니다.

**[LineHeight](properties-text.md)** - 예를 들어 텍스트 선 또는 목록의 항목 사이의 거리입니다.

**[OnChange](properties-core.md)** – 사용자가 컨트롤의 값을 변경할 때(예: 슬라이더 조절) 앱이 응답하는 방식입니다.

**[OnSelect](properties-core.md)** – 사용자가 앱을 클릭하거나 탭할 때 앱이 응답하는 방법입니다.

**[PaddingBottom](properties-size-location.md)** – 컨트롤의 텍스트와 해당 컨트롤의 아래쪽 가장자리 사이의 거리입니다.

**[PaddingLeft](properties-size-location.md)** – 컨트롤의 텍스트와 해당 컨트롤의 왼쪽 가장자리 사이의 거리입니다.

**[PaddingRight](properties-size-location.md)** – 컨트롤의 텍스트와 해당 컨트롤의 오른쪽 가장자리 사이의 거리입니다.

**[PaddingTop](properties-size-location.md)** – 컨트롤의 텍스트와 해당 컨트롤의 위쪽 가장자리 사이의 거리입니다.

**[PressedColor](properties-color-border.md)** – 사용자가 컨트롤을 탭하거나 클릭하는 경우 컨트롤의 텍스트 색입니다.

**[PressedFill](properties-color-border.md)** – 사용자가 컨트롤을 탭하거나 클릭하는 경우 컨트롤의 배경색입니다.

**RadioBackgroundFill** – 라디오 단추 컨트롤에서 원의 배경색입니다.

**RadioBorderColor** - 라디오 단추 컨트롤에서 각 옵션의 원 색입니다.

**RadioSelectionFill** – 라디오 단추 컨트롤에서 선택된 원 안에 표시되는 색입니다.

**RadioSize** – 라디오 단추 컨트롤에서 원의 직경입니다.

**[Reset](properties-core.md)** – 컨트롤이 기본값으로 되돌아가는지 여부입니다.

**[Size](properties-text.md)** -컨트롤에 표시되는 텍스트의 글꼴 크기입니다.

**[Strikethrough](properties-text.md)** - 컨트롤에 표시되는 텍스트 중앙에 선을 표시할지 여부를 선택합니다.

**[TabIndex](properties-accessibility.md)** – 0 이외의 값으로 설정된 경우 런타임 시 컨트롤의 탭 순서를 사용자 지정합니다.

**[Tooltip](properties-core.md)** – 사용자가 마우스로 컨트롤을 가리킬 때 표시되는 설명 텍스트입니다.

**[Underline](properties-text.md)** – 컨트롤에 표시되는 텍스트 아래에 선을 표시할지 여부를 선택합니다.

**[Visible](properties-core.md)** – 컨트롤을 표시하거나 숨길지 여부를 선택합니다.

**[Width](properties-size-location.md)** – 컨트롤의 왼쪽 및 오른쪽 가장자리 사이의 간격입니다.

**[X](properties-size-location.md)** – 컨트롤의 왼쪽 가장자리와 해당 부모 컨테이너(부모 컨테이너가 없는 경우 화면)의 왼쪽 가장자리 사이의 거리입니다.

**[Y](properties-size-location.md)** – 컨트롤의 위쪽 가장자리와 해당 부모 컨테이너(부모 컨테이너가 없는 경우 화면)의 위쪽 가장자리 사이의 거리입니다.

## <a name="related-functions"></a>관련된 함수
[**Distinct**( *DataSource*, *ColumnName* )](../functions/function-distinct.md)

## <a name="example"></a>예
1. **라디오** 컨트롤을 추가하고 이름을 **Pricing**으로 지정한 다음 **[Items](properties-core.md)** 속성을 다음 수식으로 설정합니다.
   <br>**["Standard", "Premium"]**
   
    [컨트롤을 추가, 이름을 지정하고, 구성](../add-configure-controls.md)하는 방법을 모르시나요?
2. **[레이블](control-text-box.md)** 컨트롤을 추가하고 **라디오** 컨트롤 아래로 이동한 다음 **[레이블](control-text-box.md)** 컨트롤의 **[Text](properties-core.md)** 속성을 다음 수식으로 설정합니다.
   <br>**If("Premium" in Pricing.Selected.Value, "$200 per day", "$150 per day")**
   
    **[If](../functions/function-if.md)** 함수 또는 [다른 함수](../formula-reference.md)에 대해 더 알고 싶으신가요?
3. F5 키를 선택한 후 **라디오** 컨트롤에서 한 옵션을 선택합니다.
   
    **[레이블](control-text-box.md)** 컨트롤이 선택에 적합한 텍스트를 표시합니다.
4. (선택 사항) **라디오** 컨트롤에서 다른 옵션을 선택하여 적합한 텍스트가 표시되는지 확인합니다.
5. 기본 작업 영역으로 돌아가려면 Esc 키를 누릅니다.

