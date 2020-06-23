---
title: 새 하위 도메인 설정
description: Campaign 인스턴스용 새 하위 도메인을 설정하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 81%

---


# 새 하위 도메인 설정 {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="새 하위 도메인 설정 및 인증서 관리"
>abstract="Adobe Campaign을 사용하여 이메일 전송을 시작하거나 랜딩 페이지를 게시하려면 새 하위 도메인을 설정하고 하위 도메인의 SSL 인증서를 관리해야 합니다."
>additional-url="https://docs.adobe.com/content/help/ko-KR/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="하위 도메인의 SSL 인증서를 모니터링하는 방법"

>[!IMPORTANT]
>
>컨트롤 패널의 하위 도메인 위임 기능은 베타로 제공되며, 별도의 고지 없이 자주 업데이트 및 수정될 수 있습니다.

## 전체 하위 도메인 위임 {#full-subdomain-delegation}

컨트롤 패널에서는 하위 도메인을 Adobe Campaign에 완전히 위임할 수 있습니다. 이렇게 하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Subdomains & Certificates]** 카드에서 원하는 프로덕션 인스턴스를 선택하고 **[!UICONTROL Setup new subdomain]**&#x200B;을 클릭합니다.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >**프로덕션** 인스턴스의 경우에만 하위 도메인을 위임할 수 있습니다.
   >
   >선택한 인스턴스에 이전에 구성한 하위 도메인이 없는 경우 Adobe에 위임하는 첫 번째 하위 도메인이 해당 인스턴스의 **주 하위 도메인**&#x200B;으로 설정되며, 주 하위 도메인은 나중에 변경할 수 없습니다. 주 하위 도메인을 사용하는 다른 하위 도메인용으로 역방향 DNS 레코드가 작성됩니다. 다른 하위 도메인용 회신 주소 및 바운스 주소는 주 하위 도메인에서 생성됩니다.

