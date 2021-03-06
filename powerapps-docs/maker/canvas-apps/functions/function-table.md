---
title: Table 함수 | Microsoft Docs
description: PowerApps의 Table 함수에 대한 구문과 예제를 포함한 참조 정보
services: ''
suite: powerapps
documentationcenter: na
author: gregli-msft
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/07/2015
ms.author: gregli
ms.openlocfilehash: 2f543a75019bfe5d665aedb2e6171200e8321690
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="table-function-in-powerapps"></a>PowerApps의 Table 함수
임시 [테이블](../working-with-tables.md)을 만듭니다.

## <a name="description"></a>설명
**Table** 함수는 [레코드](../working-with-tables.md#records)의 인수 목록에서 테이블을 만듭니다.

테이블의 [열](../working-with-tables.md#columns)은 모든 인수 레코드의 모든 속성의 합집합입니다. 레코드에 값이 없는 열에는 *빈* 값이 추가됩니다.

테이블은 문자열이나 숫자처럼 PowerApps의 값입니다. 테이블을 함수의 인수로 지정할 수 있으며 함수는 테이블을 결과로 반환할 수 있습니다. **Table**은 영구 테이블을 만들지 않습니다. 대신 인수로 이루어진 임시 테이블을 반환합니다.  이 임시 테이블을 다른 함수의 인수로 지정하거나 갤러리에서 시각화하거나 다른 테이블에 포함할 수 있습니다.  자세한 내용은 [테이블 작업](../working-with-tables.md)을 참조하세요.

**[ value1, value2, ... ]** 구문을 사용하여 단일 열 테이블을 만들 수도 있습니다.

## <a name="syntax"></a>구문
**Table**( *Record1* [, *Record2*, ... ] )

* *Record(s)* - 필수 항목입니다. 테이블에 추가할 레코드입니다.

## <a name="examples"></a>예
* 목록 상자의 **[Items](../controls/properties-core.md)** 속성을 다음 수식으로 설정합니다.
  <br>**Table({Color:"red"}, {Color:"green"}, {Color:"blue"})**
  
    목록 상자는 각 색상을 옵션으로 표시합니다.
* 텍스트 갤러리를 추가하고 **[Items](../controls/properties-core.md)** 속성을 다음 함수로 설정합니다.<br>
  **Table({Item:"Violin123", Location:"France", Owner:"Fabrikam"}, {Item:"Violin456", Location:"Chile"})**
  
    갤러리에 항목의 이름과 위치가 포함된 두 개의 레코드가 표시됩니다. 하나의 레코드에만 소유자의 이름이 포함됩니다.

