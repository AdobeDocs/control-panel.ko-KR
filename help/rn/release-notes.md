---
title: 최신 릴리스
description: 이 페이지에는 컨트롤 패널의 새로운 기능과 개선 사항이 모두 포함되어 있습니다.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 100%

---

# 최신 릴리스 {#control-panel-releases}

이 페이지에는 컨트롤 패널의 새로운 기능과 개선 사항이 모두 포함되어 있습니다.

## 2023년 10월 {#october-2023}

**사용자 인터페이스**

* [컨트롤 패널]의 지원 언어가 추가되었습니다. [자세히 알아보기](../discover/using/discovering-the-interface.md#supported-languages-languages)

**활성 프로필 모니터링**

* 이제 조직에 대해 권한이 부여된 활성 프로필 수와, 여러 인스턴스를 사용하는 경우 조직 전체에서 사용하는 모든 인스턴스 내 총 프로필 수를 모니터링할 수 있습니다. [자세히 알아보기](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 레코드**

* 이제 여러 이메일 주소에서 집계 보고서 및 오류 보고서 이메일을 받을 수 있습니다. [자세히 알아보기](../subdomains-certificates/using/dmarc.md)
* 한 하위 도메인에 대해 DMARC와 BIMI 레코드 모두 있는 경우의 작업 조건을 변경했습니다.

   * DMARC 레코드는 삭제할 수 없습니다. 삭제하려면 먼저 BIMI 레코드를 삭제해야 합니다.
   * DMARC 레코드를 편집할 수는 있지만 “없음”으로 다운그레이드하는 정책은 허용되지 않으며 해당 백분율 값은 100이어야 합니다.

