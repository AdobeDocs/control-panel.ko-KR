---
product: campaign
solution: Campaign
title: DMARC 레코드 추가
description: 하위 도메인에 대한 DMARC 레코드를 추가하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# DMARC 레코드 추가 {#dmarc}

## DMARC 레코드 {#about}

도메인 기반 메시지 인증, 보고 및 적합성(DMARC)은 조직이 피싱 및 스푸핑 공격으로부터 이메일 도메인을 보호할 수 있도록 도와주는 이메일 인증 프로토콜 표준입니다. 이를 통해 사서함 공급자가 SPF 및 DKIM 검사에 실패한 이메일을 처리하는 방법을 결정할 수 있으므로, 발신자의 도메인을 인증하고 악의적인 목적으로 도메인을 승인하지 않고 사용하는 것을 방지할 수 있습니다.

DMARC 구현에 대한 자세한 내용은 [Adobe 전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html)

## 제한 사항 및 사전 요구 사항 {#limitations}

* SPF 및 DKIM 레코드는 DMARC 레코드를 만들기 위한 사전 요구 사항입니다.
* DMARC 레코드는 전체 하위 도메인 위임을 사용하는 하위 도메인에 대해서만 추가할 수 있습니다. [하위 도메인 구성 방법에 대해 자세히 알아보기](subdomains-branding.md#subdomain-delegation-methods)

## 하위 도메인에 대한 DMARC 레코드 추가 {#add}

하위 도메인에 대한 DMARC 레코드를 추가하려면 다음 단계를 수행합니다.

1. 하위 도메인 목록에서 원하는 하위 도메인 옆에 있는 줄임표 버튼을 클릭하고 을 선택합니다 **[!UICONTROL Subdomain details]**.

1. 다음을 클릭합니다. **[!UICONTROL Add TXT record]** 버튼을 누른 다음 선택 **[!UICONTROL DMARC]** 다음에서 **[!UICONTROL Record Type]** 드롭다운 목록입니다.

   ![](assets/dmarc-add.png)

1. 다음을 선택합니다. **[!UICONTROL Policy Type]** 이메일 중 하나가 실패하면 수신자 서버가 따라야 합니다. 사용 가능한 정책 유형은 다음과 같습니다.

   * **[!UICONTROL None]**,
   * **[!UICONTROL Quarantine]** (스팸 폴더 배치),
   * **[!UICONTROL Reject]** (이메일을 차단합니다).

   DMARC의 잠재적 영향에 대한 DMARC의 이해를 돕기 위해 DMARC 정책을 p=none에서 p=quarantine, p=reject로 상향 조정하여 DMARC 구현을 천천히 롤아웃하는 것이 좋습니다.

   * **1단계:** 받아서 사용하는 피드백을 분석합니다(p=none). 이렇게 하면 수신자는 인증에 실패하는 메시지에 대해 작업을 수행하지 않지만 이메일 보고서를 보낸 사람에게 계속 전송합니다. 또한 합법적인 메시지가 인증에 실패한 경우 SPF/DKIM 문제를 검토하고 수정합니다.

   * **2단계:** SPF 및 DKIM이 정렬되어 모든 합법적인 이메일에 대한 인증을 전달하는지 확인한 다음, 정책을 (p=quarantine)으로 이동하여 수신 이메일 서버에서 인증에 실패한 이메일을 격리합니다(일반적으로 해당 메시지를 스팸 폴더에 배치함). 정책이 격리되도록 설정된 경우 이메일 수의 일부에 대해서만 시작하는 것이 좋습니다.

   * **3단계:** 정책을 (p=reject)로 조정합니다. 참고: 이 정책을 신중하게 사용하고 조직에 적합한지 확인하십시오. p= 거부 정책은 수신자에게 인증에 실패한 도메인에 대한 모든 이메일을 완전히 거부(반송)하도록 지시합니다. 이 정책이 활성화되면 도메인에서 100% 인증된 것으로 확인된 이메일에만 받은 편지함 배치 기회가 생깁니다.

   >[!NOTE]
   >
   > DMARC 레코드 정책 유형이 &quot;없음&quot;으로 설정되어 있으면 BIMI 레코드를 만들 수 없습니다.

1. DMARC 보고서를 받을 이메일 주소를 입력합니다. 이메일 중 하나가 실패하면 DMARC 보고서가 자동으로 선택한 이메일 주소로 전송됩니다.

   * Aggregate-DMARC 보고서는 지정된 기간 동안 실패한 이메일 수와 같은 높은 수준의 정보를 제공합니다.
   * 포렌식 DMARC 실패 보고서는 실패한 이메일의 출처 IP 주소와 같은 자세한 정보를 제공합니다.

1. DMARC 정책이 &quot;없음&quot;으로 설정된 경우 이메일의 100%에 적용되는 백분율을 입력합니다.

   정책이 &quot;거부&quot; 또는 &quot;격리&quot;로 설정된 경우 이메일 중 일부에 대해서만 시작하는 것이 좋습니다. 도메인에서 더 많은 이메일이 수신 서버를 통해 인증을 전달하면 더 높은 비율로 레코드를 느리게 업데이트합니다.

   >[!NOTE]
   >
   >도메인에서 BIMI를 사용하는 경우 DMARC 정책의 백분율 값은 100%여야 합니다. BIMI는 이 값이 100% 미만으로 설정된 DMARC 정책을 지원하지 않습니다.

   ![](assets/dmarc-add2.png)

1. DMARC 보고서는 24시간마다 전송됩니다. 에서 보고서 전송 빈도를 변경할 수 있습니다. **[!UICONTROL Reporting Interval]** 필드. 최소 인증 간격은 1시간이지만 최대 인증 값은 2190시간(즉, 3개월)입니다.

1. 다음에서 **SPF** 및 **[!UICONTROL DKIM Identifier Alignment]** 필드에 이메일에 대한 SPF 및 DKIM 인증을 확인하면서 수신자 서버의 수준을 지정합니다.

   * **[!UICONTROL Relaxed]** 모드: 하위 도메인에서 이메일을 보낸 경우에도 서버가 인증을 수락합니다.
   * **[!UICONTROL Strict]** 발신자 도메인이 SPF 및 DKIM 도메인과 정확히 일치하는 경우에만 모드가 인증을 수락합니다.

   을(를) 사용하여 작업하는 경우 `http://www.luma.com` 도메인. &quot;느슨한&quot; 모드에서 `marketing.luma.com` 하위 도메인은 서버에서 승인되지만, 하위 도메인은 &quot;엄격&quot; 모드에서 거부됩니다.

1. 클릭 **[!UICONTROL Add]** DMARC 레코드 만들기를 확인합니다.

DMARC 레코드 생성이 처리되면(약 5분) 하위 도메인의 세부 정보 화면에 표시됩니다. [하위 도메인의 TXT 레코드를 모니터링하는 방법 알아보기](gs-txt-records.md#monitor)
