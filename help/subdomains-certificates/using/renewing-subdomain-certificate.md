---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서 갱신
description: 하위 도메인의 SSL 인증서를 갱신하는 방법 알아보기
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 100%

---

# SSL 인증서 갱신 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 인증서 갱신"
>abstract="SSL 인증서를 추가하려면 CSR을 생성하고 하위 도메인용 SSL 인증서를 구매한 다음 인증서 번들을 설치해야 합니다. 이 작업은 인증서를 Adobe에 위임하지 않고 수동으로 관리하도록 선택한 경우에만 필요합니다. "

>[!NOTE]
>
>하위 도메인의 SSL 인증서 갱신은 해당 프로세스를 Adobe에 위임하지 않고 직접 인증서를 관리하기로 선택한 경우에만 필요한 과정입니다. 하위 도메인의 SSL 인증서 관리를 Adobe으로 위임하는 것을 강력하게 추천합니다. Adobe에서 인증서를 자동으로 만들고 매년 만료 전에 갱신하기 때문에 편리합니다. [SSL 인증서 관리에 대해 자세히 알아보기](monitoring-ssl-certificates.md#management)

SSL 인증서 갱신 프로세스에는 다음의 세 단계를 수행합니다.

1. **CSR(인증서 서명 요청) 생성**

   인증서를 구매하기 전에 보호하려는 인스턴스 및 하위 도메인에 대해 인증서 서명 요청을 생성해야 합니다.  일반 이름, 조직 이름, 주소 등 CSR을 생성하는 데 필요한 정보를 제공해야 합니다. [자세히 알아보기](#generate)

1. **SSL 인증서 구매**

   CSR이 생성되면 이를 사용하여 회사가 승인하는 인증 기관에서 SSL 인증서를 구매할 수 있습니다.

1. **SSL 인증서 설치**

   구매한 SSL 인증서를 원하는 하위 도메인에 설치하여 보안을 설정합니다. [자세히 알아보기](#install)

![](assets/do-not-localize/how-to-video.png) 이 비디오에서 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=ko) 또는 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=ko)를 사용하여 해당 기능 살펴보기

**관련 항목:**

* [게재 기능 모범 사례 안내서 - Adobe Campaign에 대한 SSL 인증서 요청 프로세스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=ko)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)

## CSR 생성 {#generate}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="CSR 생성"
>abstract="인증서를 구매하기 전에 보호하려는 인스턴스 및 하위 도메인에 대해 인증서 서명 요청을 생성해야 합니다."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="CSR을 생성할 하위 도메인 선택"
>abstract="인증서 서명 요청에는 모든 하위 도메인을 포함할 수도 있고 특정 하위 도메인만 포함할 수도 있습니다. 선택한 하위 도메인만 구매한 SSL 인증서를 통해 인증됩니다."

CSR(인증서 서명 요청)을 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 하위 도메인 및 인증서]** 카드에서 원하는 인스턴스를 선택한 후 **[!UICONTROL 인증서 관리]** 버튼을 클릭합니다.

   ![](assets/renewal1.png)

1. **[!UICONTROL 1 - CSR 생성]**&#x200B;을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭하여 CSR 생성 프로세스를 안내하는 마법사를 시작합니다.

   ![](assets/renewal2.png)

1. CSR을 생성하는 데 필요한 모든 세부 정보가 포함된 양식이 표시됩니다.

   요청된 정보를 완전하고 정확하게 입력했는지 확인합니다. 그렇지 않으면 인증서가 갱신되지 않을 수 있습니다(필요한 경우 내부 팀, 보안 및 IT 팀에 문의). **[!UICONTROL 다음]**&#x200B;을 클릭하십시오.

   * **[!UICONTROL 조직]**: 조직의 공식 이름입니다.
   * **[!UICONTROL 조직 부서]**: 하위 도메인에 연결된 부서입니다(예: 마케팅, IT).
   * **[!UICONTROL 인스턴스]**(사전 입력되어 있음): 하위 도메인에 연결된 Campaign 인스턴스의 URL입니다.
   * **[!UICONTROL 공통 이름]**: 기본적으로 공통 이름이 선택되어 있으며, 필요한 경우 하위 도메인 중 하나를 선택할 수 있습니다.

   ![](assets/renewal3.png)

