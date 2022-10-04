---
product: campaign
solution: Campaign
title: MID/RT 인스턴스 추가(하이브리드 모델)
description: 하이브리드 호스팅 모델을 사용하여 컨트롤 패널에 MID/RT 인스턴스를 추가하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: ff64acbe-d8cb-499b-b20f-b0934fb0f695
source-git-commit: c834ae7226ed9dd1f78d4f4511b52cb5f04abfae
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# MID/RT 인스턴스 추가(하이브리드 모델){#add-mid-rt-instances-hybrid-model}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="외부 계정"
>abstract="이 화면에서 하이브리드 호스팅 모델을 사용하는 고객은 컨트롤 패널 기능을 활용하기 위해 컨트롤 패널의 마케팅 인스턴스에 구성된 MID/RT 인스턴스 URL을 제공할 수 있습니다."

컨트롤 패널을 통해 하이브리드 호스팅 모델을 사용하는 고객은 특정 컨트롤 패널 기능을 활용할 수 있습니다. 이를 위해 컨트롤 패널의 마케팅 인스턴스에 구성된 MID/RT 인스턴스 URL을 제공해야 합니다.

호스팅 모델에 대한 자세한 내용은 [Campaign Classic 설명서](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html?lang=ko)를 참조하십시오.

## MID/RT 인스턴스 추가 {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="인스턴스의 URL입니다. 이 URL은 관리 > 플랫폼 > 외부 계정 메뉴의 Campaign 클라이언트 콘솔에 있습니다."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="운영자"
>abstract="Adobe 관리자가 초기 프로비저닝 후 제공한 운영자의 ID입니다."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="암호"
>abstract="Adobe 관리자가 초기 프로비저닝 후 제공한 운영자의 암호입니다."

하이브리드 고객은 Experience Cloud를 통해 컨트롤 패널에 연결해야 합니다. 처음으로 컨트롤 패널에 액세스할 때 홈 페이지에는 카드가 두 개만 표시됩니다.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>컨트롤 패널에 액세스하는 데 문제가 발생하면 마케팅 인스턴스가 [조직 ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=ko). 이 설정을 완료하고 계속 진행하려면 고객 지원 센터에 문의하십시오. 연결에 성공하면 컨트롤 패널 홈 페이지가 표시됩니다.

컨트롤 패널 기능에 액세스하려면 **[!UICONTROL Instances Settings]** 카드에 MID/RT 인스턴스 정보를 제공해야 합니다. 이렇게 하려면 아래 단계를 수행합니다.

1. **[!UICONTROL Instances Settings]** 카드에서 **[!UICONTROL External Accounts]** 탭을 선택합니다.

1. 드롭다운 목록에서 원하는 마케팅 인스턴스를 선택하고 **[!UICONTROL Add new URL]**&#x200B;을(를) 클릭합니다.

   ![](assets/external-account-addbutton.png)

1. 추가할 MID/RT 인스턴스에 대한 정보를 제공합니다.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: 인스턴스의 URL입니다. **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** 메뉴의 Campaign 클라이언트 콘솔에 있습니다.

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Adobe 관리자가 초기 프로비저닝 후 제공한 운영자의 자격 증명입니다.

      >[!NOTE]
      >
      >이러한 세부 사항을 사용할 수 없는 경우 고객 지원 센터에 문의하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭하여 확인합니다.

MID/RT URL을 추가할 때 URL의 정확성을 확인하기 위해 비동기 프로세스가 트리거됩니다. 이 작업은 몇 분 정도 걸릴 수 있습니다. MID/RT 인스턴스 URL의 유효성을 검사할 때까지 작업이 보류 상태로 유지됩니다. 유효성 검사가 완료되면 컨트롤 패널 기본 기능에 액세스할 수 있습니다.

![](assets/external-account-pending.png)

목록에서 MID/RT 인스턴스 URL을 선택하여 언제든지 제거하거나 비활성화할 수 있습니다.

![](assets/external-account-edit.png)

**[!UICONTROL External Accounts]** 탭에서 수행되는 모든 작업을 **[!UICONTROL Job Logs]**&#x200B;의 MID/RT 인스턴스 URL에서 모니터링할 수 있습니다.

![](assets/external-account-logs.png)

## 하이브리드 고객이 사용할 수 있는 기능 {#capabilities}

MID/RT 인스턴스가 컨트롤 패널에 추가되면 아래 나열된 기능을 활용할 수 있습니다.

* [주요 연락처 및 이벤트 모니터링](../../service-events/service-events.md)
* [인스턴스 세부 사항 보기](../../instances-settings/using/instance-details.md),
* [허용 목록에 IP 주소 추가](../../instances-settings/using/ip-allow-listing-instance-access.md)(RT 인스턴스용),
* [새 하위 도메인 설정](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [하위 도메인의 SSL 인증서 갱신](../../subdomains-certificates/using/renewing-subdomain-certificate.md).
