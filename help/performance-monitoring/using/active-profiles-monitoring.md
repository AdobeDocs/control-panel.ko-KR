---
title: 활성 프로파일 모니터링
description: 각 캠페인 인스턴스에 대한 최신 및 과거 활성 프로필 사용 및 진화에 대한 실시간 정보를 얻는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# 활성 프로파일 모니터링 {#active-profiles-monitoring}

>[!IMPORTANT]
>
>제어판에서 활성 프로파일 모니터링은 베타에서 제공되며 예고 없이 자주 업데이트하거나 수정할 수 있습니다.
>
>이 기능은 Campaign Standard 10368 빌드 및 Campaign Classic 8931 빌드에서 AWS에서 호스팅되는 고객이 사용할 수 있습니다. 이전 빌드를 사용하는 경우 이 기능을 사용하려면 업그레이드해야 합니다.

## 활성 프로필 정보 {#about-active-profiles}

계약에 따라 각 캠페인 인스턴스에는 청구 용도로 계산되는 특정 양의 활성 프로파일이 제공됩니다. 구입한 활성 프로필 수에 대한 자세한 내용은 최신 계약서를 참조하십시오.

&quot;프로필&quot;은 정보(예: 최종 고객, 잠재 고객 또는 리드를 나타내는 쿠키 ID, 고객 ID, 모바일 식별자 또는 특정 채널과 관련된 기타 정보가 포함된 외부 테이블 또는 nmsRecipient 테이블의 레코드

지난 12개월 동안 모든 채널을 통해 프로파일을 타깃팅하거나 커뮤니케이션한 경우 프로파일이 활성 상태로 간주됩니다.

>[!NOTE]
>
>페이스북과 트위터 채널은 고려되지 않는다.

활성 프로필에 대한 자세한 내용은 [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 및 [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 설명서를참조하십시오.

## 활성 프로파일 모니터링 {#monitoring-active-profiles}

제어판을 사용하면 각 캠페인 인스턴스에 대한 활성 프로필 사용을 모니터링할 수 있습니다.

이렇게 하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Performance Monitoring]** 카드를 열고 **[!UICONTROL Active Profiles]** 탭을 선택합니다.

1. 에서 원하는 인스턴스를 선택합니다 **[!UICONTROL Instance List]**.

1. 인스턴스에 의해 사용된 활성 프로필 수와 청구 워크플로우가 인스턴스에서 마지막으로 실행된 시간의 수가 표시됩니다.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>활성 프로파일은 매일 인스턴스 수를 기준으로 실행되는 전용 기술 워크플로우를 기반으로 계산됩니다.
>
>* Campaign Standard [의 &quot;청구](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) &quot; 워크플로우,
>* Campaign Classic [에 대한 &quot;활성 청구 프로필](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) 수&quot; 워크플로입니다.


아래쪽 영역은 지난 30일 동안 활성 프로파일 사용을 그래픽으로 표시합니다. 오른쪽 위 모서리의 사용 가능한 필터를 사용하여 표시된 기간을 1년으로 변경할 수 있습니다.

그래프 막대 중 하나를 마우스로 가리키면 선택한 기간에 사용된 정확한 활성 프로필 수를 가져올 수 있습니다.
