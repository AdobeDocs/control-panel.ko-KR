---
product: campaign
solution: Campaign
title: 주요 연락처 및 이벤트 모니터링
description: Adobe 인스턴스 및 주요 연락처에서 발생하는 이벤트를 식별하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: ht
source-wordcount: '497'
ht-degree: 100%

---

# 주요 연락처 및 이벤트 모니터링 {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="서비스 캘린더"
>abstract="주요 연락처 섹션에는 Adobe에서 인스턴스에 대한 요청이나 문제에 대해 연락할 수 있는 사람이 나열됩니다. 서비스 이벤트 캘린더 섹션에서 선택한 인스턴스에 대한 릴리스 및 서비스 검토를 식별하고 예정된 이벤트에 대한 미리 알림을 설정할 수 있습니다."

>[!IMPORTANT]
>
>서비스 캘린더는 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

Campaign 인스턴스를 모니터링하려면 인스턴스에서 계획된 이벤트를 확인해야 합니다.

Campaign 컨트롤 패널을 사용하면 인스턴스에서 발생하는 릴리스 및 서비스 검토를 모니터링하고 요청 또는 문제에 관해 Adobe의 주요 연락처 목록에 액세스할 수 있습니다.

이러한 정보는 Campaign 컨트롤 패널 홈페이지의 **[!UICONTROL Service Calendar]** 카드에서 액세스할 수 있습니다.

## 주요 연락처 {#key-contacts}

**[!UICONTROL Key contacts]** 섹션에는 인스턴스 관련 요청이나 문제에 대해 연락할 수 있는 Adobe 직원 목록이 있습니다.

>[!NOTE]
>
>이 섹션에는 Managed Service 계정에 대한 정보만 표시됩니다.

![](assets/service-events-contacts.png)

주요 연락처에는 다음 역할이 포함됩니다.

* **[!UICONTROL TAM]**: 기술 계정 관리자,
* **[!UICONTROL CSM]**: 고객 성공 관리자,
* **[!UICONTROL Deliverability]**: 게재 작업 담당자,
* **[!UICONTROL Transition Manager]**: Managed Service 전환 관리자(Managed Service 계정만 해당),
* **[!UICONTROL On-boarding Specialist]**: Campaign Classic 온보딩을 지원하기 위해 계정에 배정된 전문가(Managed Services 계정만 해당).

## 이벤트 {#events}

### 이벤트 모니터링 {#monitor-events}

**[!UICONTROL Service Event Calendar]** 섹션에는 선택한 인스턴스에 대해 과거 및 예정된 릴리스 및 서비스 검토가 모두 표시됩니다.

![](assets/service-events-calendar.png)

**[!UICONTROL Note]** 열은 각 릴리스의 상태에 대한 정보를 제공합니다.

* **[!UICONTROL General availability]**: 사용 가능한 안정적인 최신 빌드.
* **[!UICONTROL Limited availability]**: 주문형 배포만 가능.
* **[!UICONTROL Release candidate]**: 엔지니어링 유효성 검사. 프로덕션 교정을 기다리는 중입니다.
* **[!UICONTROL Pre release]**: 특정한 고객 요구에 대한 사전 가용성.
* **[!UICONTROL No longer available]**: 빌드에 중요한 문제가 없지만 버그가 추가로 수정된 새 빌드를 사용할 수 있습니다. 업그레이드가 필요합니다.
* **[!UICONTROL Deprecated]**: 알려진 회귀가 포함된 빌드.
빌드는 더 이상 지원되지 않습니다. 업그레이드는 필수입니다.

예정된 하나 또는 여러 이벤트에 플래그를 할당하여 추적할 수 있습니다. 이렇게 하려면 이벤트 이름 옆에 있는 타원형 버튼을 클릭하십시오.

![](assets/service-events-flag.png)

### 미리 알림 설정 {#reminders}

서비스 캘린더를 사용하면 이벤트가 발생하기 전에 이메일로 알림을 받기 위해 미리 알림을 설정할 수 있습니다.

>[!NOTE]
>
>예정된 이벤트에 대한 알림을 받으려면 Campaign 컨트롤 패널에서 이메일 경고를 구독했는지 확인하십시오. [자세히 알아보기](../performance-monitoring/using/email-alerting.md)

이벤트에 대한 경고를 설정하려면 다음 단계를 수행합니다.

1. 알림을 받을 이벤트 옆에 있는 타원 버튼을 클릭한 다음 **[!UICONTROL Set Reminder]** 아이콘을 선택합니다.

1. 미리 알림의 제목을 지정한 다음, 이벤트가 발생하기 전에 알림을 받을 날짜를 선택합니다.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Campaign 컨트롤 패널 경고를 구독하지 않은 경우 메시지가 표시되며, 등록하여 이메일 알림을 받을 수 있습니다.

1. 이제 선택한 이벤트에 대해 미리 알림이 설정됩니다. 언제든지 마우스로 제목을 표시할 수 있습니다.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >동일한 이벤트에 대해 최대 2개의 미리 알림을 설정할 수 있습니다.

1. 미리 알림에 지정된 날짜에 예정된 이벤트에 대해 알리는 이메일이 전송되며 미리 알림은 자동으로 서비스 달력 메뉴의 **[!UICONTROL Reminders]** 카운트에서 제거됩니다.
