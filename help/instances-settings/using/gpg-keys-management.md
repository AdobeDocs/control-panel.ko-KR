---
product: campaign
solution: Campaign
title: GPG 키 관리
description: Adobe Campaign에서 데이터를 암호화하고 해독하기 위해 GPG 키를 관리하는 방법을 알아봅니다.
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 100%

---

# GPG 키 관리 {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="GPG 키 정보"
>abstract="이 탭에서는 Campaign에서 전송된 데이터를 암호화하고 수신되는 데이터를 해독하기 위해 마케팅 인스턴스에 GPG 키를 설치 및/또는 생성합니다."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=ko" text="성능 모니터링 정보"

## GPG 암호화 정보 {#about-gpg-encryption}

GPG 암호화를 사용하면 [OpenPGP](https://www.openpgp.org/about/standard/) 사양을 따르는 공개-개인 키 쌍 시스템을 사용하여 데이터를 보호할 수 있습니다.

구현되면 전송하기 전에 수신 데이터의 암호를 해독하고 전송 데이터를 암호화하여 일치하는 키 쌍이 유효하지 않으면 다른 사람이 해당 데이터에 액세스할 수 없도록 할 수 있습니다.

Campaign을 사용하여 GPG 암호화를 구현하려면 관리자가 컨트롤 패널에서 직접 마케팅 인스턴스에 GPG 키를 설치 및/또는 생성해야 합니다.

그러면 다음을 수행할 수 있습니다:

* **보낸 데이터 암호화**: Adobe Campaign은 설치된 공개 키로 데이터를 암호화한 후 전송합니다.

* **수신 데이터 암호 해독**: Adobe Campaign은 컨트롤 패널에서 다운로드한 공개 키를 사용하여 외부 시스템에서 암호화된 데이터를 수신합니다. Adobe Campaign은 컨트롤 패널에서 생성된 개인 키를 사용하여 데이터의 암호를 해독합니다.

## 데이터 암호화 {#encrypting-data}

컨트롤 패널을 사용하면 Adobe Campaign 인스턴스에서 나오는 데이터를 암호화할 수 있습니다.

이렇게 하려면 PGP 암호화 도구에서 GPG 키 쌍을 생성한 다음 공개 키를 컨트롤 패널에 설치해야 합니다. 그러면 인스턴스에서 전송하기 전에 데이터를 암호화할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

>[!NOTE]
>
>컨트롤 패널에 최대 60개의 GPG 키를 설치할 수 있습니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

1. [OpenPGP 사양](https://www.openpgp.org/about/standard/)에 따라 PGP 암호화 도구를 사용하여 공개/개인 키 쌍을 생성합니다. 이렇게 하려면 GPG 유틸리티 또는 GNuGP 소프트웨어를 설치합니다.

   >[!NOTE]
   >
   >키를 생성하는 오픈 소스 무료 소프트웨어를 사용할 수 있습니다. 단, 조직의 지침을 따르고 IT/보안 조직에서 권장하는 GPG 유틸리티를 사용해야 합니다.

1. 유틸리티가 설치되면 Mac 터미널 또는 Windows 명령에서 아래 명령을 실행합니다.

   `gpg --full-generate-key`

1. 메시지가 표시되면 키에 대해 원하는 매개 변수를 지정합니다. 필수 매개 변수는 다음과 같습니다.

   * **키 유형**: RSA
   * **키 길이**: 3072~4096비트
   * **실명** 및 **이메일 주소**: 누가 키 쌍을 만들었는지 추적할 수 있습니다. 조직 또는 부서에 연결된 이름 및 이메일 주소를 입력합니다.
   * **주석**: 주석 필드에 레이블을 추가하면 데이터를 암호화하는 데 사용할 키를 쉽게 식별할 수 있습니다.
     >[!IMPORTANT]
     >
     >이 필드가 비어 있지 않은지, 주석이 입력되었는지 확인합니다.

   * **만료**: 만료일이 없는 경우 날짜 또는 “0”입니다.
   * **암호**

   ![](assets/do-not-localize/gpg_command.png)

1. 확인되면 스크립트는 연결된 지문이 있는 키를 생성하여 파일로 내보내거나 컨트롤 패널에 직접 붙여넣을 수 있습니다. 파일을 내보내려면 이 명령을 실행한 다음 생성한 키의 지문을 실행합니다.

   `gpg -a --export <fingerprint>`

1. 공개 키를 컨트롤 패널에 설치하려면 **[!UICONTROL 인스턴스 설정]** 카드를 연 다음 **[!UICONTROL GPG 키]** 탭과 원하는 인스턴스를 선택합니다.

1. **[!UICONTROL 키 설치]** 버튼을 클릭합니다.

   ![](assets/gpg_install_button.png)

1. PGP 암호화 도구에서 생성된 공개 키를 붙여넣습니다. 내보낸 공개 키 파일을 직접 끌어다 놓을 수도 있습니다.

   >[!NOTE]
   >
   >공개 키는 OpenPGP 형식이어야 합니다.

   ![](assets/gpg_install_paste.png)

1. **[!UICONTROL 키 설치]** 버튼을 클릭합니다.

공개 키가 설치되면 목록에 표시됩니다. **...** 버튼을 클릭하여 다운로드하거나 지문을 복사합니다.

![](assets/gpg_install_download.png)

그런 다음 Adobe Campaign 워크플로우에서 키를 사용할 수 있습니다. 데이터 추출 활동을 사용할 때 이를 사용하여 데이터를 암호화할 수 있습니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

이 항목에 대한 자세한 내용은 Adobe Campaign 설명서를 참조하십시오.

**Campaign v7/v8:**

* [파일 압축 또는 암호화](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=ko)
* [사용 사례: 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=ko#use-case-gpg-encrypt)

**Campaign Standard:**

* [암호화된 데이터 관리](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=ko)
* [사용 사례: 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=ko#use-case-gpg-encrypt)

## 데이터 복호화 {#decrypting-data}

컨트롤 패널을 사용하면 Adobe Campaign 인스턴스로 들어오는 외부 데이터를 해독할 수 있습니다.

이렇게 하려면 컨트롤 패널에서 직접 GPG 키 쌍을 생성해야 합니다.

* **공개 키**&#x200B;는 외부 시스템과 공유되며 이 키를 사용하여 Campaign으로 보낼 데이터를 암호화합니다.
* **개인 키**&#x200B;는 Campaign에서 수신되는 암호화된 데이터의 암호를 해독하는 데 사용됩니다.

![](assets/do-not-localize/how-to-video.png)[ 비디오에서 이 기능 살펴보기](#video)

컨트롤 패널에서 키 쌍을 생성하려면 다음 단계를 수행하십시오.

1. **[!UICONTROL 인스턴스 설정]** 카드를 연 다음 **[!UICONTROL GPG 키]** 탭과 원하는 Adobe Campaign 인스턴스를 선택합니다.

1. **[!UICONTROL 키 생성]** 버튼을 클릭합니다.

   ![](assets/gpg_generate.png)

1. 키 이름을 지정한 다음 **[!UICONTROL 키 생성]**&#x200B;을 클릭합니다. 이 이름은 Campaign 워크플로우에서 암호 해독에 사용할 키를 식별하는 데 도움이 됩니다.

   ![](assets/gpg_generate_name.png)

키 쌍이 생성되면 공개 키가 목록에 표시됩니다. 암호 해독 키 쌍은 만료 날짜 없이 생성됩니다.

**...** 버튼을 사용하여 공개 키를 다운로드하거나 지문을 복사합니다.

![](assets/gpg_generate_list.png)

그러면 공개 키를 외부 시스템과 공유할 수 있습니다. Adobe Campaign은 데이터 로드 활동에서 개인 키를 사용하여 공개 키로 암호화된 데이터를 해독할 수 있습니다.

자세한 내용은 Adobe Campaign 설명서를 참조하십시오.

**Campaign v7 및 v8:**

* [처리 전 파일 압축 해제 또는 암호 해독](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=ko)
* [사용 사례: 컨트롤 패널에서 생성한 키를 사용하여 암호화된 데이터 가져오기](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=ko#use-case-gpg-decrypt)

**Campaign Standard:**

* [암호화된 데이터 관리](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=ko)
* [사용 사례: 컨트롤 패널에서 생성한 키를 사용하여 암호화된 데이터 가져오기](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=ko#use-case-gpg-decrypt)

## GPG 키 모니터링

인스턴스에 설치 및 생성된 GPG 키에 액세스하려면 **[!UICONTROL 인스턴스 설정]** 카드를 연 다음 **[!UICONTROL GPG 키]** 탭을 선택합니다.

![](assets/gpg_list.png)

이 목록에는 인스턴스에 대해 설치되고 생성된 모든 암호화 및 암호 해독 GPG 키가 각 키에 대한 세부 정보와 함께 표시됩니다.

* **[!UICONTROL 이름]**: 키를 설치하거나 생성할 때 정의된 이름입니다.
* **[!UICONTROL 사용 사례]**: 이 열은 키의 사용 사례를 지정합니다.

  ![](assets/gpg_icon_encrypt.png): 데이터 암호화를 위해 키가 설치되었습니다.

  ![](assets/gpg_icon_decrypt.png): 데이터 암호 해독을 허용하기 위해 키가 생성되었습니다.

* **[!UICONTROL 지문]**: 키의 지문입니다.
* **[!UICONTROL 만료]**: 키의 만료 날짜입니다. 키의 만료 날짜가 가까워지면 컨트롤 패널에서 시각적 표시를 제공합니다.

   * 30일 전에 긴급(빨간색)이 표시됩니다.
   * 경고(노란색)는 60일 전에 표시됩니다.
   * 키가 만료되면 “만료됨” 빨간색 배너가 표시됩니다.

  >[!NOTE]
  >
  >컨트롤 패널은 이메일 알림을 보내지 않습니다.

가장 좋은 방법은 더 이상 필요하지 않은 키를 제거하는 것입니다. 이렇게 하려면 **...** 버튼을 클릭한 다음 **[!UICONTROL 키 삭제].**&#x200B;를 선택하십시오.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>키를 제거하기 전에 실패를 방지하기 위해 어떤 Adobe Campaign 워크플로우에서도 이 키가 사용되지 않는지 확인하십시오.

## 튜토리얼 비디오 {#video}

아래 비디오에서는 데이터 암호화에 대한 GPG 키를 생성하고 설치하는 방법을 보여 줍니다.

GPG 키 관리와 관련된 추가 방법 비디오는 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=ko#instance-settings) 및 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=ko#instance-settings) 튜토리얼 페이지에서 볼 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
