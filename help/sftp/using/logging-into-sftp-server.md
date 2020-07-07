---
title: SFTP 서버에 로그인
description: SFTP 서버에 로그인하는 방법 학습
translation-type: tm+mt
source-git-commit: f6d75de9c3d92e4f5d0b3d254f103db0901ab20a
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 5%

---


# SFTP 서버에 로그인 {#logging-into-sft-server}

아래 단계는 SFTP 클라이언트 응용 프로그램을 통해 SFTP 서버를 연결하는 방법을 자세히 설명합니다.

서버에 로그인하기 전에 다음을 확인하십시오.

* SFTP 서버는 **Adobe에서 호스팅합니다**.
* 서버에 **사용자 이름**&#x200B;이 설정되었습니다. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* SFTP 서버에 로그인할 **개인 및 공개 키 쌍이** 있습니다. SSH 키를 추가하는 방법에 대한 자세한 내용은 [이 섹션을](../../sftp/using/key-management.md) 참조하십시오.
* 공개 **IP 주소가 SFTP 서버의 허용 목록** 에 추가되었습니다. 그렇지 않은 경우 허용 목록에 IP 범위를 추가하는 방법에 대한 자세한 내용은 [이 섹션을](../../sftp/using/ip-range-allow-listing.md) 참조하십시오.
* SFTP 클라이언트 소프트웨어에 액세스할 수 **있습니다**. 회사 정책에 의해 허용되는 경우 IT 부서에서 사용할 것을 권장하는 SFTP 클라이언트 응용 프로그램을 참조하거나 인터넷에서 검색할 수 있습니다.

SFTP 서버에 연결하려면 다음 단계를 따르십시오.

1. 제어판을 실행한 다음 카드에서 **[!UICONTROL Key Management]** 탭을 **[!UICONTROL SFTP]** 선택합니다.

   ![](assets/sftp_card.png)

1. SFTP 클라이언트 애플리케이션을 실행한 다음 제어판에서 서버 주소를 복사하여 붙여 넣은 다음 &quot;campaign.adobe.com&quot;을 입력한 다음 사용자 이름을 입력합니다.

   ![](assets/do-not-localize/connect1.png)

1. 필드에서 **[!UICONTROL SSH Private Key]** 컴퓨터에 저장된 개인 키 파일을 선택합니다. &quot;.pub&quot; 확장명(예: &quot;enable&quot;) 없이 공개 키와 동일한 이름을 가진 텍스트 파일에 해당합니다.

   ![](assets/do-not-localize/connect2.png)

   이 **[!UICONTROL Password]** 필드는 파일의 개인 키로 자동으로 채워집니다.

   ![](assets/do-not-localize/connect3.png)

   개인 또는 공개 키의 지문을 SFTP 카드의 [키 관리] 탭에 나타나는 키 지문과 비교하여 사용하려는 키가 제어판에 저장되었는지 확인할 수 있습니다.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Mac 컴퓨터를 사용하는 경우 다음 명령을 실행하여 컴퓨터에 저장된 개인 키의 지문을 볼 수 있습니다.
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 모든 정보가 입력되면 을 클릭하여 SFTP 서버 **[!UICONTROL Connect]** 에 로그인합니다.

   ![](assets/do-not-localize/sftpconnected.png)
