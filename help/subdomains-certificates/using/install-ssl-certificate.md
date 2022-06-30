---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서 갱신
description: 하위 도메인의 SSL 인증서를 갱신하는 방법 알아보기
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 88%

---

# SSL 인증서 설치 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="SSL 인증서 설치"
>abstract="조직에서 승인한 인증 기관에서 구매한 SSL 인증서를 설치합니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=ko" text="하위 도메인 브랜딩"

구매한 SSL 인증서는 인스턴스에 설치할 수 있습니다. 계속 진행하기 전에 아래 사전 요구 사항을 숙지하십시오.

* 컨트롤 패널에서 CSR(인증서 서명 요청)을 생성한 상태여야 합니다. CSR을 생성하지 않은 경우에는 컨트롤 패널에서 인증서를 설치할 수 없습니다.
* CSR(인증서 서명 요청)은 Adobe에서 작동하도록 구성된 하위 도메인과 일치해야 합니다. 예를 들어 구성된 하위 도메인보다 더 많은 하위 도메인을 포함할 수 없습니다.
* 인증서의 날짜가 현재 날짜여야 합니다. 날짜가 오늘 이후인 인증서는 설치할 수 없습니다. 또한 인증서가 만료되지 않은 상태이며, 시작 날짜와 종료 날짜가 유효해야 합니다.
* Comodo, DigiCert, GoDaddy 등의 신뢰할 수 있는 CA(인증 기관)에서 발급한 인증서를 사용해야 합니다.
* 인증서 크기는 2048비트여야 하며 알고리즘은 RSA여야 합니다.
* 인증서는 X.509 PEM 형식이어야 합니다.
* SAN 인증서가 지원됩니다.
* 와일드카드 인증서는 지원되지 않습니다.
* ZIP 파일 또는 인증서를 암호로 보호해서는 안 됩니다.
* ZIP 파일에는 다음 항목만 가급적 개별 파일 형태로 포함해야 합니다.
   * 최종 엔티티 인증서
   * 적절한 순서로 정렬된 중간 인증서 체인
   * 루트 인증서(선택 사항)

인증서를 설치하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Subdomains & Certificates]** 카드에서 원하는 인스턴스를 선택하고 **[!UICONTROL Manage Certificate]** 버튼을 클릭합니다.

   ![](assets/renewal1.png)

1. **[!UICONTROL 3 - Install Certificate Bundle]**&#x200B;를 선택하고 **[!UICONTROL Next]**&#x200B;을 클릭하여 인증서 설치 프로세스를 안내하는 마법사를 시작합니다.

   ![](assets/install1.png)

1. 설치할 인증서가 포함된 .zip 파일을 선택하고 **[!UICONTROL Submit]**&#x200B;을 클릭합니다.

   ![](assets/install2.png)

>[!NOTE]
>
>CSR에 포함된 모든 도메인/하위 도메인에 인증서가 설치됩니다. 인증서에 포함된 추가 도메인/하위 도메인은 확인 대상에서 제외됩니다.

SSL 인증서가 설치되면 인증서의 만료 날짜 및 상태 아이콘이 그에 따라 업데이트됩니다.
