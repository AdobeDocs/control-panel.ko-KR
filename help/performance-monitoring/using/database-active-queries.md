---
product: campaign
solution: Campaign
title: 활성 쿼리 모니터링
description: Campaign 컨트롤 패널의 Campaign 인스턴스에서 활성 쿼리를 모니터링하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 50%

---

# 활성 쿼리 모니터링 {#long-running-queries}

다음 **[!UICONTROL Databases]** 탭의 **[!UICONTROL Active queries]** 영역에는 선택한 인스턴스에서 가장 오랫동안 실행되는 5개의 쿼리가 나열됩니다.

![](assets/active-queries.png)

다음 **[!UICONTROL Duration]** 열은 인스턴스에서 쿼리가 실행되는 시간을 지정합니다. 기간은 `hh:mm:ss.ms` 형식으로 표시됩니다.

>[!IMPORTANT]
>
>쿼리 중 하나가 24시간 이상 활성 상태인 경우, 을 구독하면 전자 메일로 알림을 받게 됩니다 [이메일 경고](email-alerting.md).
>
>이 경우 문제를 식별하고 해결하도록 고객 지원 센터에 문의하십시오. 이 사용자에게 **[!UICONTROL PID]** 열 값 - 쿼리의 고유 식별자입니다.
