---
product: campaign
solution: Campaign
title: 컨트롤 패널 릴리스
description: 최신 Campaign 컨트롤 패널 릴리스 노트.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 10c4cf41dc9502bb66566951780cf8f963b08aa9
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 65%

---

# 컨트롤 패널 릴리스 {#control-panel-releases}

여기서는 최신 컨트롤 패널 릴리스 관련 정보를 확인할 수 있습니다.

>[!NOTE]
>
>Campaign 컨트롤 패널은 관리자 사용자만 액세스할 수 있습니다. 사용 권한에 대해 자세히 알아보기 [이 섹션](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=ko#discover-control-panel).
>
>Campaign Classic v7의 경우 인스턴스는 Amazon Web Services(AWS)에서 호스팅하고 최신 버전으로 업그레이드해야 합니다 [캠페인 안정적인 빌드](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=ko#rn-statuses) (또는 빌드 9032 이상) [이 섹션](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=ko#getting-your-campaign-version)에서 사용 중인 버전을 확인하는 방법을 알아봅니다. 인스턴스가 AWS에서 호스팅되는지 확인하려면 [이 페이지](faq.md#hosted-aws)에 설명된 단계를 수행합니다.

## 2022년 1월 {#january-2022}

**활성 쿼리 모니터링**

이제 Campaign 컨트롤 패널을 통해 인스턴스에서 가장 오랫동안 실행되는 쿼리를 모니터링할 수 있습니다. [자세히 표시](performance-monitoring/using/database-active-queries.md)

**처리량 및 지연 모니터링**

이제 인스턴스의 일정 시간 동안 게재 처리량과 지연 시간이 어떻게 트렌드인지 모니터링할 수 있습니다. [자세히 표시](performance-monitoring/using/thoughputs-latencies.md)

**새 하위 도메인에서 SSL 인증서 작업**

이제 게재 기능 감사가 진행 중인 경우에도 새로 설정된 하위 도메인에서 SSL 인증서 작업을 수행할 수 있습니다. [자세히 표시](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2021년 10월 {#october-2021}

**IP 범위 및 공개 키 유효 기간**

이제 IP 범위 및 공개 키의 가용성에 대한 기간을 설정할 수 있습니다. 자세한 내용은 [IP 범위 허용 목록](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) 및 [키 관리](sftp/using/key-management.md#installing-ssh-key) 섹션에 자세히 설명되어 있습니다.

**IP 범위 및 공개 키 편집**

이제 를 편집할 수 있습니다 [IP 범위](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) 및 [공개 키](sftp/using/key-management.md#editing-public-keys) 생성하십시오. 이 기능은 현재 Campaign 컨트롤 패널 릴리스 전에 생성된 항목에 사용할 수 없습니다.

**SFTP IP 범위 및 공개 키 만료 경고**

이제 이메일 경고 기능에는 SFTP IP에 대한 경고(만료 허용 및 SFTP 공개 키 만료)가 포함되어 있습니다. [자세히 표시](performance-monitoring/using/email-alerting.md)

**Campaign v8에서 모든 기능 지원**

다음 **하위 도메인** 및 **인증서** 관리 기능은 이제 Adobe Campaign v8의 Campaign 컨트롤 패널에서 지원됩니다.

## 2021년 8월 {#august-2021}

**Campaign v8을 사용한 지원**

이제 Adobe Campaign v8에 대해 Campaign 컨트롤 패널을 사용할 수 있으며, **하위 도메인** 및 **인증서** 관리 기능. 아직 지원되지 않습니다. 자세한 내용은 [Campaign v8 설명서](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html)를 참조하십시오{target=&quot;_blank&quot;}

## 2020년 10월 {#october-2020}

**CNAME을 사용한 하위 도메인 구성**

이제 컨트롤 패널을 통해 인터페이스에서 직접 CNAME을 사용하여 Adobe에서 작동하도록 하위 도메인을 구성할 수 있습니다. [자세한 내용](subdomains-certificates/using/setting-up-new-subdomain.md)

**데이터베이스 모니터링 개선**

데이터베이스의 공간을 사용하는 리소스에 대한 자세한 정보를 얻을 수 있는 추가 지표와 함께 데이터베이스 모니터링이 향상되었습니다. [자세한 내용](performance-monitoring/using/database-monitoring.md)

## 2020년 6월 {#june-2020}

**하위 도메인 게재 가능성 감사**

새 하위 도메인을 위임한 후, 이제 제어 패널을 통해 게재 가능성 팀이 수행한 감사를 추적할 수 있습니다. [자세한 내용](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG 키 관리**

이제 컨트롤 패널에서 GPG 키 쌍을 관리할 수 있으므로 외부에서 Campaign으로 전송되는 데이터의 암호를 쉽게 해독할 수 있습니다. 또한 Campaign에서 전송되는 데이터를 암호화하기 위해 공개 GPG 키를 설치할 수 있는 기능도 추가되었습니다. [자세한 내용](instances-settings/using/gpg-keys-management.md)

**활성 프로필 모니터링**

이제 컨트롤 패널을 통해 인스턴스 및 대금 청구 용도로 계산되는 활성 프로필의 수를 모니터링할 수 있습니다. [자세한 내용](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>컨트롤 패널의 활성 파일 모니터링은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

## 2020년 5월 {#may-2020}

**CNAME 하위 도메인용 인증서 관리**

이제 컨트롤 패널에서 CNAME 방법을 통해 구성된 하위 도메인의 SSL 인증서를 갱신할 수 있습니다. [자세한 내용](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020년 4월 {#april-2020}

**Google TXT 레코드 관리**

Campaign 컨트롤 패널을 통해 Gmail 주소로 이메일을 전송하는 데 사용되는 모든 하위 도메인에 Google TXT 사이트 확인 레코드를 추가할 수 있습니다. [자세한 내용](subdomains-certificates/using/managing-txt-records.md)

**데이터베이스 공간 모니터링**

Campaign 컨트롤 패널에 포함된 데이터베이스 모니터링 기능을 사용하면 온디맨드 방식으로 시간별 데이터베이스 공간 사용률을 확인할 수 있습니다. [자세한 내용](performance-monitoring/using/database-monitoring.md)

**이메일 경고**

Campaign 컨트롤 패널에 포함된 실시간 이메일 경고 기능을 사용하면 컨트롤 패널에 로그인한 다음 시스템에 성능 저하 위험이 있거나 향후 높은 성능을 유지하기 위해 특정 작업을 수행해야 할 때 경고를 수신하도록 등록할 수 있습니다. [자세한 내용](performance-monitoring/using/email-alerting.md)

## 2020년 1월 {#january-2020}

*2020년 1월 22일*

관리자가 컨트롤 패널에서 하위 도메인을 구성하고 SSL 인증서를 갱신할 수 있는 새 기능이 추가되었습니다.

자세한 내용은 다음 페이지를 참조하십시오.
* [새 하위 도메인 설정](subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인의 SSL 인증서 갱신](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>이러한 기능은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

## 2019년 9월 {#september-2019}

*2019년 9월 16일*

Campaign Classic 인스턴스에 연결하기 위해 관리자가 허용 목록에 IP 주소를 추가할 수 있는 새로운 기능이 추가되었습니다.
또한 관리자는 이제 Campaign Classic 인스턴스 목록과 빌드 업그레이드 가능 여부를 확인할 수 있습니다.

자세한 내용은 [전용 설명서](instances-settings/using/ip-allow-listing-instance-access.md)를 참조하십시오.

## 2019년 8월 {#august-2019}

관리자가 도메인용 SSL 인증서 만료 전에 알림을 수신할 수 있는 새 기능이 추가되었습니다. 자세한 내용은 [세부 설명서](subdomains-certificates/using/monitoring-ssl-certificates.md)를 참조하십시오.

또한 관리자는 이제 SFTP 서버에 액세스하기 위해 추가한 SSH 키를 삭제할 수 있습니다.

## 2019년 7월 {#july-2019}

관리자가 Campaign Classic 인스턴스 설정을 더 자세히 제어할 수 있는 새 기능이 추가되었습니다. 새로운 컨트롤 기능에는 Adobe Campaign가 데이터/파일 전송을 위해 연결하는 URL을 추가하는 기능 등이 있습니다.

자세한 내용은 [세부 설명서](instances-settings/using/url-permissions.md)를 참조하십시오.
