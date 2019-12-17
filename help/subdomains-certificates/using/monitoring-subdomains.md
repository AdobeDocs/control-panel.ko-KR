---
title: 하위 도메인의 SSL 인증서 모니터링
description: 하위 도메인의 SSL 인증서를 모니터링하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 하위 도메인 모니터링 {#monitoring-subdomains}

하위 도메인을 모니터링하여 Adobe Campaign과 함께 작동하도록 모두 올바르게 구성되어 있는지 확인해야 합니다.

각 프로덕션 인스턴스에 대한 하위 도메인 목록은 **[!UICONTROL Subdomains & Certificates]**카드를 선택할 때 직접 액세스할 수 있습니다.

![](assets/subdomains_list.png)

하위 도메인에 대한 자세한 내용을 보려면 **[!UICONTROL Subdomain Details]**단추를 클릭합니다.
모든 관련 하위 도메인 목록이 표시됩니다. 일반적으로 랜딩 페이지, 리소스 페이지 등의 하위 도메인을 포함합니다.

이 **[!UICONTROL Sender info]**탭에는 구성된 받은 편지함(발신자, 회신, 오류 이메일)에 대한 정보가 표시됩니다.

![](assets/subdomain_details.png)


하위 도메인 목록에서 하위 도메인이 마지막으로 확인된 시점을 나타내는 **[!UICONTROL Last verification]**열이 표시됩니다.** 언제든지 **...을 클릭하여 검증을 시작할 수 있습니다./**[!UICONTROL Verify subdomain]** button.

>[!CAUTION]
>
>확인 날짜가 없는 하위 도메인을 사용하는 것은 이러한 하위 도메인이 배달 문제가 있을 수 있음을 의미하므로 권장하지 않습니다.

![](assets/subdomain_verification.png)

검증을 시작할 때 하위 도메인이 올바르게 구성되었는지 확인하기 위해 몇 가지 작업이 수행됩니다.

1. 제어판은 하위 도메인이 인스턴스 테넌트에 속하는지 확인합니다.
1. 해당 하위 도메인을 사용하는 인스턴스에서 &quot;250ok&quot;의 테스트 받는 사람 집합(타사 이메일 분석 및 전달 플랫폼)으로 이메일이 전송됩니다.
1. 이메일을 받은 후 250ok는 이메일 헤더를 읽고 SPF 및 DKIM이 설정되고 유효한지 확인합니다.
1. 컨트롤 패널은 250OK에서 약 20분 동안 배달 상태를 지속적으로 폴링합니다. SPF와 DKIM이 전달되는 경우, 요청된 하위 도메인이 확인되고 완전히 구성되었으며 이메일을 보낼 준비가 되었음을 의미합니다.
