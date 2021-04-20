---
product: campaign
solution: Campaign
title: SFTP 관리
description: Campaign 컨트롤 패널의 SFTP 관리에 대한 자세한 내용
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# SFTP 관리 {#about-sftp-management}

Campaign 컨트롤 패널에서 액세스 권한이 있는 Campaign 인스턴스에 연결된 모든 SFTP 서버와 상호 작용할 수 있습니다. 대부분의 인스턴스에는 SFTP 서버가 연결되어 있습니다(경우에 따라 개발 및 단계 인스턴스가 SFTP 서버에 연결되지 않을 수 있습니다).

SFTP 서버에 대한 액세스는 온라인으로 찾아 다운로드할 수 있는 SFTP 클라이언트 소프트웨어를 사용하여 이루어집니다. 이러한 클라이언트 응용 프로그램 또는 API를 통해 서버에 연결하려면 공개 SSH 키를 설정하고 SFTP 서버에 연결하는 IP 주소를 허용 목록에 추가해야 합니다.

제어판에서 아래 작업을 수행하여 SFTP 서버를 관리할 수 있습니다.

* **스토리지 용량 모니터링**,
* **IP 주소 관리를 통해** 나열 허용:하나 이상의 서버에 대한 IP 주소 범위를 추가하거나 삭제합니다.
* 서버에 액세스하려면 **공개 SSH 키**&#x200B;를 관리합니다.

이러한 각 작업에 대한 자세한 내용은 아래 섹션에 있습니다.
