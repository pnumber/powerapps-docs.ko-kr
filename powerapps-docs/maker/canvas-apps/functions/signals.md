---
title: 가속, 앱, 나침반, 연결 및 위치 신호 | Microsoft Docs
description: PowerApps의 가속, 앱, 나침반, 연결 및 위치 센서 등, 구문 및 예제를 포함한 참조 정보
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
ms.openlocfilehash: ae649c4935a92d9db800dcd75fddf848eccbfcc1
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="acceleration-app-compass-connection-and-location-signals-in-powerapps"></a>PowerApps의 가속, 앱, 나침반, 연결 및 위치 신호 
전 세계에서 사용자의 위치, 표시할 화면 등과 같이 앱 환경 관련 정보를 반환합니다.  

## <a name="description-and-syntax"></a>설명 및 구문
모든 신호는 정보의 [레코드](../working-with-tables.md#records)를 반환합니다. 이 정보를 레코드로 사용 및 저장하거나, **.** [연산자](operators.md)를 사용하여 개별 속성을 추출할 수 있습니다.

### <a name="acceleration"></a>가속
**가속** 신호는 장치의 화면에 상대적인 장치의 가속을 3차원으로 반환합니다. 가속은 9.81m/초<sup>2</sup> 또는 32.2피트/초<sup>2</sup>의 *g* 단위로 측정됩니다(지구 중력이 표면의 물체에 영향을 미치는 가속도).

| 신호 속성 | 설명 |
| --- | --- |
| **Acceleration.X** |오른쪽 및 왼쪽.  오른쪽이 양수입니다. |
| **Acceleration.Y** |앞으로 및 뒤로.  앞으로가 양수입니다. |
| **Acceleration.Z** |위 및 아래.  위가 양수입니다. |

### <a name="app"></a>앱
**앱** 신호는 실행 중인 앱 관련 정보를 반환합니다.

| 신호 속성 | 설명 |
| --- | --- |
| **App.ActiveScreen** |표시되는 화면입니다. 화면의 속성을 참조하거나, 다른 화면과 비교하여 표시할 화면을 결정하는 데 사용할 수 있는 화면 개체를 반환합니다.  **[Back](function-navigate.md)** 또는 **[Navigate](function-navigate.md)** 함수를 사용하여 표시되는 화면을 변경할 수 있습니다. |

### <a name="compass"></a>나침반
**나침반** 신호는 화면 맨 위의 나침반 방향을 반환합니다. 방향은 자기장의 북쪽을 기준으로 합니다.

| 신호 속성 | 설명 |
| --- | --- |
| **Compass.Heading** |각도 단위의 방향입니다.  숫자 0~360을 반환하고 0이 북쪽입니다. |

### <a name="connection"></a>연결
**연결** 신호는 네트워크 연결 관련 정보를 반환합니다. 측정되는 연결에서 네트워크를 통해 보내거나 받는 데이터 크기를 제한하려 할 수 있습니다.

| 신호 속성 | 설명 |
| --- | --- |
| **Connection.Connected** |장치의 네트워크 연결 여부를 표시하는 부울 값 **true** 또는 **false**를 반환합니다. |
| **Connection.Metered** |연결의 측정 여부를 표시하는 부울 값 **true** 또는 **false**를 반환합니다. |

### <a name="location"></a>위치
**위치** 신호는 GPS(Global Positioning System) 기준 장치 위치와, 셀 타워 통신 및 IP 주소와 같은 기타 장치 정보를 반환합니다.

사용자가 처음으로 위치 정보에 액세스할 때 장치는 이 정보에 대한 액세스를 허용하라는 메시지를 사용자에게 표시할 수 있습니다.

위치가 바뀌면 해당 위치에 대한 종속성이 지속적으로 재계산되며 장치의 배터리에서 전력을 소비합니다. 배터리를 절약하기 위해 **[Enable](function-enable-disable.md)** 및 **[Disable](function-enable-disable.md)** 함수를 사용하여 위치 업데이트를 끄고 켤 수 있습니다. 표시되는 화면이 위치 정보에 종속되지 않은 경우 위치가 자동으로 꺼집니다.

| 신호 속성 | 설명 |
| --- | --- |
| **Location.Altitude** |피트 단위로 해발 고도를 표시하는 숫자를 반환합니다. |
| **Location.Latitude** |적도로부터 도 단위로 측정되는 경도를 나타내는 숫자 -90~90을 반환합니다.  양수 값이 적도 북쪽의 지역을 나타냅니다. |
| **Location.Longitude** |영국 그리니치로부터 도 단위로 측정되는 경도를 나타내는 숫자 0~180을 반환합니다.  |

## <a name="examples"></a>예
워싱턴 주 시애틀에 있는 사페코 필드 야구장에서 마운트에 있는 투수가 휴대전화를 홈 플레이트의 포수에게 던집니다. 전화는 그라운드에 평행하게 있다가 화면 위쪽이 포수를 향하고 포수가 회전을 더하지 않습니다. 이 위치에서 휴대전화에는 측정은 되지만 WiFi는 없는 셀룰러 네트워크 서비스가 있습니다. **PlayBall** 화면이 표시됩니다.   

| 수식 | 설명 | 결과 |
| --- | --- | --- |
| **Location.Latitude** |현재 위치의 위도를 반환합니다.  사페코 필드 야구장의 지도 좌표는 47.591 N, 122.333 W입니다. |47.591<br><br>전화가 투수와 포수 사이를 이동하는 동안 위도는 지속적으로 바뀝니다. |
| **Location.Longitude** |현재 위치의 경도를 반환합니다. |122.333<br><br>전화가 투수와 포수 사이를 이동하는 동안 경도는 지속적으로 바뀝니다. |
| **Location** |현재 위치의 위도 및 경도를 레코드로 반환합니다. |{&nbsp;Latitude:&nbsp;47.591, Longitude:&nbsp;122.333&nbsp;} |
| **Compass.Heading** |화면 맨 위의 나침반 방향을 반환합니다. 사페코 필드 경기장의 홈 플레이트는 대충 투수 마운트의 남서쪽에 있습니다. |230.25 |
| **Acceleration.X** |장치의 측면 방향 가속도를 반환합니다. 투수가 화면 맨위에 대해 직선 방향으로 휴대전화를 던지므로 장치에는 측면 방향 가속도가 없습니다. |0 |
| **Acceleration.Y** |장치의 전후 방향 가속도를 반환합니다. 투수가 처음에 장치를 던질 때는 장치에 높은 가속도가 부여되며 0.5초 안에 시간당 0에서 90마일(초당 132피트)로 가속됩니다. 장치가 공중에 오른 뒤 공기 마찰을 무시하고 장치는 더 이상 가속되지 않습니다. 포수가 장치를 잡을 때 장치가 가속이 줄어 멈추게 됩니다. |투수가 장치를 던지는 동안 8.2<br><br>장치가 공중에 있을 때 0<br><br>포수가 장치를 잡을 때 -8.2 |
| **Acceleration.Z** |장치의 상하 방향 가속도를 반환합니다. 공중에 있는 동안 장치는 중력의 영향을 받습니다. |투수가 장치를 던지기 전 0<br><br>장치가 공중에 있을 때 1<br><br>포수가 장치를 잡은 후 0 |
| **Acceleration** |가속을 레코드로 반환합니다. |투수가 장치를 던질 때 { X: 0, Y: 264, Z: 0}  |
| **Connection.Connected** |장치의 네트워크 연결 여부를 표시하는 부울 값을 반환합니다. |**true** |
| **Connection.Metered** |연결의 측정 여부를 표시하는 부울 값을 반환합니다. |**true** |
| **App.ActiveScreen = PlayBall** |**PlayBall** 표시 여부를 표시하는 부울 값을 반환합니다. |**true** |
| **App.ActiveScreen.Fill** |표시되는 화면의 배경색을 반환합니다. |**Color.Green** |

