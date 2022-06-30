---
title: 최신 릴리스
description: 이 페이지에는 Campaign 컨트롤 패널의 새로운 기능과 개선 사항이 모두 포함되어 있습니다
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: e0b0daba3a5820dc80b35d8c83ffc9143d547529
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 49%

---

# 최신 릴리스 {#control-panel-releases}

이 페이지에는 Campaign 컨트롤 패널의 새로운 기능과 개선 사항이 모두 포함되어 있습니다.

## 2022년 6월 {#june-2022}

### 새로운 기능?

<table>
<thead>
<tr>
<th><strong>SFTP 서버의 공간을 사용하는 상위 10개 파일</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 SFTP 서버에서 가장 많은 공간을 사용하는 상위 10개 파일을 식별할 수 있습니다. <a href="../sftp/using/sftp-storage-management.md">자세히 알아보기</a></p>
<img src="../assets/do-not-localize/sftp.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>서비스 달력 미리 알림</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 서비스 달력에서 이벤트가 인스턴스에서 발생되기 전에 전자 메일로 알림을 받기 위해 미리 알림을 설정할 수 있습니다. <a href="../instances-settings/using/external-accounts.md">자세히 알아보기</a></p>
<img src="../assets/do-not-localize/reminders.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>하위 도메인의 CSR 생성 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CSR 생성 프로세스에 몇 가지 개선 사항이 있습니다. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">자세히 알아보기</a></p><ul><li>이제 CSR을 생성할 때 포함된 하위 도메인 중 하나를 공통 이름으로 선택할 수 있습니다.</li><li>이제 CSR을 생성하기 전에 CSR 요약을 복사할 수 있습니다.</li><li>CSR이 생성되면 작업 로그에서 다시 다운로드할 수 있습니다. 이 기능은 이 릴리스 전에 생성된 인증서에는 적용되지 않습니다.</li></ul><p>
<img src="../assets/do-not-localize/CSR.gif"/>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**인스턴스 설정**

* Campaign 컨트롤 패널의 최대 GPG 키 수가 60키로 늘었습니다. [자세히 알아보기](../instances-settings/using/gpg-keys-management.md)

## 2022년 5월 {#may-2022}

<table>
<thead>
<tr>
<th><strong>하이브리드 호스팅 모델에 대한 컨트롤 패널 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 하이브리드 호스팅 모델을 사용하는 고객은 컨트롤 패널을 사용할 수 있습니다. 이러한 고객은 컨트롤 패널에서 마케팅 인스턴스에 구성된 MID/RT 인스턴스 URL을 제공하여 컨트롤 패널의 기능을 활용할 수 있습니다.</p><p>자세한 내용은 <a href="../instances-settings/using/external-accounts.md">자세한 설명서</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>처리량 및 대기 시간 모니터링 업데이트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>처리량 및 대기 시간 모니터링 기능이 향상되었습니다:<ul><li>이제 인스턴스의 처리량에 기여하는 상위 5개 게재의 ID를 식별할 수 있습니다.</li><li>이제 Campaign Classic v7/v8 고객이 특정 채널에 대한 지연을 시각화할 수 있습니다.</p></li><p>자세한 내용은 <a href="../performance-monitoring/using/thoughputs-latencies.md">자세한 설명서</a></p>
</td>
</tr>
</tbody>
</table>


## 2022년 4월 {#april-2022}

<table>
<thead>
<tr>
<th><strong>인스턴스 내 주요 연락처 및 이벤트 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 인스턴스에서 발생하는 이전 및 예정된 릴리스 및 서비스 검토를 모니터링하고 요청 또는 문제에 관해 Adobe의 주요 연락처 목록에 액세스할 수 있습니다.</p><p>자세한 내용은 <a href="../service-events/service-events.md">자세한 설명서</a></p>
</td>
</tr>
</tbody>
</table>

## 2022년 3월 {#march-2022}

<table>
<thead>
<tr>
<th><strong>처리량 및 지연 모니터링 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 모든 Campaign Standard 및 v8 고객과 9032,9330, 9346 또는 9349 빌드 번호를 사용하는 Campaign V7 고객이 처리량 및 지연 모니터링을 사용할 수 있습니다(mid 인스턴스 없음).</p><p>자세한 내용은 <a href="../performance-monitoring/using/thoughputs-latencies.md">자세한 설명서</a></p>
</td>
</tr>
</tbody>
</table>

## 2022년 2월 {#february-2022}

<table>
<thead>
<tr>
<th><strong>워크플로우 매개 변수 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 인스턴스의 문제를 방지하기 위해 특정 주의가 필요한 워크플로우 매개 변수를 모니터링할 수 있습니다. </p><p>자세한 내용은 <a href="../performance-monitoring/using/workflow-monitoring.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

## 2022년 1월 {#january-2022}

<table>
<thead>
<tr>
<th><strong>활성 쿼리 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Campaign 컨트롤 패널을 통해 인스턴스에서 가장 오랫동안 실행되는 쿼리를 모니터링할 수 있습니다.</p><p>자세한 내용은 <a href="../performance-monitoring/using/database-active-queries.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>처리량 및 지연 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 인스턴스의 일정 시간 동안 게재 처리량과 지연 시간이 어떤 트렌드인지 모니터링할 수 있습니다.</p><p>자세한 내용은 <a href="../performance-monitoring/using/thoughputs-latencies.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새 하위 도메인에서 SSL 인증서 작업</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 게재 기능 감사가 진행 중인 경우에도 새로 설정된 하위 도메인에서 SSL 인증서 작업을 수행할 수 있습니다.</p><p>자세한 내용은 <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>
