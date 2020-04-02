---
title: 새 하위 도메인 설정
description: 캠페인 인스턴스에 대한 새 하위 도메인을 설정하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 43d5d522c29586b9898d924dd164435ee8fbb614

---


# 새 하위 도메인 설정 {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id=&quot;cp_subdomain_management&quot;
>title=&quot;새 하위 도메인 설정 및 인증서 관리&quot;
>abstract=&quot;새 하위 도메인을 설정하고 하위 도메인의 SSL 인증서를 관리해야 이메일 전송을 시작하거나 Adobe Campaign을 사용하여 랜딩 페이지를 게시할 수 있습니다.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html&quot; text=&quot;하위 도메인&#39; SSL 인증서를 모니터링하는 방법&quot;

>[!IMPORTANT]
>
>제어판의 하위 도메인 위임은 베타에서 사용할 수 있으며, 예고 없이 자주 업데이트와 수정이 가능합니다.

## 전체 하위 도메인 위임 {#full-subdomain-delegation}

제어판에서 하위 도메인을 Adobe Campaign에 완전히 위임할 수 있습니다. 이렇게 하려면 아래 절차를 따르십시오.

>[!NOTE]
>
>선택한 인스턴스에 이전에 구성된 하위 도메인이 없는 경우 Adobe에 위임된 첫 번째 하위 도메인이 해당 인스턴스에 대한 **주 하위 도메인이** 되므로 나중에 변경할 수 없습니다.
>
>주 하위 도메인을 사용하는 다른 하위 도메인에 대해 역방향 DNS 레코드가 만들어집니다. 다른 하위 도메인의 회신 주소 및 바운스 주소는 기본 하위 도메인에서 생성됩니다.

1. 카드에서 **[!UICONTROL Subdomains & Certificates]** 원하는 프로덕션 인스턴스를 선택한 다음 을 클릭합니다 **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >하위 도메인 위임은 **프로덕션** 인스턴스에만 사용할 수 있습니다.

1. 전체 위임 방법을 **[!UICONTROL Next]** 확인하려면 을 클릭합니다.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) 및 사용자 지정 메서드는 현재 제어판에서 지원되지 않습니다.

