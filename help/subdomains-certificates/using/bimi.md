---
product: campaign
solution: Campaign
title: BIMI 레코드 추가
description: 하위 도메인에 대한 BIMI 레코드를 추가하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0ad4c1f12eb035c8d543777be2a8806d507be5be
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# BIMI 레코드 추가 {#dmarc}

## BIMI 레코드 정보 {#about}

BIMI(Brand Indicators for Message Identification)는 업계 표준으로, 승인된 로고가 사서함 공급자의 받은 편지함에 있는 보낸 사람의 이메일 옆에 표시되어 브랜드 인지도와 신뢰를 높일 수 있습니다. DMARC 인증을 통해 발신자의 신원을 확인함으로써 이메일 스푸핑 및 피싱을 방지할 수 있어 악성 행위자가 이메일에서 합법적인 브랜드를 사칭하는 것이 더욱 어려워진다. BIMI 구현에 대한 자세한 내용은 [Adobe 전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## 제한 사항 및 사전 요구 사항 {#limitations}

* BIMI 레코드를 만들기 위한 필수 조건은 SPF, DKIM 및 DMARC 레코드입니다.
* BIMI 레코드는 전체 하위 도메인 위임을 사용하는 하위 도메인에 대해서만 추가할 수 있습니다. [하위 도메인 구성 방법에 대해 자세히 알아보기](subdomains-branding.md#subdomain-delegation-methods)
* DMARC 레코드 사전 요구 사항:

   * 하위 도메인의 레코드 정책 유형은 &quot;격리&quot; 또는 &quot;거부&quot;로 설정되어야 합니다. DMARC 정책 유형이 &quot;없음&quot;으로 설정되어 있으면 BIMI 레코드를 만들 수 없습니다.
   * DMARC 정책이 적용되는 이메일의 비율은 100%여야 합니다. BIMI는 이 비율이 100% 미만으로 설정된 DMARC 정책을 지원하지 않습니다.

[DMARC 레코드 구성 방법 알아보기](dmarc.md)

## 하위 도메인에 대한 BIMI 레코드 추가 {#add}

하위 도메인에 대한 BIMI 레코드를 추가하려면 다음 단계를 수행합니다.

1. 하위 도메인 목록에서 원하는 하위 도메인 옆에 있는 줄임표 버튼을 클릭하고 을 선택합니다 **[!UICONTROL Subdomain details]**.

1. 다음을 클릭합니다. **[!UICONTROL Add TXT record]** 버튼을 누른 다음 선택 **[!UICONTROL BIMI]** 다음에서 **[!UICONTROL Record type]** 드롭다운 목록입니다.

   ![](assets/bimi-add.png)

1. 다음에서 **[!UICONTROL Company Logo URL]**&#x200B;로고가 포함된 SVG 파일의 URL을 지정합니다.

1. 다음 **[!UICONTROL Certificate URL]** 필드는 선택 사항입니다. 이를 통해 스팸 메일 및 기타 악의적인 사용자가 소유하지 않은 브랜드 로고를 사용하지 못하도록 조직이 로고의 법적 소유자임을 입증하는 VMC(Verified Mark Certificate) URL을 추가할 수 있습니다.

   +++VMC를 받으려면 어떻게 해야 합니까?

   VMC를 가져오는 주요 단계는 다음과 같습니다.

   1. VMC 발행자가 인식하는 지적 재산 사무소에 브랜드 로고를 상표로 등록하십시오. 법률 팀이 있는 경우, 해당 팀과 함께 로고 상표가 지정되었거나 이미 상표가 지정되었는지 확인하는 것이 좋습니다.

   1. 로고가 상표가 지정되었는지 확인한 후 DigiCert 또는 인증 기관(CA)에 문의하여 VMC를 요청하십시오.

   1. VMC가 승인되면 엔티티 인증서 PEM(개인 정보 보호 강화 메일) 파일을 받게 됩니다. CA에서 가져온 다른 중간 인증서를 이 PEM 파일에 추가합니다. PEM 파일(추가 파일과 함께)을 공용 웹 서버에 업로드하고 PEM 파일 URL을 기록해 둡니다. BIMI TXT 레코드의 URL을 사용하게 됩니다.

   BIMI 구현에 대한 자세한 내용은 [BIMI 표준 설명서](https://bimigroup.org/implementation-guide/)
+++

1. 클릭 **[!UICONTROL Add]** BIMI 레코드 생성을 확인합니다.

BIMI 레코드 생성이 처리되면(약 5분) 하위 도메인의 세부 정보 화면에 표시됩니다. [하위 도메인의 TXT 레코드를 모니터링하는 방법 알아보기](gs-txt-records.md#monitor)
