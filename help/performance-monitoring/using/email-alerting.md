---
product: campaign
solution: Campaign
title: 이메일 경고
description: 캠페인 인스턴스 문제가 발생하는 경우 이메일 알림을 받는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# 이메일 경고 {#email-alerting}

작업의 유연성을 높이기 위해 Campaign 컨트롤 패널은 실시간 이메일 경고 기능을 갖추고 있습니다.

이러한 경고를 가입하려면 다음 단계를 수행합니다.

1. Campaign 컨트롤 패널의 모든 위치에서 사용 가능한 **[!UICONTROL Alerting notifications]** 단추를 클릭한 다음 을 클릭합니다 **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. 구독을 확인하는 이메일이 전송됩니다.

   ![](assets/email_subscription.png)

1. 사용료 지불 옵션을 구입한 후 Campaign 컨트롤 패널은 시스템 문제를 알리고 수행할 작업을 권장합니다. 이메일 경고는 관리자가 되는 **모든 인스턴스에** 대해 등록한 모든 사람에게 전송됩니다.

   ![](assets/alert_sample.png)


경고 목록은 다음과 같습니다.

* **SFTP 저장소 사용**:SFTP 서버 중 하나가 80% 이상의 용량에 도달했습니다. See [SFTP storage management](../../sftp/using/sftp-storage-management.md).

* **데이터베이스 사용**:인스턴스 데이터베이스 중 하나가 80% 이상 용량에 도달했습니다. 데이터베이스 [모니터링을 참조하십시오](../../performance-monitoring/using/database-monitoring.md).

* **SSL 인증서 만료**:하위 도메인의 SSL 인증서 중 하나가 만료되었거나 60일 이내에 만료될 예정입니다. See [Monitoring subdomains&#39; SSL certificates](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

