---
title: Excel 연결 개요 | Microsoft Docs
description: 클라우드 저장소 계정으로 통합 문서를 저장한 다음 앱에서 데이터에 연결하여 Excel로 데이터를 표시하고 업데이트할 수 있습니다.
services: ''
suite: powerapps
documentationcenter: na
author: archnair
manager: anneta
editor: ''
tags: ''
ms.service: powerapps
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/02/2016
ms.author: archanan
ms.openlocfilehash: d57d279670bf49c330b68a30bcd99a4578d3bbf9
ms.sourcegitcommit: 59785e9e82da8f5bd459dcb5da3d5c18064b0899
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/22/2018
---
# <a name="connect-to-excel-from-powerapps"></a>PowerApps에서 Excel에 연결
![Excel](./media/connection-excel/excelicon.png)

Excel은 *일종의* 연결입니다. 앱에서 Excel 데이터를 표시하려면 다음을 수행합니다.

1. [Excel 데이터를 표로 서식 지정](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-E81AA349-B006-4F8A-9806-5AF9DF0AC664)합니다.
2. Box, Dropbox, Google Drive, OneDrive 및 비즈니스용 OneDrive와 같은 클라우드 저장소 계정으로 Excel 파일을 저장합니다.
3. [클라우드 저장소 계정에 연결](../add-manage-connections.md)한 다음, 데이터 원본으로 Excel 테이블을 추가합니다.
4. [앱을 자동으로 생성](../get-started-create-from-data.md)하거나 **갤러리** 컨트롤 등을 추가하고 구성하여 앱에 이 정보를 표시합니다.

> [!NOTE]
> PowerApps에서 Excel 테이블에 연결하면, PowerApps는 Excel 테이블의 각 행에 고유한 ID가 있는 *\_*PowerAppsId_***라고 하는 새 열을 만듭니다.

[클라우드 저장소 연결 개요](cloud-storage-blob-connections.md)는 연결을 추가하고 Excel 표를 데이터 원본으로 저장하며 앱에서 Excel 데이터를 사용하는 방법을 보여줍니다.

다른 종류의 데이터에 연결하는 방법에 대한 자세한 내용은 [PowerApps 연결 목록](../connections-list.md)을 참조하십시오.

### <a name="known-limitations"></a>알려진 제한 사항
조직 내에서 Excel 데이터를 공유하는 방법에 대한 자세한 내용은 [이러한 제한 사항을 검토](cloud-storage-blob-connections.md#sharing-excel-tables)하세요.

