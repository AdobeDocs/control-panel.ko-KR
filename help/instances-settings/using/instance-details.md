---
product: campaign
solution: Campaign
title: 인스턴스 세부 사항
description: 컨트롤 패널에서 인스턴스 세부 사항을 모니터링하는 방법 알아보기
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 100%

---

# 인스턴스 세부 사항 {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="인스턴스 세부 사항 정보"
>abstract="유형, 이름, 빌드 정보, 가능한 업그레이드 관련 권장 사항 등 Adobe Campaign 인스턴스의 세부 사항 보여줍니다."

## 인스턴스 세부 사항 정보 {#about-instance-details}

>[!IMPORTANT]
>
>능이 기능은 Campaign v7/v8 인스턴스에서만 사용할 수 있습니다.

마케팅 활동을 유동적으로 진행하기 위해 Adobe Campaign 인스턴스 아키텍처에 서버를 여러 개 포함할 수 있습니다. 예를 들어 인스턴스를 지원하는 마케팅, 실시간/메시지 센터 및 중간 소싱 서버를 포함할 수 있습니다.

인스턴스 세부 사항 기능을 사용하면 인스턴스의 단순 아키텍처를 확인할 수 있습니다. 또한 서버 정보 외에 인스턴스 빌드가 최신 상태인지 여부도 확인할 수 있으며, 필요 시에는 업그레이드 권장 메시지도 표시됩니다.

>[!NOTE]
>
>성능 저하를 방지하고 Adobe Campaign v7/v8이 제공하는 최신 기능과 수정 사항을 활용할 수 있도록 인스턴스를 1년에 한 번 이상 업그레이드하는 것이 좋습니다.

**관련 항목:**

* [빌드 업그레이드 수행](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=ko)
* [Adobe Campaign 업데이트](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/introduction.html?lang=ko)

## 인스턴스 관련 정보 검색 {#retrieving-information-about-instances}

인스턴스에 연결된 서버 관련 정보를 확인하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 인스턴스 설정]** 카드를 열어 **[!UICONTROL 인스턴스 세부 사항]** 탭에 액세스합니다.

   >[!NOTE]
   >
   >컨트롤 패널 홈 페이지에 인스턴스 설정 카드가 표시되지 않으면 조직 ID가 Adobe Campaign v7/v8 인스턴스와 연결되어 있지 않은 것입니다.

1. 왼쪽 창에서 원하는 Campaign 인스턴스를 선택합니다.

   >[!NOTE]
   >
   >모든 Campaign 인스턴스가 왼쪽 창 목록에 표시됩니다. 인스턴스 세부 사항 기능은 Campaign v7/v8 인스턴스 전용이므로 Campaign Standard 인스턴스를 선택하면 “미해당 인스턴스” 메시지가 표시됩니다.

1. 인스턴스에 연결된 서버가 표시됩니다.

   ![](assets/instance_details.png)

제공되는 정보는 다음과 같습니다.

* **[!UICONTROL 유형]**: 서버 유형입니다. 가능한 값은 MKT(마케팅), MID(중간 소싱), RT(메시지 센터/실시간 메시징)입니다.
* **[!UICONTROL 이름]**: 서버의 이름입니다.
* **[!UICONTROL 빌드:]** 서버에 설치된 빌드 버전.
* **[!UICONTROL 업그레이드 정보]**: 이 열은 서버에 업데이트가 필요한지 알려줍니다.
   * 녹색: 서버가 최신 상태이므로 업그레이드할 필요가 없습니다.
   * 노랑: 업그레이드를 고려해야 합니다. 최신 기능과 수정 사항이 설치되어 있지 않습니다.
   * 빨강: 최대한 빨리 업그레이드해야 합니다. 새 기능이 설치되어 있지 않아 서버 성능이 최적 상태가 아닐 수 있습니다.

서버 중 하나를 업그레이드해야 하는 경우의 진행 방법에 대한 자세한 내용은 [이 설명서](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=ko)를 참조하십시오.

## 일반적인 질문 {#common-questions}

**인스턴스 아키텍처에 MID 서버가 표시되지 않으면 인스턴스가 정상 작동하지 않는 것입니까? 현재 특정 작업을 수행할 수 없다면 RT 인스턴스가 필요합니까?**

인스턴스는 상황에 따라 일부 서버 유형만 포함할 수도 있고 같은 서버를 여러 개 포함할 수도 있습니다. 특정 서버 유형이 포함되어 있지 않다고 해서 실시간 메시지를 전송할 수 없거나 기타 유형의 활동을 수행할 수 없는 것은 아닙니다. 이러한 경우에는 추가 서버 용량을 요청할 수 있습니다(추가 비용이 부과됨).

일부 서버가 &quot;인스턴스 세부 사항&quot; 페이지에 표시되지 않는 경우 고객 지원 센터에 문의하십시오. 메시지에 해당 인스턴스의 URL을 구체적으로 기입해야 합니다.
