---
title: 하위 도메인 정보
description: 하위 도메인에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# 하위 도메인 정보 {#about-subdomains}

## 하위 도메인을 설정하는 이유는 무엇입니까? {#why-setting-up-subdomains}

하위 도메인은 다양한 유형의 트래픽(기업, 마케팅 정보 등)을 차단하는 데 사용할 수 있는 도메인의 분할입니다.

다음과 같이 유용한 정보와 마케팅 커뮤니케이션을 전달하는 데 사용되는 &quot;mybrand.com&quot; 도메인의 예를 들어보겠습니다.

* 내부 통신용 info.mybrand.com
* marketing.mybrand.com을 참조하십시오.

이 경우 &quot;marketing.mybrand.com&quot; 하위 도메인을 Adobe Campaign에 위임하도록 결정할 수 있습니다. 이렇게 하면 도메인 및 기타 하위 도메인의 명성을 유지하는 데 도움이 됩니다. 예를 들어 &quot;marketing.mybrand.com&quot; 하위 도메인이 잘못된 배달 때문에 인터넷 서비스 제공자에 의해 차단되는 경우, 이로 인해 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인이 차단되지 않습니다.

## 하위 도메인 위임 메서드 {#subdomain-delegation-methods}

하위 도메인 위임을 사용하면 도메인의 하위 섹션(&quot;DNS 영역&quot;)을 Adobe Campaign과 함께 사용하도록 위임할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe Campaign에 대한 전체 하위 도메인** 위임(권장)

   하위 도메인은 Adobe에 완전히 위임됩니다. Adobe는 이메일 캠페인을 전달, 렌더링 및 추적하는 데 필요한 DNS의 모든 측면을 제어하고 유지 관리하여 Campaign을 관리 서비스로 제공할 수 있습니다.

* **CNAME 사용** (제어판을 통해 권장되지 않음 및 지원되지 않음):

   하위 도메인을 만들고 CNAME을 사용하여 Adobe 특정 레코드를 가리킵니다. 이 설정을 사용하면 Adobe와 고객 모두 DNS를 유지 관리할 책임이 있습니다.

이러한 방법(암묵적 책임, 요구 사항 등)에 대한 자세한 내용은 [이 문서를](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)참조하십시오.
