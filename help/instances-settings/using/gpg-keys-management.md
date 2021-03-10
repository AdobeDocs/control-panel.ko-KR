---
product: campaign
solution: Campaign
title: GPG 키 관리
description: Adobe Campaign 내에서 데이터를 암호화하고 해독하기 위해 GPG 키를 관리하는 방법을 알아봅니다.
feature: 'Campaign 컨트롤 패널   '
role: 건축가
level: 경험
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 8%

---


# GPG 키 관리 {#gpg-keys-management}

## GPG 암호화 {#about-gpg-encryption} 정보

GPG 암호화를 사용하면 [OpenPGP](https://www.openpgp.org/about/standard/) 사양을 따르는 공개 전용 키 쌍 시스템을 사용하여 데이터를 보호할 수 있습니다.

구현되면 전송 전에 수신 데이터가 암호화되거나 나가는 데이터를 암호화하여 유효한 일치하는 키 쌍 없이는 아무도 이에 액세스하지 못하도록 할 수 있습니다.

Campaign을 사용하여 GPG 암호화를 구현하려면 관리자가 Campaign 컨트롤 패널에서 직접 마케팅 인스턴스에 GPG 키를 설치 및/또는 생성해야 합니다.

그런 다음 다음을 수행할 수 있습니다.

* **보낸 데이터 암호화**:Adobe Campaign은 설치된 공개 키로 암호화한 후 데이터를 보냅니다.

* **들어오는 데이터의 암호를 해독합니다**.Adobe Campaign은 Campaign 컨트롤 패널에서 다운로드한 공개 키를 사용하여 외부 시스템에서 암호화된 데이터를 수신합니다. Adobe Campaign은 Campaign 컨트롤 패널에서 생성된 개인 키를 사용하여 데이터를 해독합니다.

## 데이터 {#encrypting-data} 암호화

Campaign 컨트롤 패널을 사용하면 Adobe Campaign 인스턴스에서 나오는 데이터를 암호화할 수 있습니다.

이렇게 하려면 PGP 암호화 도구에서 GPG 키 쌍을 생성한 다음 공개 키를 Campaign 컨트롤 패널에 설치해야 합니다. 그런 다음 인스턴스에서 데이터를 보내기 전에 데이터를 암호화할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

1. [OpenPGP 사양](https://www.openpgp.org/about/standard/) 다음에 나오는 PGP 암호화 도구를 사용하여 공개/비공개 키 쌍을 생성합니다. 이렇게 하려면 GPG 유틸리티 또는 GNuGP 소프트웨어를 설치합니다.

   >[!NOTE]
   >
   >키를 생성하는 오픈 소스 무료 소프트웨어를 사용할 수 있습니다. 그러나 조직의 지침을 따르고 IT/보안 조직에서 추천하는 GPG 유틸리티를 사용해야 합니다.

1. 유틸리티가 설치되면 Mac Terminal 또는 Windows 명령에서 아래 명령을 실행합니다.

   `gpg --full-generate-key`

1. 메시지가 표시되면 키에 원하는 매개 변수를 지정합니다. 필수 매개 변수는 다음과 같습니다.

   * **키 유형**:RSA
   * **키 길이**:1024 - 4096비트
   * **실제** 이름 및  **이메일 주소**:키 쌍을 만든 사람을 추적할 수 있습니다. 조직 또는 부서에 연결된 이름 및 이메일 주소를 입력합니다.
   * **주석**:주석 필드에 레이블을 추가하면 데이터를 암호화하는 데 사용할 키를 쉽게 식별할 수 있습니다.
   * **만료**:만료 날짜가 없는 날짜 또는 &quot;0&quot;입니다.
   * **암호**

   ![](assets/do-not-localize/gpg_command.png)

1. 스크립트가 확인되면 연결된 지문이 있는 키를 생성하여 파일로 내보내거나 Campaign 컨트롤 패널에 직접 붙여넣을 수 있습니다. 파일을 내보내려면 이 명령을 실행한 다음 생성한 키의 지문을 실행합니다.

   `gpg -a --export <fingerprint>`

1. 공개 키를 Campaign 컨트롤 패널에 설치하려면 **[!UICONTROL Instance settings]** 카드를 연 다음 **[!UICONTROL GPG keys]** 탭 및 원하는 인스턴스를 선택합니다.

1. **[!UICONTROL Install Key]** 버튼을 클릭합니다.

   ![](assets/gpg_install_button.png)

1. PGP 암호화 도구에서 생성된 공개 키를 붙여넣습니다. 내보낸 공개 키 파일을 바로 드래그하여 놓을 수도 있습니다.

   >[!NOTE]
   >
   >공개 키는 OpenPGP 형식이어야 합니다.

   ![](assets/gpg_install_paste.png)

1. **[!UICONTROL Install Key]** 버튼을 클릭합니다.

공개 키가 설치되면 목록에 표시됩니다. **..** 단추를 클릭하여 해당 지문을 다운로드하거나 복사합니다.

![](assets/gpg_install_download.png)

그런 다음 Adobe Campaign 워크플로우에서 키를 사용할 수 있습니다. 데이터 추출 활동을 사용할 때 데이터를 암호화하는 데 사용할 수 있습니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

이 항목에 대한 자세한 내용은 Adobe Campaign 설명서를 참조하십시오.

**Campaign Classic:**

* [파일 압축 또는 암호화](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [사용 사례:Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [암호화된 데이터 관리](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [사용 사례:Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## 데이터 암호 해독 {#decrypting-data}

Campaign 컨트롤 패널을 사용하면 Adobe Campaign 인스턴스로 들어오는 외부 데이터를 해독할 수 있습니다.

이렇게 하려면 Campaign 컨트롤 패널에서 직접 GPG 키 쌍을 생성해야 합니다.

* **공개 키**&#x200B;는 Campaign으로 전송할 데이터를 암호화하는 데 사용하는 외부 시스템과 공유됩니다.
* **개인 키**&#x200B;는 Campaign에서 들어오는 암호화된 데이터를 해독하는 데 사용됩니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

Campaign 컨트롤 패널에서 키 쌍을 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Instance settings]** 카드를 연 다음 **[!UICONTROL GPG keys]** 탭 및 원하는 Adobe Campaign 인스턴스를 선택합니다.

1. **[!UICONTROL Generate Key]** 버튼을 클릭합니다.

   ![](assets/gpg_generate.png)

1. 키 이름을 지정한 다음 **[!UICONTROL Generate Key]**&#x200B;을 클릭합니다. 이 이름은 캠페인 워크플로우에서 암호 해독에 사용할 키를 식별하는 데 도움이 됩니다

   ![](assets/gpg_generate_name.png)

키 쌍이 생성되면 공개 키가 목록에 표시됩니다. 암호 해독 키 쌍은 만료 날짜가 없는 상태로 생성됩니다.

**..** 단추를 클릭하여 공개 키를 다운로드하거나 해당 지문을 복사합니다.

![](assets/gpg_generate_list.png)

공개 키는 외부 시스템과 공유할 수 있습니다. Adobe Campaign은 공개 키로 암호화된 데이터를 해독하기 위해 데이터 로드 활동에 개인 키를 사용할 수 있습니다.

자세한 내용은 Adobe Campaign 설명서를 참조하십시오.

**Campaign Classic:**

* [처리 전 파일 압축 해제 또는 암호 해독](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [사용 사례:Campaign 컨트롤 패널에서 생성된 키를 사용하여 암호화된 데이터 가져오기](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [암호화된 데이터 관리](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [사용 사례:Campaign 컨트롤 패널에서 생성된 키를 사용하여 암호화된 데이터 가져오기](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## GPG 키 모니터링

인스턴스용으로 설치 및 생성된 GPG 키에 액세스하려면 **[!UICONTROL Instance settings]** 카드를 연 다음 **[!UICONTROL GPG keys]** 탭을 선택합니다.

![](assets/gpg_list.png)

목록에는 각 키에 대한 자세한 정보와 함께 해당 인스턴스에 대해 설치 및 생성된 모든 암호화 및 암호 해독 GPG 키가 표시됩니다.

* **[!UICONTROL Name]**:키를 설치하거나 생성할 때 정의된 이름입니다.
* **[!UICONTROL Use case]**:이 열은 키의 사용 사례를 지정합니다.

   ![](assets/gpg_icon_encrypt.png):데이터 암호화를 위해 키가 설치되어 있습니다.

   ![](assets/gpg_icon_decrypt.png):데이터 암호 해독을 허용하도록 키가 생성되었습니다.

* **[!UICONTROL Fingerprint]**:키의 지문.
* **[!UICONTROL Expires]**:키의 만료 날짜입니다. Campaign 컨트롤 패널은 주요 만료 날짜가 다가오면 시각적 표시를 제공합니다.

   * 30일 전에 긴급(빨간색)이 표시됩니다.
   * 경고(노란색)는 60일 전에 표시됩니다.
   * 키가 만료되면 &quot;만료된&quot; 빨간색 배너가 표시됩니다.

   >[!NOTE]
   >
   >Campaign 컨트롤 패널은 이메일 알림을 전송하지 않습니다.

가장 좋은 방법은 더 이상 필요하지 않은 모든 키를 제거하는 것입니다. 이렇게 하려면 **...을 클릭합니다.** 단추를 클릭한 다음 **[!UICONTROL Delete Key].**&#x200B;을 선택합니다.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>키를 제거하기 전에 오류가 발생하지 않도록 Adobe Campaign 작업 과정에 키가 사용되지 않도록 하십시오.

## 자습서 비디오 {#video}

아래 비디오에서는 데이터 암호화에 대한 GPG 키를 생성하고 설치하는 방법을 보여 줍니다.

GPG 키 관리와 관련된 추가 방법 비디오는 [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings) 및 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings) 자습서 페이지에서 사용할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)

