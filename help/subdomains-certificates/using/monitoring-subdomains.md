---
product: campaign
solution: Campaign
title: 하위 도메인 모니터링
description: 하위 도메인을 모니터링하여 이 모두 Adobe Campaign에서 작동하도록 제대로 구성되었는지 확인합니다.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: acf0334e894649d6b5edf0b96877c3f643894763
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# 하위 도메인 모니터링 {#monitoring-subdomains}

이 모두 Adobe Campaign에서 작동하도록 제대로 구성되었는지 확인하려면 하위 도메인을 모니터링해야 합니다.

각 프로덕션 인스턴스의 하위 도메인 목록은 **[!UICONTROL Subdomains & Certificates]** 카드.

다음 **[!UICONTROL Last verification]** 열은 하위 도메인이 마지막으로 확인된 시기를 나타냅니다. 다음을 클릭하여 언제든지 확인을 시작할 수 있습니다. **...** / **[!UICONTROL Verify subdomain]** 단추를 클릭합니다.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe은 인증서 날짜가 없는 하위 도메인은 전달에 문제가 있을 수 있으므로 이러한 하위 도메인을 사용하지 않는 것이 좋습니다.

확인을 시작할 때 하위 도메인이 올바르게 구성되었는지 확인하기 위해 몇 가지 작업이 수행됩니다(인스턴스 테넌트 확인, 이메일 전송 테스트 등). 하위 도메인의 확인에 실패하는 경우 추가 조사를 위해 Adobe 고객 지원 센터에 문의하십시오.

**관련 항목:**

* [하위 도메인의 SSL 인증서 갱신](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
