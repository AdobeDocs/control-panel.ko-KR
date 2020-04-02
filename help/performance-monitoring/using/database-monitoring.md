---
title: 데이터베이스 모니터링
description: 제어판에서 Campaign 데이터베이스를 모니터링하는 방법 알아보기
translation-type: tm+mt
source-git-commit: f995e0dc51fd95d00fdcaa2eb347b2aedfdef60d

---


# 데이터베이스 모니터링 {#database-monitoring}

## 인스턴스 데이터베이스 정보 {#about-instances-databases}

계약에 따라 각 Campaign 인스턴스에는 특정 양의 데이터베이스 공간이 제공됩니다.

데이터베이스에는 Adobe Campaign에 저장된 모든 **자산**, **워크플로우** 및 **데이터가** 포함됩니다.

시간이 지남에 따라, 특히 저장된 리소스가 인스턴스에서 삭제되지 않거나 일시 중지된 상태에 많은 워크플로우가 있는 경우 데이터베이스가 최대 용량에 도달할 수 있습니다.

인스턴스 데이터베이스를 넘치면 몇 가지 문제가 발생할 수 있습니다(로그인하지 못함, 이메일 전송 등). 따라서 인스턴스 데이터베이스를 모니터링하는 것은 최적의 성능을 보장하기 위해 필수적입니다.

>[!NOTE]
>
>현재 데이터베이스 공간 용량에 차이가 있을 수 있으며, 성능이 향상될 수 있도록 특정 기간 동안 계약에 지정된 양에 차이가 있을 수 있습니다.

## 데이터베이스 사용 모니터링 {#monitoring-instances-database}

1. 카드를 **[!UICONTROL Health Monitoring]** 열고 **[!UICONTROL Databases]** 탭을 선택합니다.

1. 에서 원하는 인스턴스를 **[!UICONTROL Instance List]**&#x200B;선택합니다.

   상단 영역은 인스턴스의 데이터베이스 용량 및 사용 공간에 대한 정보를 제공합니다.

   ![](assets/databases_dashboard.png)

   하위 영역은 지난 7일 동안 데이터베이스 사용률을 그래픽으로 표시합니다. 오른쪽 위 모서리에서 사용 가능한 필터를 사용하여 표시되는 기간을 변경할 수 있습니다.

   그래프 위로 마우스를 가져가면 선택한 기간에 대한 자세한 정보를 얻을 수 있습니다.

   ![](assets/databases_dashboard_detail.png)

## 데이터베이스 오버로드 방지 {#preventing-database-overload}

Campaign Standard 및 Classic에서는 데이터베이스 디스크 공간의 과소비를 방지하는 다양한 방법을 제공합니다.

아래 섹션에서는 데이터베이스 사용을 최적화하는 데 도움이 되는 Campaign 문서의 유용한 리소스를 제공합니다.

**워크플로우 모니터링**

* [워크플로우 우수 사례](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [워크플로우 실행](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) 모니터링(Campaign Classic)

**데이터베이스 유지 관리**

* 데이터베이스 정리 기술 워크플로우([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflowshtml#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [데이터베이스 유지 관리 안내서](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [데이터베이스 성능 문제 해결](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [데이터베이스 관련 옵션](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)