---
product: campaign
solution: Campaign
title: 데이터베이스 모니터링 정보
description: 컨트롤 패널에서 Campaign 데이터베이스를 모니터링하는 방법을 알아봅니다.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 데이터베이스 모니터링 정보 {#database-monitoring}

## 인스턴스 데이터베이스 정보 {#about-instances-databases}

계약에 따라 각 Campaign 인스턴스에는 특정 양의 데이터베이스 공간으로 프로비전됩니다. 데이터베이스에는 Adobe Campaign에 저장된 모든 **자산**, **워크플로** 및 **데이터**&#x200B;가 포함되어 있습니다.

시간이 지남에 따라, 특히 저장된 리소스를 인스턴스에서 삭제하지 않거나 일시 중지된 상태에 많은 워크플로가 있는 경우 데이터베이스가 최대 용량에 도달할 수 있습니다.

인스턴스 데이터베이스가 오버플로된 경우 문제(로그인, 이메일 보내기 불가 등)가 발생할 수 있습니다. 그러므로 최적의 성능을 보장하기 위해 인스턴스 데이터베이스를 모니터링하는 것이 필수입니다.

[이메일 경고](../../performance-monitoring/using/email-alerting.md)를 구독한 경우, 인스턴스의 데이터베이스 중 하나가 용량 80% 이상에 도달하면 이메일로 알림을 받게 됩니다.

## 데이터베이스 사용량 모니터링{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="데이터베이스 모니터링 정보"
>abstract="이 탭에서는 각 Campaign 인스턴스의 최신 및 과거 데이터베이스 사용량과 변화에 대하여 실시간으로 정보를 확인할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=ko" text="성능 모니터링 정보"

컨트롤 패널을 사용하면 각 캠페인 인스턴스에 대한 데이터베이스 사용량을 모니터링할 수 있습니다. 이렇게 하려면 **[!UICONTROL 성능 모니터링]** 카드를 연 다음 **[!UICONTROL 데이터베이스]** 탭을 선택하십시오.

**[!UICONTROL 인스턴스 목록]**&#x200B;에서 원하는 인스턴스를 선택하면 해당 인스턴스의 데이터베이스 용량 및 사용 공간에 대한 정보가 표시됩니다.

>[!NOTE]
>
>컨트롤 패널에 표시된 데이터베이스 공간의 양이 계약의 내용과 다른 경우 고객 지원 센터에 문의하십시오.

![](assets/databases_dashboard.png)

이 대시보드의 데이터는 Campaign 인스턴스에서 실행되는 **[!UICONTROL 데이터베이스 정리 기술 워크플로]**&#x200B;를 기반으로 업데이트됩니다([Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=ko#list-of-technical-workflows) 및 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=ko) 설명서 참조). **[!UICONTROL 사용된 공간]** 및 **[!UICONTROL 제공된 공간]** 메트릭 아래에서 워크플로가 마지막으로 실행된 시간을 확인할 수 있습니다. 워크플로가 3일 이상 실행된 적이 없는 경우, 워크플로가 실행 중이 아닌 이유를 조사할 수 있도록 Adobe 고객 지원 센터에 문의하는 것이 좋습니다.

이 대시보드에서 추가 메트릭을 사용하여 인스턴스의 데이터베이스 사용량을 분석할 수 있습니다. 이러한 내용은 다음 섹션에 자세히 설명되어 있습니다.

* [데이터베이스 사용률](../../performance-monitoring/using/database-utilization.md)
* [스토리지 개요](../../performance-monitoring/using/database-storage-overview.md)
* [상위 10개의 임시 리소스](../../performance-monitoring/using/database-top-ten-resources.md)
* [활성 쿼리](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) 이 비디오에서 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=ko#performance-monitoring) 또는 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=ko#performance-monitoring)를 사용하여 해당 기능 살펴보기
