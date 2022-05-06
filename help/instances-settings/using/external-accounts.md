---
product: campaign
solution: Campaign
title: MID/RT 인스턴스 연결
description: MID/RT 인스턴스를 Campaign 컨트롤 패널에 연결하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---


# MID/RT 인스턴스 연결

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="하위 도메인 세부 사항"
>abstract="이 화면에서 하이브리드 호스팅 모델을 사용하는 고객은 Campaign 컨트롤 패널에서 특정 작업을 수행하기 위해 마케팅 인스턴스에 있는 MID/RT 인스턴스를 제공할 수 있습니다."

Campaign 컨트롤 패널을 사용하는 고객은 하이브리드 호스팅 모델을 사용하여 마케팅 인스턴스에 있는 MID/RT 인스턴스를 제공하여 Campaign 컨트롤 패널에서 특정 작업을 수행할 수 있습니다. 호스팅 모델에 대한 자세한 내용은 [Campaign Classic 설명서](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## MID/RT 인스턴스 연결 {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="하위 도메인 세부 사항"
>abstract="클라이언트 콘솔에서 마케팅 인스턴스에 MID/RT 인스턴스를 추가하는 데 사용되는 연산자의 ID입니다."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="하위 도메인 세부 사항"
>abstract="마케팅 인스턴스에서 MID/RT 인스턴스를 추가하기 위해 클라이언트 콘솔에 사용되는 연산자의 암호입니다."

Campaign 컨트롤 패널에서 MID/RT 인스턴스를 제공하려면 다음 단계를 수행합니다.

1. 에서 **[!UICONTROL Instances Settings]** 카드를 선택한 다음 **[!UICONTROL External Accounts]** 탭.

1. 드롭다운 목록에서 마케팅 인스턴스를 선택하고 **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. 연결할 MID/RT 인스턴스에 대한 정보를 제공합니다.
   * **[!UICONTROL URL]**: 인스턴스의 URL,
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: 마케팅 인스턴스에서 MID/RT 인스턴스를 추가하기 위해 클라이언트 콘솔에 사용되는 연산자의 자격 증명입니다.

   ![](assets/external-account-add.png)

1. 클릭 **[!UICONTROL Save]** 확인합니다.

이제 인스턴스가 Campaign 컨트롤 패널에 연결됩니다. 목록에서 연결을 선택하여 언제든지 연결을 제거하거나 비활성화할 수 있습니다.

![](assets/external-account-edit.png)

## MID/RT 인스턴스에 사용 가능한 기능 {#capabilities}

MID/RT 인스턴스가 Campaign 컨트롤 패널에 연결되면 아래 나열된 기능을 활용하여 모니터링할 수 있습니다.

* [인스턴스 세부 사항 보기](../../instances-settings/using/instance-details.md),
* [허용 목록에 IP 주소를 추가하여 인스턴스에 액세스합니다](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [위임된 하위 도메인에 대한 정보 보기](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [SSL 인증서에 대한 정보 보기](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
