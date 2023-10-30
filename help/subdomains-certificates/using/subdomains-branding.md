---
product: campaign
solution: Campaign
title: 하위 도메인 브랜딩
description: 하위 도메인 브랜딩에 대해 자세히 알아보기
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 78%

---

# 하위 도메인 브랜딩 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="하위 도메인 및 SSL 인증서"
>abstract="하위 도메인 및 관련 SSL 인증서를 모니터링하는 방법을 알아봅니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=ko" text="SSL 인증서 모니터링"

## 하위 도메인을 설정하는 이유  {#why-setting-up-subdomains}

하위 도메인은 브랜드나 다양한 트래픽 유형(트랜잭션 메시지, 마케팅 정보 등)을 분리하는 데 사용할 수 있는 도메인의 개별 부분입니다.

트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 가능성 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 차단 목록에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 차단 목록에 추가되지 않습니다.

## 하위 도메인 구성 메서드 {#subdomain-delegation-methods}

하위 도메인 구성을 사용하면 Adobe Campaign에서 사용할 도메인의 하위 섹션(기술적 명칭은 &quot;DNS 영역&quot;)을 구성할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe Campaign에 전체 하위 도메인 위임**(권장): 하위 도메인이 Adobe에 완전히 위임됩니다. Adobe는 이메일 캠페인 게재, 렌더링 및 추적에 필요한 DNS의 모든 측면을 제어하고 유지 관리하는 방식을 통해 Campaign을 관리 서비스로 제공할 수 있습니다.

* **CNAME 사용**: 하위 도메인을 만들고 CNAME을 사용하여 Adobe 관련 레코드를 가리킵니다. 이 설정을 사용하는 경우 Adobe와 고객이 DNS 유지 관리를 공동으로 수행합니다.

아래 표에는 이러한 두 가지 방법의 작동 방식과 각 방법을 사용하는 경우의 작업량이 간략하게 요약되어 있습니다.

| 구성 방법 | 작동 방법 | 작업량 |
|---|---|---|
| **전체 위임** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서는 Adobe가 하위 도메인 및 모든 DNS 레코드를 관리를 전적으로 책임집니다. | 낮음 |
| **CNAME, 사용자 지정 방법** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서는 사용자와 Adobe가 DNS 유지 관리를 공동으로 수행합니다. | 높음 |

도메인 구성에 대한 추가 정보는에서 사용할 수 있습니다. [이 설명서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

하위 도메인 구성 방법에 대한 질문이 있는 경우 Adobe 전달성 팀에 문의하거나 고객 지원 센터에 연락하여 전달성 컨설팅을 요청하십시오.

## 하위 도메인의 사용 사례(Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="하위 도메인의 사용 사례 선택"
>abstract="메시지 전달성을 높이려면 사용 사례에 따라 하위 도메인을 구분하는 것이 좋습니다. 이렇게 하면 각 하위 도메인의 평판을 독립적으로 보호할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=ko" text="새 하위 도메인 설정"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=ko" text="하위 도메인 브랜딩"

Campaign v7/v8 인스턴스에 대한 하위 도메인을 설정할 때는 하위 도메인을 사용할 사용 사례를 선택해야 합니다(참조) [새 하위 도메인 설정](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

가능한 사용 사례는 다음과 같습니다.

* **마케팅 커뮤니케이션**: 상업적 메시지 전송용 하위 도메인으로 설정합니다. 영업 이메일 캠페인 등을 예로 들 수 있습니다.

* **거래 및 운영 커뮤니케이션**: 거래 커뮤니케이션에는 수신자가 시작한 프로세스를 완료하는 데 필요한 정보가 포함됩니다. 구매 확인, 암호 재설정 이메일 등을 예로 들 수 있습니다. 조직 커뮤니케이션은 상업적 목적 없이 조직 내/외부에서 정보, 아이디어, 견해 등을 교환하는 과정에서 사용됩니다.

**메시지 배달 가능성을 높이려면 사용 사례에 따라 하위 도메인을 구분하는 것이 좋습니다**. 이렇게 하면 각 하위 도메인의 평판을 독립적으로 보호할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 마케팅 커뮤니케이션용 하위 도메인을 차단 목록에 추가해도 트랜잭션 커뮤니케이션용 하위 도메인에는 아무런 영향이 없으므로 통신을 계속 전송할 수 있습니다.

**마케팅 및 트랜잭션 사용 사례 모두에 대해 하위 도메인을 구성할 수 있습니다**:

* 마케팅 사용 사례의 경우 하위 도메인은 **MID**(미드 소싱) 인스턴스에 구성됩니다.
* 거래 사용 사례의 경우 연결을 보장하기 위해 모든 **RT**(메시지 센터/실시간 메시징) 인스턴스에 하위 도메인이 구성됩니다. 따라서 하위 도메인이 모든 RT 인스턴스와 연동됩니다.

>[!NOTE]
>
>Campaign v7/v8을 사용하는 경우 Campaign 컨트롤 패널을 통해 작업 중인 마케팅 인스턴스에 연결된 RT/MID 인스턴스를 확인할 수 있습니다. 자세한 내용은 [인스턴스 세부 정보](../../instances-settings/using/instance-details.md) 섹션을 참조하십시오.

**관련 항목:**

* [새 하위 도메인 설정](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)
