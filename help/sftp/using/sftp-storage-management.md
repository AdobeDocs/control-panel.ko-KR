---
title: SFTP 저장소 관리
description: SFTP 서버의 저장소 모니터링 및 관리 방법 알아보기
translation-type: tm+mt
source-git-commit: 111c8fd461f6f1c567288acd7a83aee5ef7fce97

---


# SFTP 저장소 관리 {#sftp-storage-management}

계약 약관에 따라 SFTP 서버에서 프로비저닝된 저장소 용량이 다를 수 있습니다.

각 SFTP 서버에 대해 사용 가능한 공간을 정기적으로 모니터링해야 합니다. 그렇지 않으면 더 이상 서버에 추가 파일을 저장할 수 없거나 이 서버의 업데이트를 사용하는 워크플로를 성공적으로 실행할 수 없습니다.

**관련 항목:**

* [Campaign Standard 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-sftp-servers.html)
* [Campaign Classic 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## 스토리지 용량 정보 액세스 {#accessing-storage-capacity-information}

헤더의 **[!UICONTROL Top utilized SFTP disk capacity]** 섹션에는 관리 액세스 권한이 있는 인스턴스에 연결된 가장 많이 사용되는 세 개의 서버가 포함되어 있습니다. 이 정보는 SFTP 카드의 모든 탭에서 사용할 수 있습니다.

![](assets/control_panel_topspaceNEW.png)

액세스 권한이 있는 모든 인스턴스에서 사용하는 공간에 대한 정보는 SFTP 카드의 **[!UICONTROL Storage]** 탭에서 사용할 수 있습니다. 새로 고칠 때마다 업데이트됩니다.

![](assets/control_panel_spaceNEW.png)

각 인스턴스에 대해 시각적 경고를 통해 스토리지 용량이 초과되는지 알 수 있습니다.

* **주황**:그 인스턴스는 그 용량의 80%를 넘었고
* **빨간색**:그 예는 그 용량의 90%를 능가한다.

서버 용량이 가까워지면 어떻게 진행할지 아는 데 도움이 되는 추가 팁도 제공됩니다.

## 스토리지 용량이 부족한 경우의 우수 사례 {#best-practices-when-capacity-runs-out}

1. **이전 파일이나 불필요한 파일에서** SFTP 서버를 정리합니다. SFTP 서버 폴더에 액세스하는 방법에 대한 자세한 내용은 [이 섹션을](../../sftp/using/logging-into-sftp-server.md)참조하십시오.
1. SFTP 서버를 정리하는 **워크플로우가** 성공적으로 실행되는지 확인합니다. Adobe Campaign의 기술 워크플로우에 대한 자세한 내용은 전용 [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) 및 Campaign Standard [설명서를](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) 참조하십시오.
1. 계정 팀에 연락하여 더 많은 스토리지를 **요청하십시오** (추가 비용이 발생할 수 있음).
1. 문제가 있다고 생각되면 **고객 지원 센터**&#x200B;에 문의하십시오.
