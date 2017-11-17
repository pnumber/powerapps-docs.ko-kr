---
title: "Date 및 Time 함수 | Microsoft Docs"
description: "PowerApps의 Date 및 Time 함수에 대한 구문과 예제를 포함한 참조 정보"
services: 
suite: powerapps
documentationcenter: na
author: gregli-msft
manager: anneta
editor: 
tags: 
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/07/2015
ms.author: gregli
ms.openlocfilehash: bed2bc9b13b4d167d6852b7029e4e69d54d50413
ms.sourcegitcommit: 43be6a4e08849d522aabb6f767a81c092419babc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/07/2017
---
# <a name="date-and-time-functions-in-powerapps"></a>PowerApps의 Date 및 Time 함수
날짜 및 시간 구성 요소를 날짜/시간 값으로 변환합니다.

## <a name="description"></a>설명
**Date** 함수는 개별 연도, 월 및 일 값을 날짜/시간 값으로 변환합니다.  시간 부분은 자정입니다.

* 연도가 0과 1899(포함) 사이인 경우, 이 함수는 해당 값을 1900에 추가하여 연도를 계산합니다.  **70**은 **1970**이 됩니다.
* Month가 1보다 작거나 12보다 큰 경우, 결과는 지정된 연도의 시작부터 개월을 그만큼 빼거나 추가합니다.
* Day가 지정된 월의 일 수보다 큰 경우, 이 함수는 그만큼의 일 수를 월의 첫날에 추가하고 다음 달의 해당 날짜를 반환합니다.  Day가 1보다 작으면, 이 함수는 그만큼의 일 수 더하기 1을 지정된 월의 첫날에서 뺍니다.

**Time** 함수는 개별 시, 분, 초 값을 날짜/시간 값으로 변환합니다.  결과에는 연관된 날짜가 없습니다.

문자열을 값으로 변환하는 방법에 대한 자세한 내용은 **[DateValue](function-datevalue-timevalue.md)**, **[TimeValue](function-datevalue-timevalue.md)**, **[DateTimeValue](function-datevalue-timevalue.md)** 함수를 참조하세요.  

[날짜 및 시간 작업](../show-text-dates-times.md)에서도 자세한 내용을 참조하세요.

## <a name="syntax"></a>구문
**Date**( *Year*, *Month*, *Day* )

* *Year* - 필수 항목입니다.  1899보다 큰 숫자는 절대값으로 해석됩니다(1980은 1980으로 해석됩니다). 0에서 1899까지의 숫자는 1900의 상대값으로 해석됩니다. (예를 들어, 80은 1980으로 해석됩니다.)
* *Month* - 필수 항목입니다.  1부터 12까지의 숫자입니다.
* *Day* - 필수 항목입니다. 1부터 31까지의 숫자입니다.

**Time**( *Hour*, *Minute*, *Second* )

* *Hour* - 필수 항목입니다.  0(오전: 12:00)부터 23(오후 11:00)까지의 숫자입니다.
* *Minute* - 필수 항목입니다. 0부터 59까지의 숫자입니다.
* *Second* - 필수 항목입니다. 0부터 59까지의 숫자입니다.

## <a name="examples"></a>예
### <a name="date"></a>날짜
사용자가 **HireYear**라는 텍스트 입력 컨트롤에 **1979**를 입력하고 **HireMonth**라는 텍스트 입력 컨트롤에 **3**을 입력하고 **HireDay**라는 텍스트 입력 컨트롤에 **17**을 입력하면, 이 함수는 **3/17/1979**를 반환합니다.

**Date(Value(HireYear.Text), Value(HireMonth.Text), Value(HireDay.Text))**

### <a name="time"></a>시간
사용자가 **BirthHour**라는 텍스트 입력 컨트롤에 **14**를 입력하고 **BirthMinute**라는 텍스트 입력 컨트롤에 **50**을 입력하고 **BirthSecond**라는 텍스트 입력 컨트롤에 **24**를 입력하면, 이 함수는 **02:50:24 p**를 반환합니다.

**Text(Time(Value(BirthHour.Text), Value(BirthMinute.Text), Value(BirthSecond.Text)), "hh:mm:ss a/p")**