1. CSR에 포함할 하위 도메인을 선택하고 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   ![](assets/renewal4.png)

1. 선택한 하위 도메인이 목록에 표시됩니다. 각각에 대해 포함할 하위 도메인을 선택하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![](assets/renewal5.png)

1. CSR에 포함할 하위 도메인의 요약이 표시됩니다. 요청을 확인하려면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

   ![](assets/renewal6.png)

   >[!NOTE]
   >
   >**[!UICONTROL CSR 콘텐츠 복사]** 버튼으로 CSR과 관련된 모든 정보(조직 ID, 인스턴스, 조직 이름, 공통 이름, 포함된 하위 도메인 등)를 복사할 수 있습니다.

1. 선택한 항목에 해당하는 .csr 파일이 자동으로 생성되어 다운로드됩니다. 이제 이 파일을 사용하여 회사가 승인하는 인증 기관에서 SSL 인증서를 구매할 수 있습니다. CSR을 다시 다운로드해야 하는 경우 [이 섹션](#download)에 자세히 나와 있는 단계를 따르면 됩니다.

CSR 생성과 다운로드가 완료되면 사용자의 조직에서 승인한 인증 기관에서 SSL 인증서를 구매하는 데 사용할 수 있습니다.

구매한 SSL 인증서는 인스턴스에 설치하여 하위 도메인의 보안을 유지할 수 있습니다. [자세히 알아보기](#install)

## CSR 다운로드 {#download}

SSL 인증서를 구매하려면 먼저 CSR(인증서 서명 요청)을 다운로드해야 합니다. CSR은 생성 후 자동으로 다운로드됩니다. 작업 로그에서 언제든지 다시 다운로드할 수도 있습니다.

1. **[!UICONTROL 작업 로그]**&#x200B;에서 **[!UICONTROL 완료]** 탭을 선택한 다음 하위 도메인 관리와 관련된 작업을 표시하도록 목록을 필터링합니다.

   ![](assets/renewal-download.png)

1. CSR 생성에 해당하는 작업을 연 다음 **[!UICONTROL 다운로드]** 링크를 클릭하여 .csr 파일을 가져옵니다.

   ![](assets/renewal-download-button.png)

## SSL 인증서 설치 {#install}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="SSL 인증서 설치"
>abstract="조직에서 승인한 인증 기관에서 구매한 SSL 인증서를 설치합니다."

구매한 SSL 인증서는 인스턴스에 설치할 수 있습니다. 계속 진행하기 전에 아래 사전 요구 사항을 숙지하십시오.

* 컨트롤 패널에서 CSR(인증서 서명 요청)을 생성한 상태여야 합니다. CSR을 생성하지 않은 경우에는 컨트롤 패널에서 인증서를 설치할 수 없습니다.
* CSR(인증서 서명 요청)은 Adobe에 맞추어 구성한 하위 도메인과 일치해야 합니다. 예를 들어 이미 구성한 하위 도메인보다 더 많은 하위 도메인을 포함할 수는 없습니다.
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

1. **[!UICONTROL 하위 도메인 및 인증서]** 카드에서 원하는 인스턴스를 선택한 후 **[!UICONTROL 인증서 관리]** 버튼을 클릭합니다.

   ![](assets/renewal1.png)

1. **[!UICONTROL 3 - 인증서 번들 설치]**&#x200B;를 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭하여 인증서 설치 프로세스를 안내하는 마법사를 시작합니다.

   ![](assets/install1.png)

1. 설치할 인증서가 포함된 .zip 파일을 선택한 다음 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

   ![](assets/install2.png)

>[!NOTE]
>
>CSR에 포함된 모든 도메인/하위 도메인에 인증서가 설치됩니다. 인증서에 포함된 추가 도메인/하위 도메인은 확인 대상에서 제외됩니다.

SSL 인증서가 설치되면 인증서의 만료 날짜 및 상태 아이콘이 그에 따라 업데이트됩니다.
