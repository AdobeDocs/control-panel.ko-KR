---
product: campaign
solution: Campaign
title: TXT 레코드 관리
description: 도메인 소유권 확인을 위해 TXT 레코드를 관리하는 방법을 알아봅니다.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# TXT 레코드 시작 {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="TXT 레코드 관리"
>abstract="TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다. 컨트롤 패널을 사용하면 하위 도메인에 Google 사이트 확인, DMARC, BIMI 레코드의 세 가지 유형의 레코드를 추가할 수 있습니다."

## TXT 레코드 소개 {#about}

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다. 컨트롤 패널을 사용하면 하위 도메인에 세 가지 유형의 레코드를 추가할 수 있습니다.

* **Google TXT 레코드**&#x200B;를 사용하면 귀하가 도메인을 소유하고 있음을 증명하여 이메일의 받은 편지함 비율을 높이고 스팸 비율을 낮출 수 있습니다. [Google TXT 레코드를 추가하는 방법 알아보기](managing-txt-records.md)
* **DMARC 레코드**&#x200B;는 발신자의 도메인을 인증하고 악의적인 목적으로 도메인을 무단으로 사용하는 것을 방지하는 방법을 제공합니다. [DMARC 레코드를 추가하는 방법 알아보기](dmarc.md)
* **BIMI 레코드**&#x200B;를 사용하면 사서함 공급자의 받은 편지함에 있는 이메일 옆에 승인된 로고를 표시하여 브랜드 인지도와 신뢰도를 높일 수 있습니다. [BIMI 레코드를 추가하는 방법 알아보기](bimi.md)

## 하위 도메인의 레코드 모니터링 {#monitor}

하위 도메인의 세부 정보에 액세스하여 각 하위 도메인에 대해 추가된 모든 TXT 레코드를 모니터링할 수 있습니다.

이 화면에서는 선택한 하위 도메인의 모든 TXT 유형 레코드가 표시되고 구성에 있는 “값” 열에 정보가 표시됩니다. Google TXT, DMARC 또는 BIMI 레코드를 삭제하려면 줄임표 버튼을 클릭한 다음 삭제를 선택합니다. 필요한 경우 DMARC 및 BIMI 레코드를 편집할 수도 있습니다.

![](assets/txt-records.png)