1. 조직에서 사용하는 호스팅 솔루션에서 원하는 하위 도메인 및 이름을 만듭니다. 이렇게 하려면 마법사에 표시된 Adobe Nameserver 정보를 복사하여 붙여 넣습니다. 호스팅 솔루션에서 하위 도메인을 만드는 방법에 대한 자세한 내용은 [자습서 비디오를](https://video.tv.adobe.com/v/30175?captions=kor)참조하십시오.

   >[!IMPORTANT]
   >
   >이름 서버를 구성할 때는 루트 하위 도메인을 Adobe에 위임하지 **않아야 합니다**. 그렇지 않으면 도메인은 Adobe에서만 작동할 수 있습니다. 내부 이메일을 조직의 직원에게 보내는 것과 같은 다른 모든 용도는 불가능합니다.
   >
   >또한 이 새 하위 도메인에 대해 별도의 영역 파일을 **만들지** 마십시오.

   ![](assets/subdomain4.png)

   해당 Adobe 이름 서버 정보가 포함된 하위 도메인이 생성되면 을 클릭합니다. **[!UICONTROL Next]**

1. 하위 도메인에 대해 원하는 사용 사례를 선택합니다.

   * **마케팅 커뮤니케이션**:상업적인 목적을 위한 통신. 예:세일즈 이메일 캠페인
   * **거래 및 운영 커뮤니케이션**:트랜잭션 커뮤니케이션에는 수신자가 귀하를 시작한 프로세스를 완료하기 위한 정보가 포함되어 있습니다. 예:구매 확인, 암호 재설정 이메일. 조직의 커뮤니케이션은 기업 내외부에서 상업적인 목적 없이 정보, 아이디어 및 뷰를 교환하는 것과 관련이 있습니다.
   ![](assets/subdomain5.png)

   **사용 사례에 따라 하위 도메인을 분류하는 것은 전달**&#x200B;시 가장 좋은 방법입니다. 이렇게 하면 각 하위 도메인의 명성은 분리되고 보호됩니다. 예를 들어, 마케팅 커뮤니케이션을 위한 하위 도메인이 인터넷 서비스 제공자에 의해 차단되는 경우, 트랜잭션 커뮤니케이션 하위 도메인은 영향을 받지 않으며 계속해서 커뮤니케이션을 보낼 수 있습니다.

   **마케팅 및 트랜잭션 사용 사례**&#x200B;모두에 대한 하위 도메인을 위임할 수 있습니다.

   * 마케팅 사용 사례의 경우 하위 도메인이 MID(Mid **소싱** ) 인스턴스에 구성됩니다.
   * 트랜잭션 사용 사례의 경우, 연결을 보장하기 위해 하위 도메인이 **ALL** RT(메시지 센터/실시간 메시징) 인스턴스에 구성됩니다. 따라서 하위 도메인은 모든 RT 인스턴스와 함께 작동합니다.
   >[!NOTE]
   >
   >Campaign Classic을 사용하는 경우 제어판에서 작업 중인 Marketing 인스턴스에 연결된 RT/MID 인스턴스를 볼 수 있습니다. For more on this, refer to [this section](../../instances-settings/using/instance-details.md).

1. 호스팅 솔루션에 만든 하위 도메인을 입력한 다음 을 **[!UICONTROL Submit]**&#x200B;클릭합니다.

   위임할 하위 도메인의 **전체 이름을** 입력해야 합니다. 예를 들어 &quot;usoffers.email.weretail.com&quot; 하위 도메인을 위임하려면 &quot;usoffers.email.weretail.com&quot;을 입력합니다.

   ![](assets/subdomain6.png)

1. 하위 도메인이 제출되면 제어판이 Adobe NS 레코드를 올바르게 가리키는지, 이 하위 도메인에 대해 SOA(Start of Authority) 레코드가 없는지 확인합니다.

1. 확인이 성공하면 제어판이 DNS 레코드, 추가 URL, 받은 편지함 등이 있는 하위 도메인 설정을 시작합니다. 이 **[!UICONTROL Process details]** 단추를 클릭하여 구성 진행 상황을 자세히 알 수 있습니다.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >일부 경우 위임이 진행되지만 하위 도메인이 확인되지 않을 수 있습니다. 하위 도메인은 **[!UICONTROL Verified subdomains]** 목록으로 바로 이동하며 **[!UICONTROL Unverified]** 상태와 오류에 대한 정보를 제공하는 작업 로그가 있습니다. 문제를 해결하는 데 문제가 있으면 고객 지원 센터에 문의하십시오.
   >
   >하위 도메인 위임을 실행하는 동안 성능 문제를 방지하기 위해 제어판을 통한 다른 요청은 큐에 입력되고 하위 도메인 위임이 완료된 후에만 수행됩니다.

프로세스가 완료되면 하위 도메인이 Adobe Campaign 인스턴스와 함께 작동하도록 구성되며 아래 요소가 만들어집니다.

* **다음 DNS 레코드가** 있는 **하위 도메인**:SOA, MX, CNAME, DKIM, SPF, TXT,
* **미러, 리소스, 추적 페이지 및 도메인 키를 호스팅할 추가 하위 도메인** ,
* **받은 편지함**:보낸 사람, 오류, 회신.

>[!NOTE]
>
>기본적으로 제어판의 &quot;회신&quot; 받은 편지함은 이메일을 지우도록 구성되며 다시 볼 수 없습니다. 마케팅 캠페인에 대한 &quot;회신&quot; 받은 편지함을 모니터링하려면 이 주소를 사용하지 마십시오.

하위 도메인에 대한 자세한 내용은 **[!UICONTROL Subdomain details]** 및 **[!UICONTROL Sender info]** 단추를 클릭하여 확인할 수 있습니다.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>처리 단계에 따라 Adobe 고객 지원 센터에 문의하여 제공 팀이 생성된 새 하위 도메인을 감사하도록 감사 요청을 받았는지 확인해야 합니다. 감사 프로세스는 하위 도메인을 위임한 후 영업일 기준으로 최대 310일이 소요될 수 있습니다.
>
>수행되는 검사에는 피드백 루프와 스팸 비평 루프 테스트가 포함됩니다. 따라서 감사가 완료되기 전에 하위 도메인을 사용하는 것이 좋지 않은 하위 도메인 명성을 초래할 수 있으므로 권장하지 않습니다.

## CNAME 사용 {#use-cnames}

하위 도메인 위임에 대한 CNAME의 사용은 제어판을 통해 지원되지 않습니다. 이 방법을 사용하려면 Adobe 고객 지원 센터에 문의하십시오.

**관련 항목:**

* [하위 도메인 위임(자습서 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)