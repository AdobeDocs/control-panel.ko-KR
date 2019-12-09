---
title: 새 하위 도메인 설정
description: 캠페인 인스턴스에 대한 새 하위 도메인을 설정하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# 하위 도메인 설정 {#setting-up-subdomain}

제어판에서 하위 도메인을 Adobe Campaign에 완전히 위임할 수 있습니다. 이렇게 하려면 아래 절차에 따르십시오.

>[!NOTE]
>
>하위 도메인 위임에 대한 CNAME의 사용은 제어판을 통해 지원되지 않습니다. 이 방법에 대한 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)참조하십시오.

1. 카드에서 원하는 인스턴스를 선택한 다음 **[!UICONTROL Subdomains & Certificates]****[!UICONTROL Setup new subdomain]** 단추를 클릭합니다.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >이 **[!UICONTROL Setup new subdomain]**단추는 프로덕션 인스턴스에만 사용할 수 있습니다.

1. 메서드를 **[!UICONTROL Delegation to Adobe]**선택한 다음 을 클릭합니다**[!UICONTROL Next]**.

   ![](assets/subdomain3.png)

1. 조직에서 사용하는 호스팅 솔루션에서 원하는 하위 도메인을 만듭니다. 이렇게 하려면 마법사에 표시된 Adobe Nameserver 정보를 복사한 다음 호스팅 솔루션에 붙여 넣습니다.

   호스팅 솔루션에서 하위 도메인을 만드는 방법에 대한 자세한 내용은 마법사에서 액세스할 수 있는 자습서 비디오를 참조하십시오.

   ![](assets/subdomain4.png)

   해당 Adobe 이름 서버 정보가 포함된 하위 도메인이 생성되면 을 클릭합니다. **[!UICONTROL Next]**

1. 하위 도메인에 대해 원하는 사용 사례를 선택합니다.

   * **마케팅 커뮤니케이션**:상업적인 목적을 위한 통신. 예:세일즈 이메일 캠페인
   * **거래 및 운영 커뮤니케이션**:거래 커뮤니케이션에는 수신자가 귀하에 대해 시작한 프로세스를 완료하기 위한 정보가 포함되어 있습니다. 예:구매 확인, 암호 재설정 이메일. 조직의 커뮤니케이션은 기업 내부 및 외부에서 상업적인 목적 없이 정보, 아이디어 및 뷰를 교환하는 것과 관련이 있습니다.
   이렇게 하위 도메인을 분류하는 것은 배달 가능성을 위한 최선의 방법입니다. 이렇게 하면 각 하위 도메인의 명성은 분리되고 보호됩니다. 예를 들어, 마케팅 커뮤니케이션을 위한 하위 도메인이 인터넷 서비스 제공자에 의해 차단되는 경우, 트랜잭션 커뮤니케이션 하위 도메인은 영향을 받지 않으며 계속해서 커뮤니케이션을 보낼 수 있습니다.

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >인스턴스용으로 구성된 사용 사례만 선택할 수 있습니다. 인스턴스가 &quot;마케팅 커뮤니케이션&quot;에 대해서만 구성된 경우 &quot;거래 및 운영 커뮤니케이션&quot; 사용 사례를 선택할 수 없습니다.

1. Adobe Nameserver 정보를 사용하여 호스팅 솔루션에 생성한 하위 도메인을 입력한 다음 제출을 **[클릭합니다]**.

   >[!NOTE]
   >
   > 위임할 **전체** 하위 도메인을 입력해야 합니다. 예를 들어 &quot;usoffers.email.weretail.com&quot; 하위 도메인을 위임하려면 &quot;usoffers.email.weretail.com&quot;을 입력합니다.

   ![](assets/subdomain6.png)

1. 하위 도메인이 제출되면 제어판은 하위 도메인을 구성하는 다양한 작업을 수행하고 캠페인 인스턴스를 올바로 가리키는지 확인합니다(네임스페이스 레코드 만들기, 캠페인 인스턴스 구성, 권한 시작 레코드 확인 등).

   언제든지 **[!UICONTROL Process details]**단추를 클릭하여 구성 진행 상황을 자세히 볼 수 있습니다.

   ![](assets/subdomain7.png)

이 과정이 끝나면 어떤 결과가 나오나요?
* SOA, MX, CNAME, DKIM, SPF, TXT와 같은 DNS 레코드가 있는 하위 도메인.
* 미러, 리소스, 추적 페이지 및 도메인 키를 호스트할 추가 하위 도메인
* 받은 편지함 - 보낸 사람, 오류, 회신 주소
* 궁극적으로 하위 도메인이 Adobe Campaign 인스턴스와 작동하도록 구성됩니다
