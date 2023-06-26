---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서를 Adobe에 위임
description: 하위 도메인의 SSL 인증서를 Adobe에 위임하는 방법 알아보기
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0eefdbde25c955c84ee7534976256ca4df9a686c
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 25%

---

# 하위 도메인의 SSL 인증서를 Adobe에 위임 {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="하위 도메인의 SSL 인증서를 Adobe에 위임"
>abstract="컨트롤 패널을 사용하면 하위 도메인의 SSL 인증서를 Adobe에서 관리하도록 할 수 있습니다. CNAME을 사용하여 하위 도메인을 설정하는 경우, 도메인 호스팅 솔루션에 인증서를 생성하기 위해 인증서 레코드가 자동으로 생성되고 제공됩니다."

하위 도메인의 SSL 인증서를 Adobe으로 위임하는 것은 Adobe이 인증서를 자동으로 만들고 매년 인증서가 만료되기 전에 갱신하기 때문에 매우 좋습니다.

CNAME을 사용하여 하위 도메인 위임을 설정하는 경우 Adobe은 도메인 호스팅 솔루션에 사용할 인증서 레코드를 제공하여 인증서를 생성합니다.

새 하위 도메인을 설정할 때 또는 이미 위임된 하위 도메인에 대해 SSL 인증서의 Adobe 위임을 수행할 수 있습니다.

>[!NOTE]
>
>Adobe 관리 SSL은 무료 기능으로, 사용자라면 비용 없이 사용할 수 있습니다.

## 새 하위 도메인의 SSL 인증서 위임 {#new}

새 하위 도메인을 설정할 때 SSL 인증서를 위임하려면 **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** 하위 도메인 구성 마법사의 옵션입니다. 호스팅 솔루션으로 복사할 인증서 레코드는 나중에 구성 마법사에서 제공됩니다. 자세한 단계는에 설명되어 있습니다. [이 섹션](setting-up-new-subdomain.md).

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## 이미 위임된 하위 도메인에 대한 SSL 인증서 위임 {#delegated}

이미 위임된 하위 도메인에 대한 SSL 인증서를 위임하려면 원하는 하위 도메인 옆에 있는 줄임표 버튼을 클릭하고 **[!UICONTROL Switch to Managed SSL]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Adobe에서 자동으로 생성한 인증서 레코드가 포함된 대화 상자가 표시됩니다. 이러한 레코드를 하나씩 복사하거나 CSV 파일을 다운로드하여 복사한 다음 도메인 호스팅 솔루션으로 이동하여 일치하는 인증서를 생성합니다.

모든 인증서 레코드가 도메인 호스팅 솔루션에 생성되었는지 확인합니다. 모든 것이 올바르게 구성된 경우 레코드 생성을 확인한 다음 을 클릭합니다. **[!UICONTROL Submit]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
