---
product: campaign
solution: Campaign
title: 상위 10개의 임시 리소스
description: Campaign 데이터베이스의 워크플로우 및 게재에서 생성된 가장 큰 10개의 임시 리소스를 Campaign 컨트롤 패널에서 모니터링하는 방법을 알아봅니다.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# 상위 10개의 임시 리소스 {#top-10}

**[!UICONTROL Top 10 temporary resources]** 영역에는 워크플로우 및 게재로 생성된 가장 큰 10개의 임시 리소스가 나열됩니다.

대규모 임시 리소스를 생성하는 워크플로우 및 게재 모니터링은 데이터베이스를 모니터링하는 중요한 단계입니다. 임시 리소스가 너무 많은 데이터베이스 공간을 사용하는 경우, 해당 워크플로우나 게재가 필요한지 확인하고, 해당 인스턴스로 이동하여 중지해야 합니다.

>[!IMPORTANT]
>
>일반적으로 **40개 이상의 열**&#x200B;이 기본 제공 리소스가 아닌 곳에 있는 상황을 피하는 것이 좋습니다. 워크플로우에 테이블 수가 많거나 데이터베이스 크기가 큰 경우, 워크플로우를 검토하여 너무 많은 데이터를 생성하는 이유를 조사하는 것이 좋습니다.
>
>Campaign Standard 및 Classic 지침도 제공됩니다. [이 페이지](database-preventing-overload.md) 데이터베이스 오버로드를 방지하기 위해

![](assets/database-top10.png)

다음 **[!UICONTROL View all]** 버튼을 사용하여 **[!UICONTROL Storage overview]** 이러한 임시 리소스에 대한 자세한 정보를 얻을 수 있습니다. 자세한 정보는 이 [페이지](database-storage-overview.md)를 참조하십시오.
