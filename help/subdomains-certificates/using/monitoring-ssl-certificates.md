---
title: 하위 도메인의 SSL 인증서 모니터링
description: 하위 도메인의 SSL 인증서를 모니터링하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# 하위 도메인의 SSL 인증서 모니터링 {#monitoring-ssl-certificates}

## SSL 인증서 정보 {#about-ssl-certificates}

Adobe Campaign에서는 랜딩 페이지를 호스팅하는 하위 도메인, 특히 고객의 민감한 정보를 수집하는 하위 도메인을 보호하는 것이 좋습니다.

**SSL(Secure Socket Layer) 암호화를** 통해 Adobe에 위임한 하위 도메인이 보호됩니다. 고객이 웹 양식을 작성하거나 Adobe Campaign에서 호스팅하는 랜딩 페이지를 방문하면 기본적으로 정보가 비보안 프로토콜(HTTP)을 통해 전송됩니다. 추가 보안을 위해 HTTPS 프로토콜을 사용하여 안전하게 전송된 정보를 제공합니다. 예를 들어 &quot;http://info.mywebsite.com/&quot; 하위 도메인 주소는 이제 &quot;https://info.mywebsite.com/&quot;이 됩니다.

**SSL 인증서는 위임된 하위 도메인 자체에**&#x200B;설치되지 않습니다. 이러한 도메인은 주로 랜딩 페이지, 리소스 페이지 등을 호스팅하는 연관된 하위 도메인에 설치됩니다.

**SSL 인증서는 특정 기간** (1년, 60일 등)에 대해 제공됩니다. 인증서가 만료되면 랜딩 페이지에 액세스하거나 하위 도메인의 리소스를 사용할 때 문제가 발생할 수 있습니다. 이를 방지하기 위해 제어판에서 하위 도메인의 SSL 인증서를 모니터링하고 갱신 프로세스를 시작할 수 있습니다.

![](assets/no_certificate.png)

## SSL 인증서 모니터링 {#monitoring-certificates}

하위 도메인의 SSL 인증서 상태는 **[!UICONTROL Subdomains & Certificates]**카드를 선택할 때 하위 도메인 목록에서 직접 사용할 수 있습니다.

하위 도메인은 SSL 인증서의 가장 가까운 만료 날짜별로 배열되며 만료 날짜(일)에 대한 시각적 정보를 제공합니다.

* **녹색**:다음 60일 이내에 하위 도메인이 만료되지 않았습니다.
* **주황**:하나 이상의 하위 도메인에 다음 60일 이내에 만료되는 인증서가 있습니다.
* **빨간색**:하나 이상의 하위 도메인에 다음 30일 이내에 만료되는 인증서가 있습니다.
* **회색**:하위 도메인에 대한 인증서가 설치되어 있지 않습니다.

![](assets/subdomains_list.png)

하위 도메인에 대한 자세한 내용을 보려면 **[!UICONTROL Subdomain Details]**단추를 클릭합니다.
모든 관련 하위 도메인 목록이 표시됩니다. 일반적으로 랜딩 페이지, 리소스 페이지 등의 하위 도메인을 포함합니다.

이 **[!UICONTROL Sender info]**탭에는 구성된 받은 편지함(발신자, 회신, 오류 이메일)에 대한 정보가 표시됩니다.

![](assets/subdomain_details.png)

하위 도메인의 SSL 인증서 중 하나가 만료될 예정이면 제어판에서 바로 갱신할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.하위 [도메인의 SSL 인증서를](../../subdomains-certificates/using/renewing-subdomain-certificate.md)갱신합니다.

>[!NOTE]
>
>제어판의 인증서 갱신은 베타에서 곧 제공될 예정입니다. 제어판에서 인증서를 모니터링하는 방법에 대한 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kb/control-panel-subdomains-certificates.html) 참조하십시오.
