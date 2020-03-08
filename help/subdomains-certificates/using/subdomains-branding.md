---
title: 하위 도메인 브랜딩
description: 하위 도메인 브랜딩에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# 하위 도메인 브랜딩 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id=&quot;cp_certificate_management&quot;
>title=&quot;하위 도메인 및 SSL 인증서 정보&quot;
>abstract=&quot;하위 도메인 및 관련 SSL 인증서 모니터링&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html&quot; text=&quot;하위 도메인&#39; SSL 인증서를 모니터링하는 방법&quot;

>[!IMPORTANT]
>
>제어판의 하위 도메인 위임은 베타에서 사용할 수 있으며, 예고 없이 자주 업데이트와 수정이 가능합니다.

## 하위 도메인을 설정하는 이유는 무엇입니까? {#why-setting-up-subdomains}

하위 도메인은 브랜드 또는 다양한 트래픽 유형(트랜잭션 메시지, 마케팅 정보 등)을 차단하는 데 사용할 수 있는 도메인의 분할입니다.

트랜잭션 커뮤니케이션과 마케팅 커뮤니케이션을 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인의 예를 살펴보겠습니다. 이러한 경우 다음 두 개의 하위 도메인을 설정할 수 있습니다.

* &quot;info.mybrand.com&quot; 하위 도메인(구매 확인, 암호 재설정 등),
* &quot;marketing.mybrand.com&quot; 하위 도메인을 참조하십시오.

이렇게 하면 도메인 및 기타 하위 도메인의 명성을 유지하는 데 도움이 됩니다. 예를 들어 &quot;marketing.mybrand.com&quot; 하위 도메인이 잘못된 배달 때문에 인터넷 서비스 제공자에 의해 차단되는 경우, 이로 인해 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인이 블랙리스트에 추가되지 않습니다.

## 하위 도메인 위임 메서드 {#subdomain-delegation-methods}

하위 도메인 위임을 사용하면 도메인의 하위 섹션(&quot;DNS 영역&quot;)을 Adobe Campaign과 함께 사용하도록 위임할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe Campaign에 대한 전체 하위 도메인 위임** (권장):하위 도메인은 Adobe에 완전히 위임됩니다. Adobe는 이메일 캠페인을 전달, 렌더링 및 추적하는 데 필요한 DNS의 모든 측면을 제어하고 유지 관리하여 Campaign을 관리 서비스로 제공할 수 있습니다.

* **CNAME 사용** (제어판을 통해 권장되지 않음 및 지원되지 않음):하위 도메인을 만들고 CNAME을 사용하여 Adobe 특정 레코드를 가리킵니다. 이 설정을 사용하면 Adobe와 고객 모두 DNS를 유지 관리할 책임이 있습니다.

아래 표는 이러한 방법이 어떻게 작동하는지에 대한 요약과 암시적인 노력 수준을 제공합니다.

| 위임 메서드 | 작동 방식 | 노력 수준 |
|---|---|---|
| **전체 위임** | 하위 도메인 및 네임스페이스 레코드를 만듭니다. 그런 다음 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서 Adobe는 하위 도메인 및 모든 DNS 레코드를 관리할 책임이 있습니다. | 낮음 |
| **CNAME, 사용자 지정 메서드** | 하위 도메인 및 네임스페이스 레코드를 만듭니다. 그런 다음 Adobe는 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서 사용자와 Adobe 모두 DNS 유지 관리에 대한 책임을 공유합니다. | 높음 |

도메인 위임에 대한 추가 정보는 [이 문서에서](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)확인할 수 있습니다.

하위 도메인 위임 방법에 대한 질문이 있는 경우 Adobe Deliverability 팀에 문의하거나 고객 지원 센터에 문의하여 배달 가능성 컨설팅 요청을 참조하십시오.

**관련 항목:**

* [새 하위 도메인 설정](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인 위임(자습서 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)
