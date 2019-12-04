---
title: 하위 도메인의 SSL 인증서 관리
description: 하위 도메인의 SSL 인증서를 모니터링하고 갱신 프로세스를 시작하는 방법 살펴보기
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# 하위 도메인의 SSL 인증서 관리 {#managing-subdomains-ssl-certificates}

이 **[!UICONTROL Subdomains and Certificates]** 카드를 사용하면 SSL 인증서가 설치된 상태로 랜딩 페이지와 리소스를 호스팅하는 하위 도메인 및 하위 도메인을 확인할 수 있습니다. 만료될 인증서를 예상할 수 있도록 만료되는 하위 도메인을 쉽게 확인할 수도 있습니다.

인증서가 만료될 예정이면 모든 필수 정보가 포함된 고객 지원 요청을 시작하여 인증서를 갱신하고 인스턴스의 적절한 기능을 보장할 수 있습니다.

>[!NOTE]
>
>Adobe는 **만료 날짜가 가까워지면** 관련 하위 도메인의 SSL 인증서를 갱신하는 것을 권장합니다. 조직에 따라 인증서를 갱신하는 데 며칠이 걸릴 수 있으므로 이 프로세스에 적절한 시간을 할당하는 것이 좋습니다.

## SSL 인증서 모니터링 {#monitoring-ssl-certificates}

각 인스턴스에 대한 하위 도메인 목록은 **[!UICONTROL Subdomains & Certificates]** 카드를 선택할 때 직접 액세스할 수 있습니다.

하위 도메인은 SSL 인증서의 가장 가까운 만료 날짜별로 배열되며 만료 날짜(일)에 대한 시각적 정보를 제공합니다.

* **녹색**:다음 60일 이내에 하위 도메인이 만료되지 않았습니다.
* **주황**:하나 이상의 하위 도메인에 다음 60일 이내에 만료되는 인증서가 있습니다.
* **빨간색**:하나 이상의 하위 도메인에 다음 30일 이내에 만료되는 인증서가 있습니다.

![](assets/visual_alert2.png)

To get more details on a subdomain's certificates, click the **[!UICONTROL Certificate Details]** button.

![](assets/certificate_details4.png)

모든 관련 하위 도메인 목록이 인증서에 표시됩니다. 일반적으로 랜딩 페이지, 리소스 페이지 등의 하위 도메인을 포함합니다.

![](assets/monitoring_subdomains_details2.png)

필요한 경우 이 창에서 인증서 갱신 요청을 시작할 수 있습니다. 자세한 내용은 아래 섹션을 참조하십시오.

## SSL 인증서 갱신 시작 {#initiating-ssl-certificate-renewal}

>[!NOTE]
>
>제어판은 인증서 갱신을 자동으로 관리하지 않습니다. Adobe Campaign 고객 지원 센터로 보낼 요청을 준비하기만 하면 갱신 절차를 **시작할** 수 있습니다.

SSL 인증서 갱신 프로세스에는 다음 3단계가 포함됩니다.

1. **CSR(Certificate Signing Request)**&#x200B;의 생성 Adobe Customer Care는 고객 지원 포털을 통해 요청하여 CSR을 생성합니다. CSR을 생성하는 데 필요한 일부 정보(일반 이름, 조직명 및 주소 등)를 제공해야 합니다. 제어판에서 갱신 프로세스를 시작할 때 필요한 항목 목록을 볼 수 있습니다. 자세한 내용은 아래 섹션을 참조하십시오.
1. **SSL 인증서**&#x200B;구매 고객 지원 센터에서 CSR을 생성하고 나면, 이를 다운로드하여 회사가 승인한 인증 기관에서 SSL 인증서를 구입할 수 있습니다.
1. **SSL 인증서**&#x200B;설치SSL 인증서를 구입하면 Adobe 고객 지원 센터에 제공해야 합니다. 인증서가 설치되고 제어판에 업데이트된 인증서 만료 날짜가 표시됩니다.

제어판에서 SSL 인증서 갱신을 시작하려면 다음 단계를 수행합니다.

1. Open the **[!UICONTROL Subdomains & Certificates]** card, then click the **[!UICONTROL Certificate details]** icon of the subdomain with expiring certificates.

   ![](assets/renewal1.png)

1. 관련 하위 도메인 목록이 표시됩니다. 일반적으로 랜딩 페이지, 리소스 페이지 등의 하위 도메인이 포함됩니다.
Click the **[!UICONTROL Ticket Details]** button to initiate the certificates renewal process.

   ![](assets/renewal2.png)

1. SSL 인증서를 갱신하는 데 필요한 모든 세부 사항과 함께 양식이 표시됩니다. 요청된 정보를 완전하고 정확하게 입력해야 합니다(필요한 경우 내부 팀, 보안 및 IT 팀에 문의). 그렇지 않으면 인증서 서명 요청을 생성할 수 없으므로 인증서를 갱신할 수 없습니다.

   * **[!UICONTROL IMS Org]**:조직의 ID입니다.
   * **[!UICONTROL Instance]**:하위 도메인과 연결된 캠페인 인스턴스의 URL입니다.
   * **[!UICONTROL Common name]**:이것은 일반적으로 만료 인증서가 있는 하위 도메인과 연결된 추적 하위 도메인 URL입니다.
   * **[!UICONTROL Subdomains]**:만료 인증서가 있는 하위 도메인에 연결된 하위 도메인. 단일 SSL 인증서를 다른 하위 도메인에 적용하려면 이 목록에 추가할 수 있습니다. 이러한 경우 해당 하위 도메인이 동일한 IMS 조직 및 인스턴스 URL과 연결되어 있는지 확인합니다.
   >[!CAUTION]
   >
   >The **[!UICONTROL IMS Org]** and **[!UICONTROL Instance]** fields are filled in automatically by the Control Panel and should not be modified.

   ![](assets/renewal3.png)

1. 양식이 완료되면 **[!UICONTROL Copy Details]** 단추를 클릭하여 정보를 클립보드에 저장합니다.

   >[!NOTE]
   >
   >브라우저 내역을 지우지 않으면 입력한 정보가 저장되므로 나중에 인증서를 갱신하는 데 사용할 수 있습니다.

1. 단추를 **[!UICONTROL Log new ticket]** 클릭합니다. Adobe Campaign 고객 지원 로그인 페이지로 자동 리디렉션됩니다.

   ![](assets/renewal4.png)

1. 로그인한 다음 "SSL 인증서 CSR 요청" 제목으로 새 지원 티켓을 만듭니다.
이전에 복사한 모든 정보를 티켓 본문에 붙여 넣은 다음 제출을 클릭합니다.

   >[!NOTE]
   >
   >조직에 대한 지원 사례를 제출할 권한이 없는 경우 클립보드에 복사한 모든 정보를 지원 담당자에게 전달하여 새로운 고객 지원 티켓을 개설하도록 요청하십시오.

**관련 항목:**

* [Campaign Standard 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-ssl-certificates.html)
* [Campaign Classic 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-ssl-certificates.html)
