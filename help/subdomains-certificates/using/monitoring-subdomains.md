---
title: 하위 도메인의 SSL 인증서 모니터링
description: 하위 도메인의 SSL 인증서를 모니터링하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# 하위 도메인 모니터링 {#monitoring-subdomains}

하위 도메인을 모니터링하여 Adobe Campaign과 함께 작동하도록 모두 올바르게 구성되어 있는지 확인해야 합니다.

각 프로덕션 인스턴스에 대한 하위 도메인 목록은 **[!UICONTROL Subdomains & Certificates]**카드를 선택할 때 직접 액세스할 수 있습니다.

![](assets/subdomains_list.png)

하위 도메인 목록에서 하위 도메인이 마지막으로 확인된 시점을 나타내는 **[!UICONTROL Last verification]**열이 표시됩니다.** 언제든지 **...을 클릭하여 검증을 시작할 수 있습니다./**[!UICONTROL Verify subdomain]** button.

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>확인 날짜가 없는 하위 도메인을 사용하는 것은 이러한 하위 도메인이 배달 문제가 있을 수 있음을 의미하므로 권장하지 않습니다.

검증을 시작할 때 하위 도메인이 올바르게 구성되었는지 확인하기 위해(인스턴스 테넌트 확인, 이메일 전송 테스트 등) 몇 가지 작업이 수행됩니다.

하위 도메인의 확인이 실패할 경우 Adobe 고객 지원 센터에 문의하여 추가 조사를 받으십시오.
