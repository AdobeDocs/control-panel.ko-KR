---
product: campaign
solution: Campaign
title: 이메일 경고
description: Campaign 인스턴스와 관련된 문제가 발생하는 경우 이메일 알림을 받는 방법을 알아봅니다
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: ec83878e93536c979c39da52ed07b465f4fbbcb1
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# 이메일 경고 {#email-alerting}

Campaign 컨트롤 패널은 보다 유연하게 작업을 수행할 수 있도록 실시간 이메일 경고 기능을 제공합니다.

이러한 경고를 구독하려면 다음 단계를 수행합니다.

1. 을(를) 클릭합니다. **[!UICONTROL Alerting notifications]** Campaign 컨트롤 패널의 모든 위치에서 사용할 수 있는 단추를 클릭한 다음 **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. 가입을 확인하기 위해 이메일이 전송됩니다.

   ![](assets/email_subscription.png)

1. 가입 후 Campaign 컨트롤 패널은 시스템 문제에 대해 알리고 수행할 작업을 추천합니다. 전자 메일 경고는 등록한 모든 사용자에게 전송됩니다 **모든 인스턴스** 의 관리자임을 확인합니다.

   ![](assets/alert_sample.png)

경고 목록은 다음과 같습니다.

* **SFTP 저장소 사용**: SFTP 서버 중 하나가 용량을 80% 이상 사용했습니다. 자세한 내용은 [SFTP 스토리지 관리](../../sftp/using/sftp-storage-management.md).

* **데이터베이스 사용**: 인스턴스 데이터베이스 중 하나가 용량 80% 이상에 도달했습니다. 자세한 내용은 [데이터베이스 모니터링](../../performance-monitoring/using/database-monitoring.md).

* **SSL 인증서 만료**: 하위 도메인의 SSL 인증서 중 하나가 만료되었거나 60일 이내에 만료됩니다. 자세한 내용은 [하위 도메인의 SSL 인증서 모니터링](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **SFTP IP 허용 목록 만료**: 정의한 IP 범위 중 하나가 만료되었거나 10일 이내에 만료될 예정입니다. 자세한 내용은 [IP 범위 허용 목록](../../sftp/using/ip-range-allow-listing.md).

* **SFTP 공개 키 만료**: 정의한 공개 키 중 하나가 만료되었거나 10일 이내에 만료될 예정입니다. 자세한 내용은 [키 관리](../../sftp/using/key-management.md).

* **긴 실행 쿼리**: 인스턴스 중 하나에서 24시간 이상 쿼리를 실행했습니다. 자세한 내용은 [활성 쿼리 모니터링](database-active-queries.md).