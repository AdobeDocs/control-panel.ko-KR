---
product: campaign
solution: Campaign
title: SFTP 서버에 로그인
description: SFTP 서버에 로그인하는 방법 알아보기
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SFTP 서버에 로그인 {#logging-into-sft-server}

아래 단계에서는 SFTP 클라이언트 애플리케이션을 통해 SFTP 서버를 연결하는 방법을 자세히 설명합니다.

![](assets/do-not-localize/how-to-video.png) [&#x200B; 비디오에서 이 기능 살펴보기](https://video.tv.adobe.com/v/34787?quality=12&captions=kor)

서버에 로그인하기 전에 다음을 확인하십시오.

* SFTP 서버는 **Adobe에서 호스팅**&#x200B;합니다.
* 서버에 **사용자 이름**&#x200B;이 설정되었습니다. 컨트롤 패널에 있는 SFTP 카드의 **키 관리** 탭에서 정보를 직접 확인할 수 있습니다.
* SFTP 서버에 로그인하려면 **개인 및 공개 키 쌍**&#x200B;이 있어야 합니다. SSH 키를 추가하는 방법에 대한 자세한 내용은 [이 섹션](../../sftp/using/key-management.md)을 참조하십시오.
* **공개 IP 주소가 SFTP 서버의 허용 목록에 추가**&#x200B;되었습니다. 그렇지 않은 경우 IP 범위를 허용 목록에 추가하는 방법에 대한 자세한 내용은 [이 섹션](../../sftp/using/ip-range-allow-listing.md)을 참조하십시오.
* **SFTP 클라이언트 소프트웨어**&#x200B;에 액세스할 수 있습니다. IT 부서에서 사용을 권장하는 SFTP 클라이언트 애플리케이션에 대해 문의하거나 회사 정책에서 허용하는 경우 인터넷에서 검색할 수 있습니다.

SFTP 서버에 연결하려면 다음 단계를 따르십시오.

1. 컨트롤 패널을 실행한 다음 **[!UICONTROL SFTP]** 카드에서 **[!UICONTROL 키 관리]** 탭을 선택합니다.

   ![](assets/sftp_card.png)

1. SFTP 클라이언트 애플리케이션을 시작한 다음 컨트롤 패널에서 서버 주소를 복사하여 붙여넣은 다음 &quot;campaign.adobe.com&quot;을 선택하고 사용자 이름을 입력합니다.

   ![](assets/do-not-localize/connect1.png)

1. **[!UICONTROL SSH 개인 키]** 필드에서 컴퓨터에 저장된 개인 키 파일을 선택합니다. 이는 &quot;.pub&quot; 확장자(예: &quot;enable&quot;) 없이 공개 키와 이름이 동일한 텍스트 파일에 해당합니다.

   ![](assets/do-not-localize/connect2.png)

   **[!UICONTROL 암호]** 필드는 파일의 개인 키로 자동으로 채워집니다.

   ![](assets/do-not-localize/connect3.png)

   개인 또는 공개 키의 지문을 SFTP 카드의 키 관리 탭에 나타나는 키의 지문과 비교하여 사용하려는 키가 컨트롤 패널에 저장되었는지 확인할 수 있습니다.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Mac 컴퓨터를 사용하는 경우 다음 명령을 실행하여 컴퓨터에 저장된 개인 키의 지문을 볼 수 있습니다.
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 모든 정보를 입력한 후 **[!UICONTROL 연결]**&#x200B;을 클릭하여 SFTP 서버에 로그인합니다.

   ![](assets/do-not-localize/sftpconnected.png)
