---
product: campaign
solution: Campaign
title: 컨트롤 패널 액세스
description: 컨트롤 패널에 액세스하는 방법 알아보기
feature: Control Panel, Access Management
role: Admin
level: Experienced
exl-id: eb67af6e-a64e-49a7-9656-782f91bc1d67
source-git-commit: 2ee542f43c75d9645681228dea10c1d7ede63c23
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 83%

---

# 컨트롤 패널 액세스 {#accessing-control-panel}

컨트롤 패널은 Experience Cloud에서 직접 사용하거나 제품 자체에서 사용할 수 있습니다.

## 필수 구성 요소 {#prerequisites}

Campaign v7/v8의 경우 인스턴스를 AWS(Amazon Web Services)에서 호스팅하고 [Campaign의 안정적인 최신 빌드](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=ko#rn-statuses) 또는 빌드 9032 이상으로 업그레이드해야 합니다. [이 섹션](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=ko#getting-your-campaign-version)에서 사용 중인 버전을 확인하는 방법을 알아봅니다. 인스턴스가 AWS에서 호스팅되는지 확인하려면 [이 페이지](../../faq.md#hosted-aws)에 설명된 단계를 수행합니다.

Microsoft Azure에서 호스팅되는 Campaign v8 인스턴스도 Campaign 컨트롤 패널 기능의 하위 집합에 액세스할 수 있습니다. [인스턴스 액세스에 대한 IP 허용 목록](../../instances-settings/using/ip-allow-listing-instance-access.md), [SFTP 서버에 대한 IP 허용 목록](../../sftp/using/ip-range-allow-listing.md) 및 [고객 관리 SSL 인증서 관리](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>기본적으로 컨트롤 패널에는 &quot;관리자&quot; 제품 프로필에 속하는 관리자 사용자가 액세스할 수 있습니다. 조직 구성에 따라 제품 프로필의 이름을 다르게 지정할 수 있습니다(&quot;admin&quot;, &quot;admins&quot;, &quot;approval admin&quot; 등). **이름에 &quot;admin&quot;이라는 단어가 포함된 모든 제품 프로필은 자동으로 Campaign 컨트롤 패널에게 액세스 권한을 부여합니다**. 권한이 있는 사용자만 컨트롤 패널에 액세스하도록 하기 위해 Admin Console에서 제품 프로필 이름을 주의 깊게 검토해야 합니다. [Campaign 컨트롤 패널에 대한 권한을 관리하는 방법을 알아보세요](../../discover/using/managing-permissions.md).

## Experience Cloud 플랫폼에서 액세스 {#access-experience-cloud-platform}

Adobe Experience Cloud 플랫폼에서 컨트롤 패널에 액세스하려면 아래 단계를 따르십시오.

1. [Experience Cloud 홈페이지](https://experiencecloud.adobe.com/){target="_blank"}로 이동합니다.

1. **빠른 액세스** 섹션에서 전용 링크를 클릭합니다.

   ![](assets/do-not-localize/quickaccess.png)

컨트롤 패널은 Experience Cloud Platform **솔루션 선택기**&#x200B;에서도 액세스할 수 있습니다.

1. [Adobe Experience Cloud 홈페이지](https://experiencecloud.adobe.com/){target="_blank"}의 **바로 가기** 섹션 또는 오른쪽 상단 메뉴에서 **Campaign**&#x200B;을 선택합니다.

   ![](assets/do-not-localize/control_panel_access1.png)

1. Campaign 인스턴스 목록이 표시됩니다. **컨트롤 패널** 카드를 클릭하여 실행합니다.

   ![](assets/do-not-localize/control_panel_access2.png)

## 제품에서 액세스 {#access-product}

>[!NOTE]
>
>제품 내 액세스는 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=ko){target="_blank"}에서만 가능합니다.

1. Campaign Standard 제품을 엽니다.

1. **탐색** 창에서 **[!UICONTROL 관리]** 메뉴를 선택합니다.

   ![](assets/control_panel_access3.png)

1. **[!UICONTROL 컨트롤 패널]** 아이콘을 클릭합니다.

   ![](assets/control_panel_access4.png)
