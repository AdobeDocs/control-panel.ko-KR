---
title: 제품 설명서
description: 컨트롤 패널 설명서.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 도움말 센터 {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="컨트롤 패널"
>abstract="컨트롤 패널 홈 페이지에서는 Campaign 인스턴스에서 수행 가능한 모든 작업에 액세스할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=ko" text="컨트롤 패널 액세스"

Campaign [컨트롤 패널]에서는 각 Campaign 인스턴스의 사용량을 추적하고 설정을 관리하여 Campaign Standard와 V7/V8 제품 관리자의 작업 효율성을 높일 수 있습니다.

## 새로운 기능

**사용자 인터페이스**

* [컨트롤 패널]의 지원 언어가 추가되었습니다. [자세히 알아보기](discover/using/discovering-the-interface.md#supported-languages-languages)

**활성 프로필 모니터링**

* 이제 조직에 대해 권한이 부여된 활성 프로필 수와, 여러 인스턴스를 사용하는 경우 조직 전체에서 사용하는 모든 인스턴스 내 총 프로필 수를 모니터링할 수 있습니다. [자세히 알아보기](performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 레코드**

* 이제 여러 이메일 주소에서 집계 보고서 및 오류 보고서 이메일을 받을 수 있습니다. [자세히 알아보기](subdomains-certificates/using/dmarc.md)
* 한 하위 도메인에 대해 DMARC와 BIMI 레코드 모두 있는 경우의 작업 조건을 변경했습니다.

   * DMARC 레코드는 삭제할 수 없습니다. 삭제하려면 먼저 BIMI 레코드를 삭제해야 합니다.
   * DMARC 레코드를 편집할 수는 있지만 “없음”으로 다운그레이드하는 정책은 허용되지 않으며 해당 백분율 값은 100이어야 합니다.

>[!CAUTION]
>
>* 컨트롤 패널은 관리 사용자만 액세스할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=ko#discover-control-panel)
>
>* Campaign v7의 경우 배포 제한이 적용됩니다. [자세히 알아보기](faq.md#v7-restrictions)

## 추가 리소스 {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=ko">컨트롤 패널 튜토리얼 비디오</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=ko">Campaign Standard 제품 설명서</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=ko">컨트롤 패널 튜토리얼 비디오</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=ko">Campaign v7 제품 설명서</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=ko">컨트롤 패널 튜토리얼 비디오</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=ko">Campaign v8 제품 설명서</a></li>
        </ul>
        </td>
    </tr>
</table>
