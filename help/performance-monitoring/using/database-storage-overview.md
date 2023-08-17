---
product: campaign
solution: Campaign
title: 스토리지 개요
description: Campaign 컨트롤 패널에서 인스턴스의 데이터베이스 공간을 사용하는 다양한 Campaign 리소스를 모니터링하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# 스토리지 개요 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="저장소 개요 정보"
>abstract="이 탭에서는 데이터베이스 공간을 사용하는 다양한 Campaign 리소스에 대하여 자세한 정보를 확인할 수 있습니다."

**[!UICONTROL Storage overview]** 영역은 다음과 같이 사용자가 사용 중인 공간을 그래픽으로 표시합니다.

* **[!UICONTROL System resources]**

  데이터베이스 공간에서 시스템 리소스로 용량이 많이 사용되는 경우 고객 지원 센터에 문의하십시오.

* 기본적으로 Campaign 인스턴스와 함께 제공되는 **[!UICONTROL Out-of-the-box tables]**,
* 워크플로우 및 게재별로 작성된 **[!UICONTROL Temporary tables]**,
* 사용자 지정 리소스를 만든 후 생성된 **[!UICONTROL Non-out of the box tables]**.

![](assets/database-storage-overview.png)

데이터베이스 공간을 사용하는 다른 자산에 대한 자세한 내용을 보려면 **[!UICONTROL View details]** 단추를 클릭합니다.

드롭다운 목록을 사용하여 특정 에셋 유형(워크플로우, 게재, 수신자)에서만 검색 및 표시 테이블을 검색할 수 있습니다.

![](assets/database-storage-details.png)

이 화면에서는 인스턴스의 문제를 방지하기 위해 특정 주의가 필요한 워크플로우 매개 변수를 모니터링할 수도 있습니다. [이 페이지](workflow-monitoring.md)에서 자세히 알아보십시오.
