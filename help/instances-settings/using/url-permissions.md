---
title: URL 권한
description: 제어판에서 URL 권한을 관리하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# URL 권한 {#url-permissions}

>[!CAUTION]
>
>이 기능은 Campaign Classic 인스턴스에만 사용할 수 있습니다.

## URL 권한 정보 {#about-url-permissions}

JavaScript 코드(워크플로우 등)에서 호출할 수 있는 URL의 기본 목록 캠페인 클래식 인스턴스는 제한됩니다. 이러한 URL은 인스턴스가 제대로 작동하도록 하는 URL입니다.

기본적으로 인스턴스는 외부 URL에 연결할 수 없습니다. 제어판을 사용하면 외부 URL을 인증된 URL 목록에 추가하여 인스턴스가 URL에 연결할 수 있습니다. 이렇게 하면 파일 및/또는 데이터 전송을 활성화하기 위해 SFTP 서버나 웹 사이트와 같은 외부 시스템에 Campaign 인스턴스를 연결할 수 있습니다.

URL이 추가되면 인스턴스의 구성 파일(serverConf.xml)에서 참조됩니다.

**관련 항목:**

* [캠페인 서버 구성](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [송신 연결 보호](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [URL 권한 추가(자습서 비디오)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## 모범 사례 {#best-practices}

* 연결하지 않을 웹 사이트/서버에 캠페인 인스턴스를 연결하지 마십시오.
* 더 이상 사용하지 않는 URL을 삭제합니다. 그러나 회사의 다른 섹션이 사용자가 삭제한 URL에 계속 연결하는 경우 아무도 다시 사용할 수 없습니다.
* 제어판은 **http**, **https**&#x200B;및 **sftp** 프로토콜을지원합니다. 잘못된 URL 또는 프로토콜을 입력하면 오류가 발생합니다.

## URL 권한 관리 {#managing-url-permissions}

인스턴스에 연결할 수 있는 URL을 추가하려면 다음 단계를 따르십시오.

1. 카드를 **[!UICONTROL Instances Settings]** 열어 탭에 액세스합니다 **[!UICONTROL URL Permissions]** .

   >[!NOTE]
   >
   >인스턴스 설정 카드가 제어판의 홈 페이지에 표시되지 않으면 IMS ORG ID가 Adobe Campaign Classic 인스턴스와 연결되어 있지 않음을 의미합니다.
   >
   >URL <b><span class="uicontrol">권한</span></b> 탭에는 인스턴스가 연결할 수 있는 외부 URL이 모두 나열됩니다. 이 목록에는 Campaign이 작동하는 데 필요한 URL이 포함되지 않습니다(예: 인프라 조각 간 연결).

1. 왼쪽 창에서 원하는 인스턴스를 선택한 다음 **[!UICONTROL Add new URL]** 단추를 클릭합니다.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >모든 Campaign 인스턴스가 왼쪽 창 목록에 표시됩니다.
   >
   >URL 권한 관리는 Campaign Classic 인스턴스에만 적용되므로, Campaign Standard 인스턴스를 선택하면 "적용되지 않는 인스턴스" 메시지가 표시됩니다.

1. 승인할 URL을 관련 프로토콜(http, https 또는 sftp)과 함께 입력합니다.

   >[!NOTE]
   >
   >여러 인스턴스를 인증하여 URL에 연결할 수 있습니다. 이렇게 하려면 첫 번째 문자를 입력하여 인스턴스 필드에서 직접 추가합니다.

   ![](assets/add_url2.png)

1. 이제 목록에 URL이 추가되어 연결할 수 있습니다.

   >[!NOTE]
   >
   >"/.*" 문자는 입력한 페이지의 모든 하위 페이지를 덮기 위해 확인 후 입력한 URL 끝에 자동으로 추가됩니다.

   ![](assets/add_url_listnew.png)

URL을 선택하고 **[!UICONTROL Delete URL]** 단추를 클릭하여 언제든지 삭제할 수 있습니다.

URL을 삭제하면 인스턴스가 다시 호출할 수 없다는 점을 염두에 두십시오.

## 일반적인 질문 {#common-questions}

**새 URL을 추가했지만 인스턴스가 해당 URL에 계속 연결할 수 없습니다. 왜 그럴까.**

경우에 따라, 화이트리스트, 암호 입력 또는 다른 형태의 인증이 필요하도록 연결하려고 하는 URL이 있습니다. 제어판은 추가 인증을 관리하지 않습니다.
