---
title: IP 범위 허용 목록
description: SFTP 서버 액세스를 위한 허용 목록에 IP 범위를 추가하는 방법을 배웁니다.
translation-type: ht
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: ht
source-wordcount: '601'
ht-degree: 100%

---


# IP 범위 허용 목록 {#ip-range-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="IP 허용 목록 정보"
>abstract="이 탭에서 허용 목록에 IP 범위를 추가하여 SFTP 서버에 연결을 설정할 수 있습니다. 여기에는 액세스 권한이 있는 SFTP 서버만 표시됩니다. 다른 SFTP 서버 액세스 권한을 요청하려면 관리자에게 문의하십시오."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="데모 비디오 시청"

SFTP 서버는 보호되어 있으므로 파일을 확인하거나 새 파일을 작성하기 위해 SFTP 서버에 액세스하려면 서버에 액세스하는 클라이언트나 시스템의 공개 IP 주소를 허용 목록에 추가해야 합니다.

## CIDR 형식 {#about-cidr-format}

CIDR(Classless Inter-Domain Routing)은 컨트롤 패널 인터페이스를 사용하여 IP 범위를 추가할 때 지원되는 형식입니다.

CIDR의 구문에는 IP 주소, &#39;/&#39; 문자, 십진수가 차례로 포함됩니다. [이 문서](https://whatismyipaddress.com/cidr)에서 CIDR의 형식과 구문을 자세히 확인할 수 있습니다.

소유한 IP 범위를 CIDR 형식으로 변환하는 데 사용할 수 있는 무료 온라인 도구를 인터넷에서 검색할 수 있습니다.

## 권장사항 {#best-practices}

컨트롤 패널에서 IP 주소를 허용 목록에 추가할 때는 아래 권장 사항과 제한을 따라야 합니다.

* 단일 IP 주소가 아닌 **허용 목록에 IP 범위를 추가합니다**. IP 주소 하나를 허용 목록에 추가하려면 범위에 IP가 하나만 포함되어 있음을 나타내는 &#39;/32&#39;를 추가합니다.
* 예를 들어 265개를 초과하는 IP 주소 포함과 같은&#x200B;**허용 목록에 매우 넓은 범위를 추가하지 마십시오.** /0~/23 사이의 CIDR 형식 범위는 컨트롤 패널에서 거부됩니다.
* **공개 IP 주소**&#x200B;만 허용 목록에 추가할 수 있습니다.
* 허용 목록에서 더 이상 필요하지 않은 **IP 주소를 정기적으로 삭제**&#x200B;해야 합니다.

## 허용 목록에 IP 주소 추가 {#whitelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="새 IP 범위 추가"
>abstract="SFTP 서버에 연결하기 위해 허용 목록에 추가할 IP 범위를 정의합니다."

허용 목록에 IP 범위를 추가하려면 다음 단계를 수행합니다.

1. **[!UICONTROL SFTP]** 카드를 열고 **[!UICONTROL IP Whistelisting]** 탭을 선택합니다.
1. 허용 목록의 IP 주소 목록이 각 인스턴스에 대해 표시됩니다. 왼쪽 목록에서 원하는 인스턴스를 선택하고 **[!UICONTROL Add new IP range]** 버튼을 클릭합니다.

   ![](assets/control_panel_add_range.png)

1. 허용 목록에 추가할 IP 범위를 CIDR 형식으로 정의한 다음 목록에 표시할 레이블을 정의합니다.

   >[!NOTE]
   >
   >레이블 필드에 입력할 수 있는 특수 문자는 다음과 같습니다.
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >IP 범위가 허용 목록의 기존 범위와 겹칠 수 없습니다. IP 범위가 겹치는 경우에는 겹치는 IP가 포함된 범위를 먼저 삭제하십시오.
   >
   >여러 인스턴스에 대해 허용 목록에 범위를 추가할 수 있습니다. 이렇게 하려면 아래쪽 화살표 키를 누르거나 원하는 인스턴스의 첫 번째 문자를 입력한 다음 제안 목록에서 인스턴스를 선택합니다.

   ![](assets/control_panel_add_range3.png)

1. **[!UICONTROL Save]** 버튼을 클릭합니다. 요청이 완전히 처리될 때까지 허용 목록에 추가된 IP가 보류 중으로 표시됩니다. 요청은 몇 초 이내에 처리됩니다.

허용 목록에서 IP 범위를 삭제하려면 해당 범위를 선택한 다음 **[!UICONTROL Delete IP range]** 버튼을 클릭합니다.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>현재 허용 목록에서 범위를 편집할 수 없습니다. IP 범위를 수정하려면 해당 범위를 삭제한 다음 필요에 따라 새로 만듭니다.

## 변경 사항 모니터링 {#monitoring-changes}

컨트롤 패널 홈 페이지의 **[!UICONTROL Job Logs]**&#x200B;에서는 허용 목록에 추가한 IP 주소의 모든 변경 사항을 모니터링할 수 있습니다.

컨트롤 패널 인터페이스에 대한 자세한 내용은 [이 섹션](../../discover/using/discovering-the-interface.md)을 참조하십시오.

![](assets/control_panel_ip_log.png)
