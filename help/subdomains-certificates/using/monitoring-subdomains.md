---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서 모니터링
description: 하위 도메인의 SSL 인증서를 모니터링하는 방법 알아보기
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 8dce5b9d1eb59b7ebc8ef1f73f7552dcf61077a1
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 21%

---

# 하위 도메인 모니터링 {#monitoring-subdomains}

>[!AVAILABILITY]
>
>이 기능은 Campaign v8에서는 사용할 수 없습니다.

Adobe Campaign에서 작동하도록 하위 도메인을 모니터링하는 것이 중요합니다.

The list of subdomains for each of your production instances is accessible directly when selecting the **[!UICONTROL Subdomains & Certificates]** card.

다음 **[!UICONTROL Last verification]** 열은 마지막으로 하위 도메인을 확인한 시점을 나타냅니다. 언제든지 을(를) 클릭하여 확인을 시작할 수 있습니다 **...** / **[!UICONTROL Verify subdomain]** 버튼을 클릭합니다.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe does not recommend using subdomains with no certificate date as it could mean that these subdomains may be having some deliverability issues.

확인을 시작할 때 하위 도메인이 올바르게 구성되었는지( 인스턴스 테넌트 확인, 이메일 전송 테스트 등) 확인하는 여러 작업이 수행됩니다.

하위 도메인의 확인이 실패하면 Adobe 고객 지원 센터에 문의하여 추가 조사를 받으십시오.

**관련 항목:**

* [하위 도메인의 SSL 인증서 갱신](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
