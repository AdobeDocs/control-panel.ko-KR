---
title: 제어판 FAQ
description: 제어판과 관련된 일반적인 질문
translation-type: tm+mt
source-git-commit: 9bd57cd6d4430cf2cae8575547f8e332f94940c1

---


# FAQ {#faq}

## IMS 조직 ID {#ims-org-id}

**IMS 조직 ID란 무엇입니까?**

Adobe Experience Cloud에 처음 로그인할 때 인스턴스에 제공되는 고유 ID입니다. 형식은 다음과 같아야 합니다.xxx@AdobeOrg.

자세한 내용은 Adobe Experience Cloud [설명서를](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)참조하십시오.

**IMS 조직 ID는 어디에서 찾을 수 있습니까?**

One way is to navigate to [Adobe Experience Cloud Home](https://exc-login.experiencecloud.adobe.com/exc-content/login.html?prefixtenantid=amc) > **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration**[!UICONTROL Quick Access]** section. [Adobe Experience Cloud 설명서](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)에서 자세한 정보를 찾을 수 있습니다.

다른 방법은 Admin Console을 **실행하는 것입니다**. IMS 조직 ID는 URL에 표시되며 다음과 같이 표시됩니다.https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**IMS 조직 ID를 알아야 하는 이유는 무엇입니까?**

인스턴스에 대한 설정을 관리하기 위해 Adobe는 귀하가 회사에 여러 인스턴스를 사용하는 경우에 적합한 인스턴스에 대한 올바른 정보를 얻을 수 있도록 하려고 합니다.

**여러 IMS 조직 ID가 있는 경우 어떻게 합니까?**

여러 Adobe 솔루션에 액세스할 수 있는 경우 두 개 이상의 IMS 조직 ID가 있을 수 있습니다. 이 경우 사용해야 하는 올바른 IMS 조직 ID가 Adobe Campaign 인스턴스 아래에 표시되는 IMS 조직 ID입니다.

>[!NOTE]
>
>Adobe Campaign 및 Adobe Analytics에 대해 동일한 IMS 조직 ID가 있는 경우, 이는 매우 중요합니다. Analytics와 Campaign 사이에 하나의 IMS 조직 ID를 보유한다는 것은 장바구니 포기와 같은 복잡한 사용 사례를 활용하도록 솔루션을 통합하려는 경우에 필요합니다(AA + AC의 경우).
>
>Adobe Campaign 및 Adobe Analytics에 대해 다른 IMS 조직 ID가 있는 경우 고객 지원 센터에 연락하여 정렬하십시오.

**Adobe Campaign 인스턴스가 AWS에서 호스팅되는지 여부를 어떻게 알 수 있습니까?**

인스턴스가 AWS에서 호스팅되는지 확인하려면 다음 단계를 따르십시오.

1. 로그인 URL을 검색합니다. Campaign 인스턴스에 로그인하는 데 사용하는 URL이며, 대부분 &quot;.campaign.adobe.com&quot; 또는 &quot;.neolane.net&quot;으로 끝납니다.
1. 터미널을 연 다음 로그인 URL에서 **[!DNL nslookup]**작업을 실행합니다.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 응답은 인스턴스에 대한 정보를 반환합니다.

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

1. 반환된 IP **주소에서** 백업 작업을 실행합니다.

   `doe-macOS% nslookup 12.34.567.89`

1. 반환된 결과에서 &quot;name&quot; 값을 확인합니다. &quot;amazonaws.com&quot;이 포함되어 있는 경우, 이는 인스턴스가 AWS에서 호스팅됨을 의미합니다.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>AWS로 마이그레이션하려면 고객 성공 관리자에게 문의하여 프로세스를 시작하십시오.

## 컨트롤 패널 {#control-panel}

**제어판이란 무엇입니까?**

제어판에서 제품 관리자는 다양한 설정을 직접 관리하고 Adobe Campaign에 연결된 SFTP 서버의 용량을 모니터링할 수 있습니다.

**제어판의 현재 기능 중 일부는 무엇입니까?**

제어판에서 사용자의 요구 사항 및 기타 작업에 따라 직접 SFTP 서버에 대한 저장 공간을 추적하고 IP를 허용 목록에 추가하며 SSH 키를 관리할 수 있습니다.

자세한 내용은 제어판 지원 액션 설명서를 참조하십시오.

**제어판은 Adobe Campaign에만 해당됩니까?**

예. 제어판에서 Adobe Campaign의 설정만 관리할 수 있습니다.

**제어판을 사용할 수 있습니까?**

제어판은 AWS에서 Adobe Campaign을 호스팅하는 현재 고객의 제품 관리자만 액세스할 수 있습니다.

관리자가 아닌 액세스 권한을 원하는 경우 제품 관리자에게 문의하여 관리자로 추가하도록 도움을 받으십시오.

**제어판에 어떻게 액세스할 수 있습니까?**

제어판 설명서의 자세한 지침을 따르십시오.

**제어판을 사용하는데 추가 비용이 있습니까?**

아니요. 현재 Adobe Campaign을 사용하고 있는 경우 추가 비용은 없습니다.