1. **[!UICONTROL Next]**&#x200B;을 클릭하여 전체 위임 방법을 확인합니다.

   Note that [CNAME](#use-cnames) and custom methods are currently not supported by the Control Panel.

   ![](assets/subdomain3.png)

1. 조직에서 사용하는 호스팅 솔루션에서 원하는 하위 도메인 및 이름 서버를 만듭니다. 이렇게 하려면 마법사에 표시된 Adobe Nameserver 정보를 복사하여 붙여넣습니다. 호스팅 솔루션에서 하위 도메인을 만드는 방법에 대한 자세한 내용은 [튜토리얼 비디오](https://video.tv.adobe.com/v/30175?captions=kor)를 참조하십시오.

   >[!IMPORTANT]
   >
   >이름 서버를 구성할 때는 **루트 하위 도메인을 Adobe에 위임하면 안 됩니다**. 루트 하위 도메인을 위임하면 해당 도메인을 Adobe에서만 사용할 수 있으며, 조직 직원에게 내부 이메일을 전송하는 등의 기타 용도에는 사용할 수 없습니다.
   >
   >또한 이 새 하위 도메인용으로 **별도의 영역 파일을 만들면 안 됩니다**.

   ![](assets/subdomain4.png)

1. 해당 Adobe 이름 서버 정보를 사용하여 하위 도메인을 만든 후 **[!UICONTROL Next]**&#x200B;을 클릭합니다.

1. 하위 도메인용으로 원하는 사용 사례를 선택합니다.

   * **마케팅 커뮤니케이션**: 상업적 메시지 전송용 하위 도메인으로 설정합니다. 영업 이메일 캠페인 등을 예로 들 수 있습니다.
   * **거래 및 운영 커뮤니케이션**: 거래 커뮤니케이션에는 수신자가 시작한 프로세스를 완료하는 데 필요한 정보가 포함됩니다. 구매 확인, 암호 재설정 이메일 등을 예로 들 수 있습니다. 조직 커뮤니케이션은 상업적 목적 없이 조직 내/외부에서 정보, 아이디어, 견해 등을 교환하는 과정에서 사용됩니다.
   ![](assets/subdomain5.png)

   **메시지 배달 가능성을 높이려면 사용 사례에 따라 하위 도메인을 구분하는 것이 좋습니다**. 이렇게 하면 각 하위 도메인의 평판을 독립적으로 보호할 수 있습니다. 예를 들어, 마케팅 커뮤니케이션을 위한 하위 도메인이 인터넷 서비스 제공자에 의해 차단 목록에 추가되면, 트랜잭션 커뮤니케이션 하위 도메인은 영향을 받지 않고 통신을 계속 전송할 수 있게 됩니다.

   **하위 도메인 하나를 마케팅 및 거래 사용 사례 둘 다에 활용하도록 위임**&#x200B;할 수 있습니다.

   * 마케팅 사용 사례의 경우 하위 도메인은 **MID**(미드 소싱) 인스턴스에 구성됩니다.
   * 거래 사용 사례의 경우 연결을 보장하기 위해 모든 **RT**(메시지 센터/실시간 메시징) 인스턴스에 하위 도메인이 구성됩니다. 따라서 하위 도메인이 모든 RT 인스턴스와 연동됩니다.
   >[!NOTE]
   >
   >Campaign Classic을 사용하는 경우 컨트롤 패널에서 현재 사용 중인 마케팅 인스턴스에 연결된 RT/MID 인스턴스를 확인할 수 있습니다. 자세한 내용은 인스턴스 세부 정보 [섹션을](../../instances-settings/using/instance-details.md) 참조하십시오.

1. 만든 하위 도메인을 호스팅 솔루션에 입력하고 **[!UICONTROL Submit]**&#x200B;을 클릭합니다.

   위임할 하위 도메인의 **전체 이름** 을 입력해야 합니다. 예를 들어 &quot;usoffers.email.weretail.com&quot; 하위 도메인을 위임하려면 &quot;usoffers.email.weretail.com&quot;을 입력합니다.

   ![](assets/subdomain6.png)

1. 하위 도메인을 제출하면 컨트롤 패널에서 이 하위 도메인이 Adobe NS 레코드를 올바르게 가리키는지와 이 하위 도메인에 해당하는 SOA(권한 시작) 레코드가 없는지를 확인합니다.

   >[!NOTE]
   >
   >하위 도메인 위임을 실행하는 동안에는 성능 문제를 방지하기 위해 컨트롤 패널을 통해 제출하는 다른 요청은 큐에 저장되며 하위 도메인 위임이 완료된 후에만 수행됩니다.

1. 이 두 가지 사항이 정상적으로 확인되면 컨트롤 패널에서 DNS 레코드, 추가 URL, 받은 편지함 등을 사용하여 하위 도메인 설정을 시작합니다.

   ![](assets/subdomain7.png)

   결국, **배달능력 팀은** 새로운 하위 도메인을 감사하기 위해 통보 받게 됩니다. 감사 프로세스는 하위 도메인이 위임된 후 영업일 기준으로 최대 10일이 소요될 수 있습니다. 이 프로세스에서는 피드백 루프, 스팸 위반 루프 테스트 등의 확인이 수행됩니다. 그러므로 감사가 완료되기 전에는 하위 도메인을 사용하지 않는 것이 좋습니다. 감사 완료 전에 하위 도메인을 사용하면 하위 도메인 평판이 낮아질 수 있기 때문입니다.

   **[!UICONTROL Process details]** 버튼을 클릭하면 구성 진행 상황을 자세히 확인할 수 있습니다.

   ![](assets/subdomain_audit.png)

   **문제 해결:**

   * 위임은 진행되지만 하위 도메인이 올바르게 확인되지 않는 경우도 있습니다. 하위 도메인은 오류에 대한 정보를 제공하는 작업 로그와 함께 **[!UICONTROL Configured]** 목록에 유지됩니다. 이 문제를 해결하기가 어렵다면 고객 지원 센터에 문의하십시오.
   * 구성 후 하위 도메인이 &quot;확인되지 않음&quot;으로 표시되는 경우 새 하위 도메인 확인을 시작합니다(**...** /) **[!UICONTROL Verify subdomain]**. 여전히 동일한 상태를 표시하는 경우 받는 사람 스키마에 대해 일부 사용자 지정이 수행되므로 표준 프로세스를 사용하여 확인할 수 없습니다. 해당 하위 도메인이 있는 캠페인을 보내십시오.
   * 전달 능력 감사 단계에서 하위 도메인 구성이 너무 오래(영업일 기준 10일 이상) 걸리면 고객 지원 센터에 문의하십시오.

프로세스가 종료되면 하위 도메인이 Adobe Campaign 인스턴스에서 사용 가능하도록 구성되며, 아래 요소가 작성됩니다.

* SOA, MX, CNAME, DKIM, SPF, TXT **DNS 레코드가 포함된 하위 도메인**
* 미러, 리소스, 추적 페이지 및 도메인 키 호스팅을 위한 **추가 하위 도메인**
* **받은 편지함**(보낸 사람, 오류, 회신)

   기본적으로 컨트롤 패널의 &quot;회신&quot; 받은 편지함은 이메일을 지우도록 구성되므로 이메일 검토가 불가능합니다. 마케팅 캠페인용 &quot;회신&quot; 받은 편지함을 모니터링하려는 경우에는 이 주소를 사용하지 마십시오.

**[!UICONTROL Subdomain details]** 및 **[!UICONTROL Sender info]** 버튼을 클릭하면 하위 도메인 세부 사항을 확인할 수 있습니다.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## CNAME 사용 {#use-cnames}

컨트롤 패널을 통해 하위 도메인 위임에 CNAME을 사용하는 방식은 지원되지 않습니다. 이 방법을 사용하려면 Adobe 고객 지원 센터에 문의하십시오.

**관련 항목:**

* [하위 도메인 위임(튜토리얼 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [하위 도메인 브랜딩](../../subdomains-certificates/using/subdomains-branding.md)
* [하위 도메인 모니터링](../../subdomains-certificates/using/monitoring-subdomains.md)