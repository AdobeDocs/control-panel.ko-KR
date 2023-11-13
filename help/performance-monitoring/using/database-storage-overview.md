---
product: campaign
solution: Campaign
title: 스토리지 개요
description: 컨트롤 패널에서 인스턴스의 데이터베이스 공간을 사용하는 다양한 Campaign 리소스를 모니터링하는 방법을 알아봅니다.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '175'
ht-degree: 100%

---

# 스토리지 개요 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="저장소 개요 정보"
>abstract="이 탭에서는 데이터베이스 공간을 사용하는 다양한 Campaign 리소스에 대하여 자세한 정보를 확인할 수 있습니다."

**[!UICONTROL 스토리지 개요]** 영역은 다음이 차지하는 공간을 그래픽으로 보여줍니다.

* **[!UICONTROL 시스템 리소스]**

  데이터베이스 공간에서 시스템 리소스로 용량이 많이 사용되는 경우 고객 지원 센터에 문의하십시오.

* Campaign 인스턴스와 함께 기본적으로 제공되는 **[!UICONTROL 기본 테이블]**,
* 워크플로우 및 게재로 생성된 **[!UICONTROL 임시 테이블]**,
* 사용자 정의 리소스 생성 후 생성된 **[!UICONTROL 기본 제공이 아닌 테이블]**.

![](assets/database-storage-overview.png)

데이터베이스 공간을 소비하는 다양한 에셋에 대한 자세한 내용을 보려면 **[!UICONTROL 세부 사항 보기]** 버튼을 클릭합니다.

드롭다운 목록을 사용하여 특정 에셋 유형(워크플로우, 게재, 수신자)에서만 검색 및 표시 테이블을 검색할 수 있습니다.

![](assets/database-storage-details.png)

이 화면에서는 인스턴스의 문제를 방지하기 위해 특정 주의가 필요한 워크플로우 매개 변수를 모니터링할 수도 있습니다. [이 페이지](workflow-monitoring.md)에서 자세히 알아보십시오.
