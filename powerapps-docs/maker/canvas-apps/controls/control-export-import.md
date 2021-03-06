---
title: '컨트롤 내보내기 및 가져오기: 참조 | Microsoft Docs'
description: 속성 및 예제를 포함한 컨트롤 내보내기 및 가져오기에 대한 정보
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
ms.openlocfilehash: 2bc1eddc09fde255fbc1f7a7899ba2f416374e0c
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="export-control-and-import-control-in-powerapps"></a>PowerApps에서 컨트롤 내보내기 및 가져오기
로컬 파일에 데이터를 내보내고 해당 데이터를 PowerApps의 다른 앱으로 가져오기 위한 컨트롤

## <a name="description"></a>설명
동일한 데이터를 사용하는 여러 앱을 만들고자 하지만 해당 앱 외부로 데이터를 공유하고 싶지 않는 경우 **내보내기** 컨트롤과 **가져오기** 컨트롤을 사용하여 데이터를 가져오거나 내보낼 수 있습니다. 데이터를 내보낼 때 만든 압축 파일은 다른 컴퓨터에 복사할 수 있지만 PowerApps 이외의 프로그램에서는 읽을 수 없습니다.

## <a name="warning"></a>경고
앱에서 이 기능을 활성화하면 보안상 취약한 부분 및 데이터 유출에 노출될 수 있습니다.  사용자가 인식되고 신뢰할 수 있는 파일만 가져오고 기밀 정보나 민감한 정보가 없는 데이터만 내보내도록 안내해야 합니다.

## <a name="key-properties"></a>주요 속성
**Data** - 로컬 파일에 내보낼 컬렉션의 이름입니다.

* **Data** 속성은 **내보내기** 컨트롤에만 사용할 수 있으며 **가져오기** 컨트롤에는 사용할 수 없습니다.

**[OnSelect](properties-core.md)** – 사용자가 앱을 클릭하거나 탭할 때 앱이 응답하는 방법입니다.

## <a name="additional-properties"></a>추가 속성
**[Align](properties-text.md)** - 컨트롤의 가로 가운데를 기준으로 한 텍스트의 위치입니다.

**[BorderColor](properties-color-border.md)** - 컨트롤의 테두리 색입니다.

**[BorderStyle](properties-color-border.md)** - 컨트롤의 테두리는 **Solid**, **Dashed**, **Dotted**, **None**입니다.

**[BorderThickness](properties-color-border.md)** - 컨트롤의 테두리 굵기입니다.

**[Color](properties-color-border.md)** – 컨트롤의 텍스트 색입니다.

**[DisplayMode](properties-core.md)** – 컨트롤이 사용자 입력을 허용(**편집**)하거나, 데이터만 표시(**보기**)하거나 사용 안 하도록(**사용 안 함**) 설정할지 선택합니다.

