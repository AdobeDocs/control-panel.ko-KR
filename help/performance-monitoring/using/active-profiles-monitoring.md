---
product: campaign
solution: Campaign
title: 활성 프로필 모니터링
description: 각 Campaign 인스턴스에 대한 최신 및 과거 활성 프로필 사용 및 진화에 대한 실시간 정보를 얻는 방법을 배웁니다.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 76%

---

# 활성 프로필 모니터링 {#active-profiles-monitoring}

## 활성 프로필 정보 {#about-active-profiles}

>[!IMPORTANT]
>
>컨트롤 패널의 활성 파일 모니터링은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다. Campaign Standard 10368 빌드에서 사용할 수 있습니다.

계약에 따라 각 캠페인 인스턴스에는 청구 용도로 계산되는 특정 양의 활성 프로필이 제공됩니다. 구입한 활성 프로필 수에 대한 자세한 내용은 최신 계약서를 참조하십시오.

&quot;프로필&quot;은 최종 고객, 잠재 고객 또는 리드를 나타내는 정보의 기록(예: 쿠키 ID, 고객 ID, 모바일 식별자 또는 특정 채널과 관련된 기타 정보가 포함된 외부 테이블 또는 nmsRecipient 테이블의 레코드)을 나타냅니다.

지난 12개월 동안 어느 채널을 통해 프로필을 타겟팅하거나 통신한 경우 프로필이 활성 상태로 간주됩니다.

>[!NOTE]
>
>페이스북과 트위터 채널은 고려되지 않습니다.

활성 프로필에 대한 자세한 내용은 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 및 [Campaign Classic v7](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 설명서를 참조하십시오.

## 활성 프로필 모니터링 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="활성 프로필 모니터링"
>abstract="이 탭에서는 각 Campaign 인스턴스에 대한 최신 및 과거 활성 프로필 사용 및 진화에 대한 실시간 정보를 얻을 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html" text="성능 모니터링"

컨트롤 패널을 사용하면 각 캠페인 인스턴스에 대한 활성 프로필 사용을 모니터링할 수 있습니다.

이렇게 하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Performance Monitoring]** 카드를 열고 **[!UICONTROL Active Profiles]** 탭을 선택합니다.

1. **[!UICONTROL Instance List]**&#x200B;에서 원하는 인스턴스를 선택합니다.

1. 인스턴스에 의해 사용된 활성 프로필 수와 인스턴스에서 청구 워크플로우를 마지막으로 실행한 시간도 표시됩니다.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>활성 프로필은 인스턴스에서 매일 실행되는 전용 기술 워크플로우를 기반으로 계산됩니다.
>
>* Campaign Standard를 위한 [&quot;청구&quot;](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html) 워크플로우
>* Campaign Classic에 대한 [&quot;활성 청구 프로필 수&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) 워크플로우입니다.


아래쪽 영역은 지난 30일 동안 활성 프로필 사용의 그래픽 표현을 제공합니다. 오른쪽 위 모서리의 사용 가능한 필터를 사용하여 표시된 기간을 1년으로 변경할 수 있습니다.

그래프 막대 중 하나를 마우스로 가리키면 선택한 기간에 사용된 정확한 활성 프로필 수를 가져올 수 있습니다.
