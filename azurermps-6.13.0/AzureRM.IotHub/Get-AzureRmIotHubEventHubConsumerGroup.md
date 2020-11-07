---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 507787df7215efcd1b275f481b638aa80f979498
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664604"
---
# <span data-ttu-id="080f4-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="080f4-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="080f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="080f4-102">SYNOPSIS</span></span>
<span data-ttu-id="080f4-103">Ruft alle eventhub-consumergroups ab.</span><span class="sxs-lookup"><span data-stu-id="080f4-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="080f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="080f4-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="080f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="080f4-105">DESCRIPTION</span></span>
<span data-ttu-id="080f4-106">Ruft alle eventhub-consumergroups für die verschiedenen von IotHub verwendeten EventHubs ab.</span><span class="sxs-lookup"><span data-stu-id="080f4-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="080f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="080f4-107">EXAMPLES</span></span>

### <span data-ttu-id="080f4-108">Beispiel 1 ruft alle eventhub-consumergroups für das Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="080f4-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="080f4-109">Ruft alle eventhub-consumergroups für die Telemetrie-eventhub für die iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="080f4-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="080f4-110">Beispiel 2 ruft alle eventhub-consumergroups für den operationsmonitoring-eventhub</span><span class="sxs-lookup"><span data-stu-id="080f4-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="080f4-111">Ruft alle eventhub-consumergroups für die operationsMonitoringEvents-eventhub für die iothub mit dem Namen myiothub</span><span class="sxs-lookup"><span data-stu-id="080f4-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="080f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="080f4-112">PARAMETERS</span></span>

### <span data-ttu-id="080f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080f4-113">-DefaultProfile</span></span>
<span data-ttu-id="080f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="080f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="080f4-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="080f4-115">-EventHubEndpointName</span></span>
<span data-ttu-id="080f4-116">Name des Ereignis-Hub-Endpunkts</span><span class="sxs-lookup"><span data-stu-id="080f4-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="080f4-117">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="080f4-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="080f4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="080f4-118">-Name</span></span>
<span data-ttu-id="080f4-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="080f4-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="080f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="080f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="080f4-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="080f4-121">Resource Group Name</span></span>

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

### <span data-ttu-id="080f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080f4-122">CommonParameters</span></span>
<span data-ttu-id="080f4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="080f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080f4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="080f4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080f4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="080f4-125">INPUTS</span></span>

### <span data-ttu-id="080f4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="080f4-126">System.String</span></span>

## <span data-ttu-id="080f4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="080f4-127">OUTPUTS</span></span>

### <span data-ttu-id="080f4-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="080f4-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="080f4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="080f4-129">NOTES</span></span>

## <span data-ttu-id="080f4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="080f4-130">RELATED LINKS</span></span>
