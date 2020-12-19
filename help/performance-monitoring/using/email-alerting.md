---
product: campaign
solution: Campaign
title: 이메일 경고
description: 캠페인 인스턴스 문제가 발생하는 경우 이메일 알림을 받는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 이메일 경고 {#email-alerting}

Campaign 컨트롤 패널은 작업에 대한 유연성을 높이기 위해 실시간 이메일 알림 기능을 갖추고 있습니다.

이러한 경고를 구독하려면 다음 단계를 수행합니다.

1. Campaign 컨트롤 패널의 모든 위치에서 사용할 수 있는 **[!UICONTROL Alerting notifications]** 단추를 클릭한 다음 **[!UICONTROL Subscribe]** 을 클릭합니다.

   ![](assets/subscribing.png)

1. 구독을 확인하는 이메일이 전송됩니다.

   ![](assets/email_subscription.png)

1. 사용료 지불 옵션을 구입한 후 Campaign 컨트롤 패널은 시스템 문제를 알리고 수행할 작업을 권장합니다. 이메일 경고는 **모든 인스턴스**&#x200B;에 대해 등록한 모든 사용자가 자신의 관리자라는 알림을 보냅니다.

   ![](assets/alert_sample.png)


경고 목록은 다음과 같습니다.

* **SFTP 저장소 사용**:SFTP 서버 중 하나가 80% 이상의 용량에 도달했습니다. [SFTP 저장소 관리](../../sftp/using/sftp-storage-management.md)를 참조하십시오.

* **데이터베이스 사용**:인스턴스 데이터베이스 중 하나가 80% 이상의 용량에 도달했습니다. [데이터베이스 모니터링](../../performance-monitoring/using/database-monitoring.md)을 참조하십시오.

* **SSL 인증서 만료**:하위 도메인의 SSL 인증서 중 하나가 만료되었거나 60일 이내에 만료될 예정입니다. [하위 도메인의 SSL 인증서 모니터링](../../subdomains-certificates/using/monitoring-ssl-certificates.md)을 참조하십시오.

