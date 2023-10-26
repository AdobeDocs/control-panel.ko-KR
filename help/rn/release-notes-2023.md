---
title: 2023년 릴리스 정보
description: 이 페이지에는 2023년 Campaign 컨트롤 패널 릴리스가 모두 나열되어 있습니다.
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a8e2fb9789e9755aa6b9c55019816d7e748606ec
workflow-type: ht
source-wordcount: '341'
ht-degree: 100%

---

# 2023년 릴리스 정보 {#rn-2023}

## 2023년 9월 {#september-2023}

<table>
<thead>
<tr>
<th><strong>DMARC 및 BIMI 레코드 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>이제 컨트롤 패널에서 직접 DMARC 및 BIMI 레코드를 추가할 수 있습니다.

<ul><li><strong>DMARC 레코드</strong>는 발신자의 도메인을 인증하고 악의적인 목적으로 도메인을 무단으로 사용하는 것을 방지하는 방법을 제공합니다. <a href="../subdomains-certificates/using/dmarc.md">DMARC 레코드를 추가하는 방법 알아보기</a></li>
<li><strong>BIMI 레코드</strong>를 사용하면 사서함 공급자의 받은 편지함에 있는 이메일 옆에 승인된 로고를 표시하여 브랜드 인지도와 신뢰도를 높일 수 있습니다. <a href="../subdomains-certificates/using/bimi.md">BIMI 레코드를 추가하는 방법 알아보기</a></li></ul>
</td>
</tr>
</tbody>
</table>

## 2023년 6월 {#june-2023}

* 이제 이미 위임한 하위 도메인의 SSL 인증서를 하위 도메인 목록에서 직접 Adobe에 위임할 수 있습니다. [자세히 알아보기](../subdomains-certificates/using/delegate-ssl.md)

* 경고 이메일 발신 주소가 `"alert@notifications.campaign.adobe.com"`으로 변경되었습니다.

## 2023년 5월 개선 사항 {#may-2023}

**Adobe에 하위 도메인의 SSL 인증서 위임**

이제 Adobe에 하위 도메인의 SSL 인증서 관리를 위임할 수 있습니다. CNAME을 사용하여 하위 도메인을 설정하는 경우, 도메인 호스팅 솔루션에 인증서를 생성하기 위해 인증서 레코드가 자동으로 생성되고 제공됩니다.

이 기능은 새 하위 도메인을 설정할 때만 사용할 수 있다는 점을 참고하십시오. 기존에 위임된 하위 도메인에 대한 인증서는 위임할 수 없습니다. [자세히 알아보기](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>Adobe 관리 SSL은 무료 기능으로, 사용자라면 비용 없이 사용할 수 있습니다.

## 2023년 3월 {#march-2023}

**CNAME에 대한 하위 도메인 위임 제거**

이제 CNAME을 사용하여 구성한 하위 도메인 위임을 제거할 수 있습니다. [자세히 알아보기](../subdomains-certificates/using/remove-delegated-subdomains.md)

## 2023년 2월 {#february-2023}

**Adobe에 위임된 하위 도메인 위임 제거**

이제 Adobe에 완전히 위임된 하위 도메인을 제거할 수 있습니다. [자세히 알아보기](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>현재 CNAME을 사용하여 설정한 하위 도메인은 위임을 제거할 수 없습니다.

**서비스 캘린더**

이제 서비스 캘린더에서 인스턴스에 발생하는 중요한 이벤트를 추적할 수 있는 캘린더 보기를 제공합니다. 또한 Campaign 컨트롤 패널 경고를 구독한 사용자에게 전송되는 알림에 대한 정보가 추가되었습니다. [자세히 알아보기](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## 2023년 1월 {#january-2023}

**새로운 하이브리드 호스팅 모델 기능**

이제 하이브리드 호스팅 모델을 사용하는 고객은 MID 인스턴스 액세스 허용 목록에 IP 주소를 추가할 수 있습니다. [자세히 알아보기](../instances-settings/using/ip-allow-listing-instance-access.md)

**CSR(인증서 서명 요청) 개선**

이제 인증서 서명 요청 생성 시 도시/지역 필드는 선택 사항입니다.
