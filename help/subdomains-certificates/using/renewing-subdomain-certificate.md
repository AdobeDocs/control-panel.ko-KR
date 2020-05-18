---
title: 하위 도메인의 SSL 인증서 갱신
description: 하위 도메인의 SSL 인증서를 갱신하는 방법 살펴보기
translation-type: tm+mt
source-git-commit: bc29433167d4699ad9b840381abd0d5bbff8c630
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---


# 하위 도메인의 SSL 인증서 갱신 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 인증서 추가"
>abstract="SSL 인증서를 추가하려면 CSR을 생성하고 하위 도메인의 SSL 인증서를 구매하고 인증서 번들을 설치해야 합니다."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="CSR(인증서 서명 요청) 생성"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="SSL 인증서 설치 방법"

>[!IMPORTANT]
>
>제어판의 하위 도메인 위임은 베타 버전으로 제공되며, 예고 없이 자주 업데이트하거나 수정할 수 있습니다.

## 인증서 갱신 정보 {#about-certificate-renewal-process}

SSL 인증서 갱신 프로세스에는 다음 3단계가 포함됩니다.

1. **CSR(Certificate Signing Request)의 생성** Adobe 고객 지원 센터에서 사용자를 위한 CSR을 생성합니다. CSR을 생성하는 데 필요한 정보(예: 공통 이름, 조직 이름 및 주소 등)를 제공해야 합니다.
1. **SSL 인증서**&#x200B;구매 CSR이 생성되면 이를 다운로드하여 회사가 승인한 인증 기관에서 SSL 인증서를 구입하는 데 사용할 수 있습니다.
1. **SSL 인증서**&#x200B;설치 SSL 인증서를 구입하면 원하는 하위 도메인에 설치할 수 있습니다.

## CSR(인증서 서명 요청) 생성 {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="CSR 생성"
>abstract="인증서를 구매하기 전에 보안을 설정하려는 인스턴스 및 하위 도메인에 대해 인증서 서명 요청을 생성해야 합니다."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="CSR의 하위 도메인 선택"
>abstract="인증서 서명 요청에 모든 또는 특정 하위 도메인을 포함하도록 선택할 수 있습니다. 선택한 하위 도메인만 구매한 SSL 인증서를 통해 인증됩니다."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="CSR(인증서 서명 요청) 생성"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="하위 도메인 브랜딩 정보"

CSR(인증서 서명 요청)을 생성하려면 다음 단계를 수행하십시오.

1. 카드에서 **[!UICONTROL Subdomains & Certificates]** 원하는 인스턴스를 선택한 다음 **[!UICONTROL Manage Certificate]** 단추를 클릭합니다.

   ![](assets/renewal1.png)

1. 선택한 **[!UICONTROL 1 - Generate a CSR]****[!UICONTROL Next]** 다음 을 클릭하여 CSR 생성 프로세스를 안내하는 마법사를 시작합니다.

   ![](assets/renewal2.png)

1. CSR을 생성하는 데 필요한 모든 세부 정보가 포함된 양식이 표시됩니다.

   요청된 정보를 완전하고 정확하게 채워야 하며 그렇지 않으면 인증서가 갱신되지 않을 수 있습니다(필요한 경우 내부 팀, 보안 및 IT 팀에 문의). 그런 다음 을 클릭합니다 **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: 공식 조직명
   * **[!UICONTROL Organization Unit]**: 하위 도메인에 연결된 단위(예: 마케팅, IT).
   * **[!UICONTROL Instance]** (사전 채움): 하위 도메인에 연결된 캠페인 인스턴스의 URL.
   ![](assets/renewal3.png)

1. CSR에 포함할 하위 도메인을 선택하고 을 클릭합니다 **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. 선택한 하위 도메인이 목록에 표시됩니다. 각각에 대해 포함할 하위 도메인을 선택한 다음 을 클릭합니다 **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. CSR에 포함할 하위 도메인 요약 표시 을 **[!UICONTROL Submit]** 클릭하여 요청을 확인합니다.

   ![](assets/renewal6.png)

1. 선택한 항목에 해당하는 .csr 파일이 자동으로 생성되고 다운로드됩니다. 이제 회사에서 승인한 인증 기관에서 SSL 인증서를 구입하는 데 사용할 수 있습니다.

   >[!NOTE]
   >
   >CSR이 저장/다운로드되지 않으면 CSR이 손실되며 다시 생성해야 합니다.

## CSR을 사용하여 인증서 구입 {#purchasing-certificate}

제어판에서 인증서 서명 요청 CSR을 얻은 후 조직에서 승인한 인증 기관에서 SSL 인증서를 구입합니다.

## SSL 인증서 설치 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="SSL 인증서 설치"
>abstract="조직에서 승인한 인증 기관에서 구입한 SSL 인증서를 설치합니다."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="하위 도메인 브랜딩 정보"

SSL 인증서를 구입하면 인스턴스에 설치할 수 있습니다. 계속하기 전에 아래 사전 요구 사항을 알고 있는지 확인하십시오.

* 제어판에서 CSR(인증서 서명 요청)이 생성되어야 합니다. 그렇지 않으면 제어판에서 인증서를 설치할 수 없습니다.
* CSR(인증서 서명 요청)은 Adobe에 위임된 하위 도메인과 일치해야 합니다. 예를 들어 위임된 하위 도메인을 더 이상 포함할 수 없습니다.
* 인증서에 현재 날짜가 있어야 합니다. 나중에 날짜가 있는 인증서를 설치할 수 없으며 만료되지 않아야 합니다(예: 유효한 시작 및 종료 날짜).
* 인증서는 Comodo, DigiCert, GoDaddy 등과 같은 신뢰할 수 있는 인증 기관(CA)에서 발행해야 합니다.
* 인증서 크기는 2048비트여야 하며 알고리즘은 RSA여야 합니다.
* 인증서는 X.509 PEM 형식이어야 합니다.
* SAN 인증서가 지원됩니다.
* 와일드카드 인증서는 지원되지 않습니다.
* ZIP 파일 또는 인증서는 암호로 보호되어서는 안 됩니다.
* ZIP 파일에는 다음 내용만 포함되어야 합니다(가급적이면 개별 파일).
   * 최종 엔티티 인증서.
   * 중간 인증서 체인(적절한 순서로 배열됨).
   * 루트 인증서(선택 사항).

인증서를 설치하려면 다음 단계를 수행하십시오.

1. 카드에서 **[!UICONTROL Subdomains & Certificates]** 원하는 인스턴스를 선택한 다음 **[!UICONTROL Manage Certificate]** 단추를 클릭합니다.

   ![](assets/renewal1.png)

1. 을 선택한 **[!UICONTROL 3 - Install Certificate Bundle]****[!UICONTROL Next]** 다음 을 클릭하여 인증서 설치 과정을 안내하는 마법사를 시작합니다.

   ![](assets/install1.png)

1. 설치할 인증서가 포함된 .zip 파일을 선택한 다음 을 클릭합니다 **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>인증서가 CSR에 포함된 모든 도메인/하위 도메인에 설치됩니다. 인증서에 있는 추가 도메인/하위 도메인이 고려되지 않습니다.

SSL 인증서가 설치되면 인증서의 만료 날짜 및 상태 아이콘이 그에 따라 업데이트됩니다.

**관련 항목:**

* [SSL 인증서 추가(자습서 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)