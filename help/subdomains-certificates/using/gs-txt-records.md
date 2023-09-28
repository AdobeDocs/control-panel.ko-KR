---
product: campaign
solution: Campaign
title: TXT 레코드 관리
description: 도메인 소유권 확인을 위해 TXT 레코드를 관리하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# TXT 레코드 시작 {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="TXT 레코드 관리"
>abstract="TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다. Campaign 컨트롤 패널을 사용하면 하위 도메인에 Google 사이트 확인, DMARC 및 BIMI 레코드의 세 가지 유형의 레코드를 추가할 수 있습니다."

## TXT 레코드 {#about}

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다. Campaign 컨트롤 패널을 사용하면 하위 도메인에 세 가지 유형의 레코드를 추가할 수 있습니다.

* **Google 레코드** 을 사용하면 이메일의 받은 편지함 비율을 높이고 스팸 비율을 낮추어 자신이 도메인을 소유하고 있음을 입증할 수 있습니다. [Google TXT 레코드를 추가하는 방법 알아보기](managing-txt-records.md)
* **레코드** 보낸 사람의 도메인을 인증하고 악의적인 목적으로 도메인을 승인하지 않고 사용하지 않도록 하는 방법을 제공합니다. [DMARC 레코드를 추가하는 방법 알아보기](dmarc.md)
* **BIMI 레코드** 사서함 공급자의 받은 편지함에 전자 메일 옆에 승인된 로고를 표시하여 브랜드 인지도와 신뢰를 높일 수 있습니다. [BIMI 레코드를 추가하는 방법 알아보기](bimi.md)

## 하위 도메인의 레코드 모니터링 {#monitor}

하위 도메인의 세부 정보에 액세스하여 각 하위 도메인에 대해 추가된 모든 TXT 레코드를 모니터링할 수 있습니다.

이 화면에서는 선택한 하위 도메인의 모든 TXT 유형 레코드가 표시되고 구성에 있는 &quot;값&quot; 열에 정보가 표시됩니다. Google TXT, DMARC 또는 BIMI 레코드를 삭제하려면 줄임표 버튼을 클릭한 다음 삭제를 선택합니다. 필요한 경우 DMARC 및 BIMI 레코드를 편집할 수도 있습니다.

![](assets/txt-records.png)
