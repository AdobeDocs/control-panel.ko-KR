---
product: campaign
solution: Campaign
title: 처리량 및 지연 모니터링
description: Campaign 컨트롤 패널에서 배치 및 지연을 통해 Campaign 인스턴스를 모니터링하는 방법을 알아봅니다.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cbc068c921d0d16b49c881693e44e1ba2a90d015
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 처리량 및 지연 모니터링 {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="처리량 및 지연 모니터링 정보 "
>abstract="이 탭에서는 인스턴스의 한 기간 동안 게재 처리량과 지연 시간이 어떻게 트렌드인지 모니터링할 수 있습니다."

게재 처리량 및 지연 시간이 일정 기간 동안 어떻게 트렌드를 표시하는지 모니터링하려면 인스턴스의 사용을 이해하고 제대로 작동하는지 확인해야 합니다.

이 정보는 의 각 Campaign 인스턴스에 대해 Campaign 컨트롤 패널에서 사용할 수 있습니다 **[!UICONTROL Performance Monitoring]** 카드, **[!UICONTROL Throughputs & Latencies]** 탭.

>[!NOTE]
>
>이 영역에 나와 있는 모든 수치는 근사 정보용으로만 제공됩니다.

![](assets/throughput-latencies-overview.png)

기본적으로 현재 날짜의 데이터가 표시됩니다. 를 사용하여 표시된 기간을 변경할 수 있습니다 **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** 및 **[!UICONTROL 7 days]** 단추.

다음 **[!UICONTROL Throughput]** 영역에서는 권한이 부여된 모든 통신 채널에 대해 선택한 Campaign 인스턴스에서 시간당 전송된 메시지 수에 대한 정보를 제공합니다.

이 정보를 그래프가 아닌 정렬 가능한 열을 사용하여 표 형식으로 시각화할 수도 있습니다. 이렇게 하려면 **[!UICONTROL Visualization settings]** 단추를 누른 후 선택 **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

다음 **[!UICONTROL Latency]** 영역에서는 실시간 트랜잭션 통신을 전송할 때 선택한 인스턴스에서 발생하는 지연에 대한 정보를 제공합니다. 지연은 95 및 99 백분위수에서 캡처되고 시각화되므로, 요청의 95% 및 99%가 지정된 지연보다 빨라야 합니다.

![](assets/throughput-latencies-latency.png)