**[DisabledBorderColor](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 테두리 색입니다.

**[DisabledColor](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 텍스트 색입니다.

**[DisabledFill](properties-color-border.md)** – 컨트롤의 **[DisplayMode](properties-core.md)** 속성이 **Disabled**로 설정된 경우 컨트롤의 배경색입니다.

**[Fill](properties-color-border.md)** - 컨트롤의 배경색입니다.

**[Font](properties-text.md)** – 텍스트가 표시되는 글꼴의 제품군 이름입니다.

**[FontWeight](properties-text.md)** - 컨트롤의 텍스트 굵기입니다. **Bold**, **Semibold**, **Normal** 또는 **Lighter**로 설정합니다.

**[Height](properties-size-location.md)** – 컨트롤의 위쪽 및 아래쪽 가장자리 사이의 간격입니다.

**[HoverBorderColor](properties-color-border.md)** – 사용자가 해당 컨트롤에 마우스 포인터를 올려두는 경우 컨트롤의 테두리 색입니다.

**[HoverColor](properties-color-border.md)** – 사용자가 해당 컨트롤에 마우스 포인터를 올려두는 경우 컨트롤의 텍스트 색입니다.

**[HoverFill](properties-color-border.md)** – 사용자가 해당 컨트롤에 마우스 포인터를 올려두는 경우 컨트롤의 배경색입니다.

**[Italic](properties-text.md)** - 컨트롤의 텍스트를 기울임꼴로 설정할지 여부를 선택합니다.

**[Padding](properties-size-location.md)** – 가져오기 또는 내보내기 단추의 텍스트와 단추의 가장자리 사이의 간격입니다.

**[PressedBorderColor](properties-color-border.md)** – 사용자가 컨트롤을 탭하거나 클릭하는 경우 컨트롤의 테두리 색입니다.

**[PressedColor](properties-color-border.md)** – 사용자가 컨트롤을 탭하거나 클릭하는 경우 컨트롤의 텍스트 색입니다.

**[PressedFill](properties-color-border.md)** – 사용자가 컨트롤을 탭하거나 클릭하는 경우 컨트롤의 배경색입니다.

**[RadiusBottomLeft](properties-size-location.md)** – 컨트롤 왼쪽 아래 모서리의 둥근 정도입니다.

**[RadiusBottomRight](properties-size-location.md)** – 컨트롤 오른쪽 아래 모서리의 둥근 정도입니다.

**[RadiusTopLeft](properties-size-location.md)** – 컨트롤 왼쪽 위 모서리의 둥근 정도입니다.

**[RadiusTopRight](properties-size-location.md)** – 컨트롤 오른쪽 위 모서리의 둥근 정도입니다.

**[Size](properties-text.md)** -컨트롤에 표시되는 텍스트의 글꼴 크기입니다.

**[Strikethrough](properties-text.md)** - 컨트롤에 표시되는 텍스트 중앙에 선을 표시할지 여부를 선택합니다.

**[Text](properties-core.md)** – 컨트롤에 표시되는 텍스트 또는 사용자가 컨트롤에 입력하는 텍스트입니다.

**[Underline](properties-text.md)** – 컨트롤에 표시되는 텍스트 아래에 선을 표시할지 여부를 선택합니다.

**[VerticalAlign](properties-text.md)** – 컨트롤의 세로 가운데를 기준으로 한 텍스트의 위치입니다.

**[Visible](properties-core.md)** – 컨트롤을 표시하거나 숨길지 여부를 선택합니다.

**[Width](properties-size-location.md)** – 컨트롤의 왼쪽 및 오른쪽 가장자리 사이의 간격입니다.

**[X](properties-size-location.md)** – 컨트롤의 왼쪽 가장자리와 해당 부모 컨테이너(부모 컨테이너가 없는 경우 화면)의 왼쪽 가장자리 사이의 거리입니다.

**[Y](properties-size-location.md)** – 컨트롤의 위쪽 가장자리와 해당 부모 컨테이너(부모 컨테이너가 없는 경우 화면)의 위쪽 가장자리 사이의 거리입니다.

## <a name="example"></a>예
1. **[단추](control-button.md)** 컨트롤을 추가하고 이 수식에 **[OnSelect](properties-core.md)** 속성을 설정합니다.
   <br>**ClearCollect(Products, {Name:"Europa", Price:"10.99"}, {Name:"Ganymede", Price:"12.49"}, {Name:"Callisto", Price:"11.79"})**
   
    [컨트롤을 추가, 이름을 지정하고, 구성](../add-configure-controls.md)하는 방법을 모르시나요?
   
    **[ClearCollect](../functions/function-clear-collect-clearcollect.md)** 함수 또는 [다른 함수](../formula-reference.md)에 대해 더 알고 싶으신가요?
2. F5를 누르고 **[단추](control-button.md)** 컨트롤을 클릭하거나 탭한 다음 Esc 키를 누릅니다.
3. **내보내기** 컨트롤을 추가하고 **제품**에 **Data** 속성을 설정합니다.
4. F5를 누르고 **내보내기** 컨트롤을 클릭하거나 탭한 다음 데이터를 내보낼 파일의 이름을 지정합니다.
5. **저장**을 클릭하거나 탭한 다음 Esc를 눌러 기본 작업 영역으로 돌아갑니다.
6. 기존 또는 새 앱에서 **가져오기** 컨트롤을 추가하고 **MyData**로 이름을 지정한 다음 **[OnSelect](properties-core.md)** 속성에 이 수식을 설정합니다.<br>
   **Collect(ImportedProducts, MyData.Data)**
7. F5를 누르고 **MyData**를 클릭하거나 탭한 다음 내보낸 파일을 클릭하거나 탭하고 **열기**를 클릭하거나 탭합니다.
8. Esc 키를 누르고 **파일** 메뉴에서 **컬렉션**을 클릭하거나 탭한 다음 현재 앱에 내보낸 데이터가 있는지 확인하십시오.

