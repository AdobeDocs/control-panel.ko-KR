---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서 갱신
description: 하위 도메인의 SSL 인증서를 갱신하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 90%

---


# 하위 도메인의 SSL 인증서 갱신 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 인증서 추가"
>abstract="SSL 인증서를 추가하려면 CSR을 생성하고 하위 도메인용 SSL 인증서를 구매한 다음 인증서 번들을 설치해야 합니다."
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="CSR(인증서 서명 요청) 생성"
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="SSL 인증서 설치 방법"

>[!IMPORTANT]
>
>Campaign 컨트롤 패널의 하위 도메인 구성은 베타에서 사용 가능하며 예고 없이 자주 업데이트하거나 수정할 수 있습니다.

![](assets/do-not-localize/how-to-video.png) Campaign Classic [또는](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=en#subdomains-and-certificates) [Campaign Standard을 사용하여 비디오에서 이 기능 살펴보기](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=en#adding-ssl-certificates)

## 인증서 갱신 {#about-certificate-renewal-process}

SSL 인증서 갱신 프로세스에는 다음의 세 단계를 수행합니다.

1. **CSR(인증서 서명 요청) 생성** Adobe 고객 지원 센터에서 CSR을 생성해 드립니다. 일반 이름, 조직 이름, 주소 등 CSR을 생성하는 데 필요한 정보를 제공해야 합니다.
1. **SSL 인증서 구매** CSR이 생성되면 다운로드하여 회사가 승인하는 인증 기관에서 SSL 인증서를 구매하는 데 사용할 수 있습니다.
1. **SSL 인증서 설치** 구매한 SSL 인증서를 원하는 하위 도메인에 설치할 수 있습니다.

## CSR(인증서 서명 요청) 생성 {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="CSR 생성"
>abstract="인증서를 구매하기 전에 보호하려는 인스턴스 및 하위 도메인에 대해 인증서 서명 요청을 생성해야 합니다."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="CSR을 생성할 하위 도메인 선택"
>abstract="인증서 서명 요청에는 모든 하위 도메인을 포함할 수도 있고 특정 하위 도메인만 포함할 수도 있습니다. 선택한 하위 도메인만 구매한 SSL 인증서를 통해 인증됩니다."
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="CSR(인증서 서명 요청) 생성"
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="하위 도메인 브랜딩"

CSR(인증서 서명 요청)을 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Subdomains & Certificates]** 카드에서 원하는 인스턴스를 선택하고 **[!UICONTROL Manage Certificate]** 버튼을 클릭합니다.

   ![](assets/renewal1.png)

1. **[!UICONTROL 1 - Generate a CSR]**&#x200B;을 선택하고 **[!UICONTROL Next]**&#x200B;을 클릭하여 CSR 생성 프로세스를 안내하는 마법사를 시작합니다.

   ![](assets/renewal2.png)

1. CSR을 생성하는 데 필요한 모든 세부 정보가 포함된 양식이 표시됩니다.

   요청된 정보를 완전하고 정확하게 입력해야 합니다. 이렇게 하지 않으면 인증서가 갱신되지 않을 수도 있습니다. 필요한 경우 내부 보안/IT 팀에 문의하여 정보를 확인하고 입력한 후에 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   * **[!UICONTROL Organization]**: 공식 조직 이름
   * **[!UICONTROL Organization Unit]**: 하위 도메인에 연결된 사업부(예: 마케팅, IT)
   * **[!UICONTROL Instance]**(사전 입력되어 있음): 하위 도메인에 연결된 Campaign 인스턴스의 URL

   ![](assets/renewal3.png)

1. CSR에 포함할 하위 도메인을 선택하고 **[!UICONTROL OK]**&#x200B;을 클릭합니다.

   ![](assets/renewal4.png)

1. 선택한 하위 도메인이 목록에 표시됩니다. 각 CSR에 포함할 하위 도메인을 선택하고 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

   ![](assets/renewal5.png)

1. CSR에 포함할 하위 도메인의 요약이 표시됩니다. **[!UICONTROL Submit]**&#x200B;을 클릭하여 요청을 확인합니다.

   ![](assets/renewal6.png)

1. 선택한 항목에 해당하는 .csr 파일이 자동으로 생성되어 다운로드됩니다. 이제 이 파일을 사용하여 회사가 승인하는 인증 기관에서 SSL 인증서를 구매할 수 있습니다.

   >[!NOTE]
   >
   >CSR은 저장/다운로드하지 않으면 손실되므로 다시 생성해야 합니다.

## CSR을 사용하여 인증서 구매 {#purchasing-certificate}

컨트롤 패널에서 인증서 서명 요청 CSR을 다운로드한 후에는 조직에서 승인한 인증 기관에서 SSL 인증서를 구매합니다.

## SSL 인증서 설치 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="SSL 인증서 설치"
>abstract="조직에서 승인한 인증 기관에서 구매한 SSL 인증서를 설치합니다."
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="하위 도메인 브랜딩"

구매한 SSL 인증서는 인스턴스에 설치할 수 있습니다. 계속 진행하기 전에 아래 사전 요구 사항을 숙지하십시오.

* 컨트롤 패널에서 CSR(인증서 서명 요청)을 생성한 상태여야 합니다. CSR을 생성하지 않은 경우에는 컨트롤 패널에서 인증서를 설치할 수 없습니다.
* CSR(인증서 서명 요청)은 Adobe에서 작동하도록 구성된 하위 도메인과 일치해야 합니다. 예를 들어 구성된 하위 도메인을 더 이상 포함할 수 없습니다.
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

**관련 항목:**

* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)