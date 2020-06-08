---
title: 하위 도메인 브랜딩
description: 하위 도메인 브랜딩에 대해 자세히 알아보기
translation-type: ht
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451
workflow-type: ht
source-wordcount: '459'
ht-degree: 100%

---


# 하위 도메인 브랜딩 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="하위 도메인 및 SSL 인증서"
>abstract="하위 도메인 및 관련 SSL 인증서를 모니터링하는 방법을 알아봅니다."
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="하위 도메인의 SSL 인증서를 모니터링하는 방법"

>[!IMPORTANT]
>
>컨트롤 패널의 하위 도메인 위임 기능은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

## 하위 도메인을 설정하는 이유 {#why-setting-up-subdomains}

하위 도메인은 브랜드나 다양한 트래픽 유형(트랜잭션 메시지, 마케팅 정보 등)을 분리하는 데 사용할 수 있는 도메인의 개별 부분입니다.

트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 품질 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 블랙리스트에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 블랙리스트에 추가되지 않습니다.

## 하위 도메인 위임 방법 {#subdomain-delegation-methods}

하위 도메인을 위임하면 Adobe Campaign에서 사용할 도메인의 하위 섹션(기술적 명칭은 &quot;DNS 영역&quot;)을 위임할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe Campaign에 전체 하위 도메인 위임**(권장): 하위 도메인이 Adobe에 완전히 위임됩니다. Adobe는 이메일 캠페인 게재, 렌더링 및 추적에 필요한 DNS의 모든 측면을 제어하고 유지 관리하는 방식을 통해 Campaign을 관리 서비스로 제공할 수 있습니다.

* **CNAME 사용**(미권장/컨트롤 패널을 통해 지원되지 않음): 하위 도메인을 만든 다음 CNAME을 사용하여 Adobe 관련 레코드를 가리키도록 설정합니다. 이 설정을 사용하는 경우 Adobe와 고객이 DNS 유지 관리를 공동으로 수행합니다.

아래 표에는 이러한 두 가지 방법의 작동 방식과 각 방법을 사용하는 경우의 작업량이 간략하게 요약되어 있습니다.

| 위임 방법 | 작동 방법 | 작업량 |
|---|---|---|
| **전체 위임** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서는 하위 도메인 및 모든 DNS 레코드를 Adobe에서 관리합니다. | 낮음 |
| **CNAME, 사용자 지정 방법** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서는 사용자와 Adobe가 DNS 유지 관리를 공동으로 수행합니다. | 높음 |

도메인 위임에 대한 추가 정보는 [이 설명서](https://helpx.adobe.com/kr/campaign/kb/domain-name-delegation.html)에서 확인할 수 있습니다.

하위 도메인 위임 방법 관련 문의 사항이 있으면 Adobe Deliverability 팀에 문의하거나, 고객 지원 센터에 연락하여 Deliverability 컨설팅을 요청하십시오.

**관련 항목:**

* [새 하위 도메인 설정](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인 위임(튜토리얼 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)
