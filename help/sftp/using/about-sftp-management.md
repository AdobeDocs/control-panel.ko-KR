---
product: campaign
solution: Campaign
title: SFTP 관리
description: Campaign 컨트롤 패널의 SFTP 관리에 대해 자세히 알아보십시오
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# SFTP 관리 {#about-sftp-management}

Campaign 컨트롤 패널에서 액세스 권한이 있는 Campaign 인스턴스에 연결된 모든 SFTP 서버와 상호 작용할 수 있습니다. 대부분의 인스턴스가 SFTP 서버에 연결되어 있습니다(경우에 따라 개발 및 스테이지 인스턴스가 SFTP 서버에 연결되어 있지 않을 수 있음).

SFTP 서버에 대한 액세스는 SFTP 클라이언트 소프트웨어를 사용하여 수행되며 온라인에서 찾고 다운로드할 수 있습니다. 이러한 클라이언트 애플리케이션이나 API를 통해 서버에 연결하려면 공개 SSH 키를 설정하고 SFTP 서버에 연결하는 IP 주소를 허용 목록에 추가해야 합니다.

Campaign 컨트롤 패널을 사용하면 아래 작업을 수행하여 SFTP 서버를 관리할 수 있습니다.

* 모니터링 **스토리지 용량**,
* 관리 **IP 주소 허용 목록**: 하나 이상의 서버에 대한 IP 주소 범위를 추가하거나 삭제합니다.
* 관리 **공개 SSH 키** 서버에 액세스합니다.

이러한 각 작업에 대한 자세한 내용은 아래 섹션에서 확인할 수 있습니다.
