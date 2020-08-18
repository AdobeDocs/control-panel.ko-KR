---
title: SFTP 관리
description: Campaign 컨트롤 패널의 SFTP 관리에 대한 자세한 내용
testing: SSECD-836
translation-type: tm+mt
source-git-commit: 9fe5f25ef2f3d7dafe9ae63d430279c354fce25a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 3%

---


# SFTP 관리 {#about-sftp-management}

Campaign 컨트롤 패널에서 액세스 권한이 있는 Campaign 인스턴스에 연결된 모든 SFTP 서버와 상호 작용할 수 있습니다. 대부분의 인스턴스에는 SFTP 서버가 연결되어 있습니다(경우에 따라 개발 및 단계 인스턴스가 SFTP 서버에 연결되지 않을 수 있음).

SFTP 서버에 대한 액세스는 온라인으로 찾아 다운로드할 수 있는 SFTP 클라이언트 소프트웨어를 사용하여 이루어집니다. 이러한 클라이언트 응용 프로그램 또는 API를 통해 서버에 연결하려면 공개 SSH 키를 설정하고 SFTP 서버에 연결하는 IP 주소를 허용 목록에 추가해야 합니다.

제어판에서 아래 작업을 수행하여 SFTP 서버를 관리할 수 있습니다.

* 스토리지 **용량**&#x200B;모니터링
* IP **주소 관리를 통해 나열**&#x200B;허용:하나 이상의 서버에 대한 IP 주소 범위 추가 또는 삭제,
* 공개 **SSH 키를** 관리하여 서버에 액세스합니다.

이러한 각 작업에 대한 자세한 내용은 아래 섹션에 나와 있습니다.
