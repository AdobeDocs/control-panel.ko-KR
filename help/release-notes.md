---
title: 제어판 릴리스
translation-type: tm+mt
source-git-commit: 49d84c42446ed1fc996b9d57005565b15ca24e77
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---


# 제어판 릴리스 {#control-panel-releases}

최신 제어판 릴리스에 대한 정보를 확인할 수 있습니다.

>[!NOTE]
>
>제어판은 아직 지원되지 않는 하이브리드 환경을 제외하고 AWS에서 호스팅되는 고객에게만 제공됩니다. 제어판에 액세스하려면 업그레이드할 필요가 없습니다. 액세스 권한이 있는 관리자 사용자인지 확인하십시오.

## 2020년 5월(#5월-2020일)

**GPG 키 관리**

이제 제어판에서 GPG 키 쌍을 생성할 수 있으므로 외부에서 Campaign으로 오는 데이터의 암호를 손쉽게 해독할 수 있습니다. 또한 Adobe는 Adobe Campaign에서 데이터를 암호화하는 공개 GPG 키를 설치할 수 있도록 기능을 추가했습니다. [자세한 내용](instances-settings/using/gpg-keys-management.md)

**CNAME 하위 도메인을 위한 인증서 관리**

이제 제어판에서 CNAME 메서드로 위임된 하위 도메인의 SSL 인증서를 갱신할 수 있습니다. [자세한 내용](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020년 4월 {#april-2020}

**Google TXT 레코드 관리**

캠페인 제어판을 통해 Gmail 주소로 이메일을 전송하는 데 사용되는 모든 하위 도메인에 Google TXT 사이트 확인 레코드를 추가합니다. [자세한 내용](subdomains-certificates/using/managing-txt-records.md)

**데이터베이스 공간 모니터링**

캠페인 제어판에는 데이터베이스 모니터링 기능이 포함되어 있으므로 데이터베이스 공간 사용률을 on-demand 및 시간에 따라 볼 수 있습니다. [자세한 내용](performance-monitoring/using/database-monitoring.md)

**이메일 알림**

캠페인 제어판에는 실시간 이메일 경고 기능이 포함되어 있으므로 제어판에 로그인하여 시스템이 성능이 저하될 위험이 있거나 향후 고성능 경험을 위해 조치가 필요할 때 경고를 수신하도록 등록할 수 있습니다. [자세한 내용](performance-monitoring/using/email-alerting.md)

## 2020년 1월 {#january-2020}

*2020년 1월 22일*

관리 사용자가 하위 도메인을 위임하고 제어판에서 SSL 인증서를 갱신할 수 있는 새로운 기능이 추가되었습니다.

자세한 내용은 다음 페이지를 참조하십시오.
* [새 하위 도메인 설정](subdomains-certificates/using/setting-up-new-subdomain.md)
* [하위 도메인의 SSL 인증서 갱신](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>이러한 기능은 베타에서 제공되며, 자주 업데이트하거나 예고 없이 수정할 수 있습니다.

## 2019년 9월 {#september-2019}

*2019년 9월 16일*

관리자 사용자가 Campaign Classic 인스턴스에 연결하기 위해 IP 주소를 화이트리스트에 추가할 수 있는 새로운 기능이 추가되었습니다.
또한 관리 사용자는 이제 Campaign Classic 인스턴스 목록과 빌드 업그레이드 자격 조건을 볼 수 있습니다.

자세한 내용은 [전용 설명서를 참조하십시오](instances-settings/using/ip-whitelisting-instance-access.md).

## 2019년 8월 {#august-2019}

도메인에 대한 SSL 인증서가 만료되기 전에 알림을 수신할 수 있는 관리 사용자를 위한 새로운 기능이 추가되었습니다. 자세한 내용은 [자세한 설명서를 참조하십시오](subdomains-certificates/using/monitoring-ssl-certificates.md).

또한 관리 사용자는 이제 SFTP 서버에 액세스하기 위해 추가된 SSH 키를 삭제할 수 있습니다.

## 2019년 7월 {#july-2019}

관리 사용자가 Campaign Classic 인스턴스 설정을 더욱 잘 제어할 수 있도록 새로운 기능이 추가되었습니다. 새로운 제어판 기능에는 데이터/파일 전송을 위해 Adobe Campaign에서 연결하는 URL을 추가하는 기능이 포함됩니다.

자세한 내용은 [자세한 설명서를 참조하십시오](instances-settings/using/url-permissions.md).
