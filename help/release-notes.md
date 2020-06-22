---
title: 컨트롤 패널 릴리스
translation-type: tm+mt
source-git-commit: 0bea4b1508305254d53eb23d45bd62944a32495a
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 70%

---


# 컨트롤 패널 릴리스 {#control-panel-releases}

여기서는 최신 컨트롤 패널 릴리스 관련 정보를 확인할 수 있습니다.

>[!NOTE]
>
>컨트롤 패널은 AWS에서 호스팅되는 고객에게만 제공됩니다. 단, 아직 지원되지 않는 하이브리드 환경에서는 컨트롤 패널이 제공되지 않습니다. 최신 빌드로 업그레이드하지 않아도 컨트롤 패널에 액세스할 수 있습니다. 컨트롤 패널에 액세스하려면 관리자 권한이 있는지 확인하십시오.

## 2020년 6월 {#june-2020}

**&#39;화이트 리스트&#39; / &#39;블랙 리스트&#39; 제거**

&#39;화이트 리스트&#39;와 &#39;블랙 리스트&#39; 용어 모두 Adobe Campaign 문서에서 제거되었습니다. 이러한 용어의 일부 항목은 여전히 제품 UI, 옵션 이름 및 내부 코드에 존재할 수 있지만, 향후 캠페인 릴리스에서 &#39;blocklist&#39; 및 &#39;allowlist&#39;로 대체될 예정입니다.

**활성 프로파일 모니터링**

이제 제어판을 통해 인스턴스 및 대금 청구 용도로 계산되는 활성 프로필의 수를 모니터링할 수 있습니다. [자세한 내용](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>제어판에서 활성 프로파일 모니터링은 베타에서 제공되며 예고 없이 자주 업데이트하거나 수정할 수 있습니다.
>
>이 기능은 Campaign Standard 10368 빌드 및 Campaign Classic 8931 빌드에서 AWS를 통해 호스팅되는 고객에게 제공됩니다. 이전 빌드를 사용하는 경우 이 기능을 사용하려면 업그레이드해야 합니다.

## 2020년 5월 {#may-2020}

**CNAME 하위 도메인용 인증서 관리**

이제 컨트롤 패널에서 CNAME 방법을 통해 위임된 하위 도메인의 SSL 인증서를 갱신할 수 있습니다. [자세한 내용](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020년 4월 {#april-2020}

**Google TXT 레코드 관리**

Campaign 컨트롤 패널을 통해 Gmail 주소로 이메일을 전송하는 데 사용되는 모든 하위 도메인에 Google TXT 사이트 확인 레코드를 추가할 수 있습니다. [자세한 내용](subdomains-certificates/using/managing-txt-records.md)

**데이터베이스 공간 모니터링**

Campaign 컨트롤 패널에 포함된 데이터베이스 모니터링 기능을 사용하면 온디맨드 방식으로 시간별 데이터베이스 공간 사용률을 확인할 수 있습니다. [자세한 내용](performance-monitoring/using/database-monitoring.md)

**이메일 경고**

Campaign 컨트롤 패널에 포함된 실시간 이메일 경고 기능을 사용하면 컨트롤 패널에 로그인한 다음 시스템에 성능 저하 위험이 있거나 향후 높은 성능을 유지하기 위해 특정 작업을 수행해야 할 때 경고를 수신하도록 등록할 수 있습니다. [자세한 내용](performance-monitoring/using/email-alerting.md)

## 2020년 1월 {#january-2020}

*2020년 1월 22일*

관리자가 컨트롤 패널에서 하위 도메인을 위임하고 SSL 인증서를 갱신할 수 있는 새 기능이 추가되었습니다.

자세한 내용은 다음 페이지를 참조하십시오.
* [새 하위 도메인 설정](subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인의 SSL 인증서 갱신](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>이러한 기능은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

## 2019년 9월 {#september-2019}

*2019년 9월 16일*

Campaign Classic 인스턴스에 연결하기 위해 관리자 사용자가 허용 목록에 IP 주소를 추가하는 새로운 기능을 추가했습니다.
또한 관리자는 이제 Campaign Classic 인스턴스 목록과 빌드 업그레이드 가능 여부를 확인할 수 있습니다.

자세한 내용은 [전용 설명서](instances-settings/using/ip-whitelisting-instance-access.md)를 참조하십시오.

## 2019년 8월 {#august-2019}

관리자가 도메인용 SSL 인증서 만료 전에 알림을 수신할 수 있는 새 기능이 추가되었습니다. 자세한 내용은 [세부 설명서](subdomains-certificates/using/monitoring-ssl-certificates.md)를 참조하십시오.

또한 관리자는 이제 SFTP 서버에 액세스하기 위해 추가한 SSH 키를 삭제할 수 있습니다.

## 2019년 7월 {#july-2019}

관리자가 Campaign Classic 인스턴스 설정을 더 자세히 제어할 수 있는 새 기능이 추가되었습니다. 새로운 컨트롤 기능에는 Adobe Campaign가 데이터/파일 전송을 위해 연결하는 URL을 추가하는 기능 등이 있습니다.

자세한 내용은 [세부 설명서](instances-settings/using/url-permissions.md)를 참조하십시오.
