---
product: campaign
solution: Campaign
title: 컨트롤 패널 FAQ
description: 컨트롤 패널 관련 일반적인 질문
feature: Control Panel
role: Admin
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 98cf425548884c3a5e503c35ce5ea5b7ceaee67f
workflow-type: ht
source-wordcount: '719'
ht-degree: 100%

---

# FAQ(자주 묻는 질문) {#faq}

## 컨트롤 패널 {#control-panel}

### 컨트롤 패널이란 무엇인가요?

컨트롤 패널은 제품 관리자가 Adobe Campaign에 연결된 SFTP 서버의 용량을 모니터링하고 다양한 설정을 직접 관리할 수 있는 구성 요소입니다.

### 컨트롤 패널의 기능에는 어떤 것이 있나요?

컨트롤 패널에서는 스토리지 추적, 허용 목록에 IP 추가, 요구에 따라 SFTP 서버용 SSH 키 직접 관리 등의 작업을 수행할 수 있습니다.

자세한 내용은 컨트롤 패널에서 지원되는 작업 설명서를 참조하십시오.

### Campaign v8에서 아직 지원하지 않지만 Campaign Classic v7에서는 사용할 수 있는 기능이 있나요?{#v8-restrictions}

아니요. 이제 [하위 도메인] 및 [인증서 관리] 관련 기능 등 Campaign v7에서 사용할 수 있는 기능도 모두 Campaign v8의 [컨트롤 패널]을 통해 지원됩니다.

### 컨트롤 패널은 Adobe Campaign 전용인가요?

예. 컨트롤 패널에서는 Adobe Campaign의 설정만 관리할 수 있습니다.

### 컨트롤 패널을 사용하기 위한 자격이 있나요?

AWS에서 Adobe Campaign을 호스팅하는 현재 Adobe 고객의 제품 관리자만 컨트롤 패널을 열 수 있습니다.

컨트롤 패널을 통해 하이브리드 호스팅 모델을 사용하는 고객은 특정 컨트롤 패널 기능을 활용할 수 있습니다. 이를 위해 컨트롤 패널의 마케팅 인스턴스에 구성된 MID/RT 인스턴스 URL을 제공해야 합니다. [자세히 알아보기](instances-settings/using/external-accounts.md)

관리자가 아닌데 컨트롤 패널에 액세스하려는 경우에는 제품 관리자에게 연락하여 자신을 관리자로 추가해 줄 것을 요청해야 합니다.

### Campaign Classic v7 사용자가 컨트롤 패널에 액세스하기 위한 조건이 있나요? {#v7-restrictions}

컨트롤 패널은 관리 사용자만 액세스할 수 있습니다. [자세히 알아보기](discover/using/managing-permissions.md)

Campaign v7의 경우 인스턴스를 AWS(Amazon Web Services)에서 호스팅하고 [Campaign의 안정적인 최신 빌드](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=ko#rn-statuses) 또는 빌드 9032 이상으로 업그레이드해야 합니다. 사용 중인 Campaign Classic v7의 버전을 확인하는 방법은 [이 섹션](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=ko#getting-your-campaign-version)에서 알아볼 수 있습니다. 사용하는 Campaign Classic 인스턴스가 AWS에서 호스팅되는지 확인하는 단계는 [이 섹션](#hosted-aws)에서 자세히 설명하고 있습니다.

### 컨트롤 패널에는 어떻게 액세스할 수 있나요?

컨트롤 패널 액세스 설명서의 자세한 지침을 따라 액세스합니다.

### 컨트롤 패널 사용 시 추가 요금이 부과되나요?

아니요. 현재 Adobe Campaign의 고객인 경우 추가 비용은 없습니다.

## 조직 ID {#ims-org-id}

### 조직 ID란 무엇입니까?

Adobe Experience Cloud에 처음 로그인할 때 인스턴스에 제공되는 고유 ID입니다. 이 ID는 xxx@AdobeOrg 형식입니다.

자세한 내용은 [Adobe Experience Cloud 설명서](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=ko)를 참조하십시오.

### 조직 ID는 어디에서 찾을 수 있습니까?

한 가지 방법은 [Adobe Experience Cloud 홈](https://experiencecloud.adobe.com/) > **[!UICONTROL 관리]**&#x200B;로 이동하는 것입니다. 내 조직 ID는 관리 **[!UICONTROL 빠른 액세스]** 섹션 맨 아래에 있습니다. [Adobe Experience Cloud 설명서](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=ko)에서 자세한 정보를 찾을 수 있습니다.

**관리 콘솔**&#x200B;을 시작하여 ID를 확인할 수도 있습니다. 조직 ID는 https://adminconsole.adobe.com/xxx@AdobeOrg/overview와 같은 형태로 URL에 표시됩니다.

### 조직 ID를 알고 있어야 하는 이유는 무엇인가요?

회사에서 여러 인스턴스를 사용하는 경우 인스턴스의 설정을 관리하려면 적절한 인스턴스의 올바른 정보를 파악할 수 있어야 합니다.

### 조직 ID가 여러 개일 경우 어떻게 하나요?

구매 중단 등의 복잡한 사용 사례를 활용하기 위해 솔루션을 통합하려는 경우, 예를 들어 Adobe Analytics + Adobe Campaign 통합 시에는 Analytics와 Campaign에 같은 조직 ID를 사용해야 합니다. 여러 Adobe 솔루션 액세스 권한이 있는 경우에는 조직 ID가 여러 개일 수 있습니다. 이 경우 사용해야 하는 올바른 조직 ID는 Adobe Campaign 인스턴스 아래에 표시되는 ID입니다.

<!--
>[!NOTE]
>
>If you have different organization IDs for Adobe Campaign and Adobe Analytics, please reach out to Customer Care to get them aligned.
-->

### Adobe Campaign 인스턴스가 AWS에서 호스팅되는지 여부는 어떻게 확인할 수 있나요?{#hosted-aws}

인스턴스가 AWS에서 호스팅되는지 확인하려면 다음 단계를 수행합니다.

1. 로그인 URL을 검색합니다. 이 URL은 Campaign 인스턴스에 로그인하는 데 사용하는 URL이며 대개 &quot;.campaign.adobe.com&quot; 또는 &quot;.neolane.net&quot;.으로 끝납니다.
1. 터미널을 열고 로그인 URL에서 **[!DNL nslookup]** 작업을 실행합니다.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 응답에서 인스턴스에 대한 정보가 반환됩니다.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. 반환된 IP 주소에서 **nslookup** 작업을 실행합니다.

   `doe-macOS% nslookup 12.34.567.89`

1. 반환된 결과에서 &quot;name&quot; 값을 확인합니다. 이 값에 &quot;amazonaws.com&quot;이 포함되어 있으면 인스턴스가 AWS에서 호스팅되는 것입니다.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>AWS로 마이그레이션하는 경우에는 Customer Success Manager에게 문의하여 해당 프로세스를 시작하십시오.
