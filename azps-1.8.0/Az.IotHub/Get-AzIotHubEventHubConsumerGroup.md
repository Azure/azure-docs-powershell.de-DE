---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819780"
---
# <span data-ttu-id="13ce7-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="13ce7-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="13ce7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="13ce7-103">Ruft alle eventhub-consumergroups ab.</span><span class="sxs-lookup"><span data-stu-id="13ce7-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="13ce7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ce7-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ce7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="13ce7-106">Ruft alle eventhub-consumergroups für die verschiedenen von IotHub verwendeten EventHubs ab.</span><span class="sxs-lookup"><span data-stu-id="13ce7-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="13ce7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="13ce7-108">Beispiel 1 ruft alle eventhub-consumergroups für das Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="13ce7-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="13ce7-109">Ruft alle eventhub-consumergroups für die Telemetrie-eventhub für die iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="13ce7-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="13ce7-110">Beispiel 2 ruft alle eventhub-consumergroups für den operationsmonitoring-eventhub</span><span class="sxs-lookup"><span data-stu-id="13ce7-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="13ce7-111">Ruft alle eventhub-consumergroups für die operationsMonitoringEvents-eventhub für die iothub mit dem Namen myiothub</span><span class="sxs-lookup"><span data-stu-id="13ce7-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="13ce7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13ce7-112">PARAMETERS</span></span>

### <span data-ttu-id="13ce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ce7-113">-DefaultProfile</span></span>
<span data-ttu-id="13ce7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="13ce7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ce7-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="13ce7-115">-EventHubEndpointName</span></span>
<span data-ttu-id="13ce7-116">Name des Ereignis-Hub-Endpunkts</span><span class="sxs-lookup"><span data-stu-id="13ce7-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="13ce7-117">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="13ce7-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ce7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13ce7-118">-Name</span></span>
<span data-ttu-id="13ce7-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="13ce7-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ce7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ce7-120">-ResourceGroupName</span></span>
<span data-ttu-id="13ce7-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="13ce7-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ce7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ce7-122">CommonParameters</span></span>
<span data-ttu-id="13ce7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ce7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ce7-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ce7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ce7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13ce7-125">INPUTS</span></span>

### <span data-ttu-id="13ce7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="13ce7-126">System.String</span></span>

## <span data-ttu-id="13ce7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13ce7-127">OUTPUTS</span></span>

### <span data-ttu-id="13ce7-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="13ce7-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="13ce7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="13ce7-129">NOTES</span></span>

## <span data-ttu-id="13ce7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13ce7-130">RELATED LINKS</span></span>
