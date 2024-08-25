---
product: campaign
solution: Campaign
title: 키 관리
description: SFTP 서버에 연결하기 위해 키를 관리하는 방법 알아보기
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 키 관리 {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="공개 키 관리 정보"
>abstract="이 탭에서는 공개 키를 생성, 관리 및 편집합니다."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="데모 비디오 시청"

Adobe는 모든 고객에게 **공개 및 개인 키 쌍**&#x200B;을 사용하여 SFTP 서버에 연결할 것을 권장합니다.

아래에서는 공개 SSH 키를 생성한 다음 SFTP 서버 액세스를 위해 추가하는 단계와, 인증 관련 권장 사항에 대해 설명합니다.

서버 액세스를 설정한 후에는 해당 서버에 연결할 수 있도록 **서버 액세스 권한이 필요한 IP 주소를 허용 목록에 추가**&#x200B;해야 합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../instances-settings/using/ip-allow-listing-instance-access.md)을 참조하십시오.

![](assets/do-not-localize/how-to-video.png) 이 비디오에서 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html?lang=ko#sftp-management) 또는 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=ko#sftp-management)를 사용하여 해당 기능 살펴보기

## 모범 사례 {#best-practices}

**공개 SSH 키**

항상 동일한 인증을 사용하여 서버에 연결하고 키에 지원되는 형식을 사용해야 합니다.

**사용자 이름 및 암호와 API 통합**

매우 드문 경우이지만 일부 SFTP 서버에서는 암호 기반 인증이 활성화됩니다. Adobe에서는 키 기반 인증을 사용할 것을 권장합니다. 이 방법이 더 효율적이고 안전하기 때문입니다. 고객 지원 센터에 연락하여 키 기반 인증으로의 전환을 요청할 수 있습니다.

>[!IMPORTANT]
>
>암호가 만료되면 시스템에 키가 설치되어 있어도 SFTP 계정에 로그인할 수 없습니다.

## SSH 키 설치 {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="공개 키 추가"
>abstract="인스턴스에 대한 공개 SSH 키를 생성하고 컨트롤 패널에 추가하여 SFTP 서버에 액세스합니다."

>[!IMPORTANT]
>
>항상 SSH 키와 관련된 조직 지침을 따라야 합니다. 아래 단계는 SSH 키 생성을 수행하는 방법의 한 예일 뿐이며 팀이나 내부 네트워크 그룹에 요구 사항을 전달하는 데 유용한 참조 지점으로 활용할 수 있습니다.

1. **[!UICONTROL 키 관리]** 탭으로 이동한 다음 **[!UICONTROL 새 공개 키 추가]** 버튼을 클릭합니다.

   ![](assets/key0.png)

1. 대화 상자가 열리면 공개 키를 만들 사용자 이름과 키를 활성화할 서버를 선택합니다.

   ![](assets/key1.png)

   >[!NOTE]
   >
   >컨트롤 패널은 특정 사용자 이름이 특정 인스턴스에서 활성화되어 있는지 확인하고 하나 또는 여러 인스턴스에서 키를 활성화할 수 있도록 합니다.
   >
   >각 사용자에 대해 공개 SSH 키를 하나 이상 추가할 수 있습니다.

1. 공개 키를 더 잘 관리하기 위해 각 키의 사용 기간을 설정할 수 있습니다. 이렇게 하려면 **[!UICONTROL 유형]** 드롭다운 목록에서 단위를 선택하고 해당 필드에서 기간을 정의합니다. 공개 키 만료에 대한 자세한 내용은 [이 섹션](#expiry)을 참조하십시오.

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >기본적으로 **[!UICONTROL 유형]** 필드는 **[!UICONTROL 무제한]**&#x200B;으로 설정되어 있으며 이는 공개 키가 만료되지 않음을 의미합니다.

1. **[!UICONTROL 주석]** 필드에 이 공개 키를 추가하는 이유(왜, 누구를 위한 것인지 등)를 표시할 수 있습니다.

1. **[!UICONTROL 공개 키]** 필드를 입력하려면 공개 SSH 키를 생성해야 합니다. 사용 중인 운영 체제에 따라 아래 단계를 수행하십시오.

   **Linux 및 Mac:**

   Terminal을 사용하여 공개 키와 개인 키 쌍을 생성합니다.
   1. 다음 명령을 입력합니다. `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. 메시지가 표시되면 키의 이름을 입력합니다. .ssh 디렉토리는 없는 경우 자동으로 생성됩니다.
   1. 메시지가 표시되면 암호를 입력하고 다시 입력합니다. 암호는 비워 두어도 됩니다.
   1. 키 쌍 &quot;name&quot; 및 &quot;name.pub&quot;가 생성됩니다. &quot;name.pub&quot; 파일을 검색한 다음 엽니다. 이 파일에는 지정한 이메일 주소로 끝나는 영숫자 문자열이 있어야 합니다.

   **Windows:**

   동일한 “name.pub” 형식의 개인/공개 키 쌍을 생성하는 데 사용할 수 있는 서드파티 도구를 설치해야 할 수 있습니다.

1. .pub 파일을 열고 “ssh...”로 시작하는 전체 문자열을 복사하여 컨트롤 패널에 붙여넣습니다.

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >**[!UICONTROL 공개 키]** 필드는 OpenSSH 형식만 허용합니다. 공개 SSH 키 크기는 **2048비트**&#x200B;여야 합니다.

1. 키를 생성하려면 **[!UICONTROL 저장]** 버튼을 클릭합니다. 컨트롤 패널에서 공개 키 및 연결된 지문(SHA256 형식으로 암호화됨)이 저장됩니다. 

>[!IMPORTANT]
>
>생성한 키가 이전에 선택한 SFTP 서버에 연결된 적이 없는 시스템과의 연결을 설정하는 데 사용되는 경우, SFTP 서버에서 이 시스템을 사용하려면 먼저 해당 시스템의 공개 IP를 허용 목록에 추가해야 합니다. [이 섹션](ip-range-allow-listing.md)을 참조하십시오.

지문을 사용하면 컴퓨터에 저장된 개인 키와 컨트롤 패널에 저장된 해당 공개 키의 일치 여부를 확인할 수 있습니다.

![](assets/fingerprint_compare.png)

“**...**” 버튼을 사용하면 기존 키를 삭제하거나 연결된 지문을 클립보드에 복사할 수 있습니다.

![](assets/key_options.png)

## 공개 키 관리 {#managing-public-keys}

생성한 공개 키는 **[!UICONTROL 키 관리]** 탭에 표시됩니다.

만든 날짜 또는 편집 날짜, 항목을 만들거나 편집한 사용자 및 IP 범위 만료일을 기준으로 항목을 정렬할 수 있습니다.

이름 또는 주석을 입력하여 공개 키를 검색할 수도 있습니다.

![](assets/control_panel_key_management_sort.png)

하나 이상의 IP 범위를 편집하려면 [이 섹션](#editing-public-keys)을 참조하십시오.

목록에서 하나 이상의 공개 키를 삭제하려면 해당 공개 키를 선택한 다음 **[!UICONTROL 공개 키 삭제]** 버튼을 클릭합니다.

![](assets/control_panel_delete_key.png)

### 만료 {#expiry}

**[!UICONTROL 만료]** 열에는 공개 키가 만료될 때까지 남은 일수가 표시됩니다.

[이메일 경고](../../performance-monitoring/using/email-alerting.md)를 구독한 경우 공개 키가 만료되기 10일 전, 5일 전 및 만료 예정일에 이메일로 알림을 받게 됩니다. 경고를 받으면 [공개 키를 편집](#editing-public-keys)하여 필요한 경우 유효 기간을 연장할 수 있습니다.

만료된 공개 키는 7일 후 자동으로 삭제됩니다. **[!UICONTROL 만료]** 열에 **[!UICONTROL 만료]**&#x200B;로 표시됩니다. 7일 기간 내:

* 만료된 공개 키는 더 이상 SFTP 서버에 연결하는 데 사용할 수 없습니다.

* 만료된 공개 키를 [편집](#editing-public-keys)하고 기간을 업데이트하여 다시 사용할 수 있도록 할 수 있습니다.

* 목록에서 삭제할 수 있습니다.

## 공개 키 편집 {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="공개 키 편집"
>abstract="선택한 공개 키를 업데이트하여 SFTP 서버에 액세스합니다."

공개 키를 편집하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>컨트롤 패널 2021년 10월 릴리스 이후 생성된 공개 키만 편집할 수 있습니다.

1. **[!UICONTROL 키 관리]** 목록에서 하나 이상의 항목을 선택합니다.
1. **[!UICONTROL 공개 키 업데이트]** 버튼을 클릭합니다.

   ![](assets/control_panel_edit_key.png)

1. 공개 키 만료를 편집하거나 새 주석을 추가할 수만 있습니다.

   >[!NOTE]
   >
   >OpenSSH 형식의 사용자 이름, 인스턴스 및 공개 키를 수정하려면 공개 키를 삭제하고 필요에 따라 새 공개 키를 만듭니다.

1. 변경 내용을 저장합니다.
