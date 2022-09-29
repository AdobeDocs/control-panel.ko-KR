---
product: campaign
solution: Campaign
title: 하위 도메인의 SSL 인증서 갱신
description: 하위 도메인의 SSL 인증서를 갱신하는 방법 알아보기
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# SSL 인증서 갱신 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 인증서 갱신"
>abstract="SSL 인증서를 추가하려면 CSR을 생성하고 하위 도메인용 SSL 인증서를 구매한 다음 인증서 번들을 설치해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renew-ssl/renewing-subdomain-certificate.html?lang=ko" text="CSR(인증서 서명 요청) 생성"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renew-ssl/renewing-subdomain-certificate.html?lang=ko" text="SSL 인증서 설치"

SSL 인증서 갱신 프로세스에는 다음의 세 단계를 수행합니다.

1. **CSR(인증서 서명 요청) 생성**

   인증서를 구매하기 전에 보호하려는 인스턴스 및 하위 도메인에 대해 인증서 서명 요청을 생성해야 합니다.  일반 이름, 조직 이름, 주소 등 CSR을 생성하는 데 필요한 정보를 제공해야 합니다. [자세히 알아보기](generate-csr.md)

1. **SSL 인증서 구매**

   CSR이 생성되면 이를 사용하여 회사가 승인하는 인증 기관에서 SSL 인증서를 구매할 수 있습니다.

1. **SSL 인증서 설치**

   구매한 SSL 인증서를 원하는 하위 도메인에 설치하여 보안을 설정합니다. [자세히 알아보기](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) 이 비디오에서 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=ko) 또는 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=ko)를 사용하여 해당 기능 살펴보기

**관련 항목:**

* [게재 기능 모범 사례 안내서 - Adobe Campaign에 대한 SSL 인증서 요청 프로세스](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=ko)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)
