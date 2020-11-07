---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650984"
---
# <span data-ttu-id="f8169-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f8169-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="f8169-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8169-102">SYNOPSIS</span></span>
<span data-ttu-id="f8169-103">Ruft alle eventhub-consumergroups ab.</span><span class="sxs-lookup"><span data-stu-id="f8169-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="f8169-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8169-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8169-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8169-105">DESCRIPTION</span></span>
<span data-ttu-id="f8169-106">Ruft alle eventhub-consumergroups für die verschiedenen von IotHub verwendeten EventHubs ab.</span><span class="sxs-lookup"><span data-stu-id="f8169-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="f8169-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8169-107">EXAMPLES</span></span>

### <span data-ttu-id="f8169-108">Beispiel 1 ruft alle eventhub-consumergroups für das Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="f8169-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="f8169-109">Ruft alle eventhub-consumergroups für die Telemetrie-eventhub für die iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="f8169-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="f8169-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8169-110">PARAMETERS</span></span>

### <span data-ttu-id="f8169-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8169-111">-DefaultProfile</span></span>
<span data-ttu-id="f8169-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8169-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8169-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="f8169-113">-EventHubEndpointName</span></span>
<span data-ttu-id="f8169-114">Name des Ereignis-Hub-Endpunkts</span><span class="sxs-lookup"><span data-stu-id="f8169-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="f8169-115">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="f8169-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="f8169-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f8169-116">-Name</span></span>
<span data-ttu-id="f8169-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="f8169-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="f8169-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8169-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8169-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f8169-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f8169-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8169-120">CommonParameters</span></span>
<span data-ttu-id="f8169-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8169-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8169-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8169-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8169-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8169-123">INPUTS</span></span>

### <span data-ttu-id="f8169-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f8169-124">System.String</span></span>

## <span data-ttu-id="f8169-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8169-125">OUTPUTS</span></span>

### <span data-ttu-id="f8169-126">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="f8169-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="f8169-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8169-127">NOTES</span></span>

## <span data-ttu-id="f8169-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8169-128">RELATED LINKS</span></span>
