---
title: SSL 인증서 정보
description: SSL 인증서에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# SSL 인증서 정보 {#about-ssl-certificates}

Adobe Campaign에서는 랜딩 페이지를 호스팅하는 하위 도메인, 특히 고객의 민감한 정보를 수집하는 하위 도메인을 보호하는 것이 좋습니다.

**SSL(Secure Socket Layer) 암호화를** 통해 Adobe에 위임한 하위 도메인이 보호됩니다. 고객이 웹 양식을 작성하거나 Adobe Campaign에서 호스팅하는 랜딩 페이지를 방문하면 기본적으로 정보가 비보안 프로토콜(HTTP)을 통해 전송됩니다. 추가 보안을 위해 HTTPS 프로토콜을 사용하여 안전하게 전송된 정보를 제공합니다. 예를 들어 &quot;http://info.mywebsite.com/&quot; 하위 도메인 주소는 이제 &quot;https://info.mywebsite.com/&quot;이 됩니다.

**SSL 인증서는 위임된 하위 도메인 자체에**&#x200B;설치되지 않습니다. 이러한 도메인은 주로 랜딩 페이지, 리소스 페이지 등을 호스팅하는 연관된 하위 도메인에 설치됩니다.

**SSL 인증서는 특정 기간** (1년, 60일 등)에 대해 제공됩니다. 인증서가 만료되면 랜딩 페이지에 액세스하거나 하위 도메인의 리소스를 사용할 때 문제가 발생할 수 있습니다. 이를 방지하기 위해 제어판에서 하위 도메인의 SSL 인증서를 모니터링하고 갱신 프로세스를 시작할 수 있습니다.

하위 도메인 위임에 대한 자세한 내용은 [여기에서](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)확인할 수 있습니다.
