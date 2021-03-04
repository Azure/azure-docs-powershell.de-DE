---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 23f6c4b7d40f0ec2e02541f82d5d517019bd15fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942515"
---
# <span data-ttu-id="051ec-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="051ec-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="051ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="051ec-102">SYNOPSIS</span></span>
<span data-ttu-id="051ec-103">Erstellt eine Eventhub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="051ec-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="051ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="051ec-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="051ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="051ec-105">DESCRIPTION</span></span>
<span data-ttu-id="051ec-106">Erstellt eine Consumergruppe im Eventhub, der dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="051ec-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="051ec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="051ec-107">EXAMPLES</span></span>

### <span data-ttu-id="051ec-108">Beispiel 1: Hinzufügen einer Consumergruppe zum Telemetrieereignishub</span><span class="sxs-lookup"><span data-stu-id="051ec-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="051ec-109">Fügt dem Eventhub eine neue Consumergruppe mit dem Namen "myconsumergroup" für Telemetrieereignisse im Iothub mit dem Namen "myiothub" hinzu.</span><span class="sxs-lookup"><span data-stu-id="051ec-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="051ec-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="051ec-110">PARAMETERS</span></span>

### <span data-ttu-id="051ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051ec-111">-DefaultProfile</span></span>
<span data-ttu-id="051ec-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="051ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="051ec-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="051ec-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="051ec-114">Name der EventHub ConsumerGroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="051ec-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="051ec-115">-Name</span></span>
<span data-ttu-id="051ec-116">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="051ec-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="051ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="051ec-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="051ec-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="051ec-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="051ec-119">-Confirm</span></span>
<span data-ttu-id="051ec-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="051ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="051ec-121">-WhatIf</span></span>
<span data-ttu-id="051ec-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="051ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="051ec-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="051ec-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051ec-124">CommonParameters</span></span>
<span data-ttu-id="051ec-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="051ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051ec-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="051ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051ec-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="051ec-127">INPUTS</span></span>

### <span data-ttu-id="051ec-128">System.String</span><span class="sxs-lookup"><span data-stu-id="051ec-128">System.String</span></span>

## <span data-ttu-id="051ec-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="051ec-129">OUTPUTS</span></span>

### <span data-ttu-id="051ec-130">System.String</span><span class="sxs-lookup"><span data-stu-id="051ec-130">System.String</span></span>

## <span data-ttu-id="051ec-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="051ec-131">NOTES</span></span>

## <span data-ttu-id="051ec-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="051ec-132">RELATED LINKS</span></span>
