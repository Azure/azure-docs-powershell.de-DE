---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004003"
---
# <span data-ttu-id="91dd7-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="91dd7-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="91dd7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="91dd7-103">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="91dd7-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="91dd7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91dd7-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91dd7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="91dd7-106">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="91dd7-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="91dd7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="91dd7-108">Beispiel 1 Entfernen von eventhub consumergroup aus der Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="91dd7-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="91dd7-109">Entfernt die verbrauchergroup mit dem Namen "myconsumergroup" aus dem IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="91dd7-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="91dd7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91dd7-110">PARAMETERS</span></span>

### <span data-ttu-id="91dd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dd7-111">-DefaultProfile</span></span>
<span data-ttu-id="91dd7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="91dd7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91dd7-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="91dd7-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="91dd7-114">Name der EventHub-consumergruppe</span><span class="sxs-lookup"><span data-stu-id="91dd7-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91dd7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91dd7-115">-Name</span></span>
<span data-ttu-id="91dd7-116">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="91dd7-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="91dd7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91dd7-117">-ResourceGroupName</span></span>
<span data-ttu-id="91dd7-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="91dd7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="91dd7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91dd7-119">-Confirm</span></span>
<span data-ttu-id="91dd7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91dd7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91dd7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91dd7-121">-WhatIf</span></span>
<span data-ttu-id="91dd7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91dd7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91dd7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91dd7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91dd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dd7-124">CommonParameters</span></span>
<span data-ttu-id="91dd7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91dd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dd7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91dd7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dd7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91dd7-127">INPUTS</span></span>

### <span data-ttu-id="91dd7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91dd7-128">System.String</span></span>

## <span data-ttu-id="91dd7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91dd7-129">OUTPUTS</span></span>

### <span data-ttu-id="91dd7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="91dd7-130">System.String</span></span>

## <span data-ttu-id="91dd7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="91dd7-131">NOTES</span></span>

## <span data-ttu-id="91dd7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91dd7-132">RELATED LINKS</span></span>
