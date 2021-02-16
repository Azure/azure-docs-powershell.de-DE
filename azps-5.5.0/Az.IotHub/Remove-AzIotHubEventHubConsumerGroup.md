---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155417"
---
# <span data-ttu-id="7a791-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a791-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7a791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a791-102">SYNOPSIS</span></span>
<span data-ttu-id="7a791-103">Löscht eine Eventhub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="7a791-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="7a791-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a791-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a791-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a791-105">DESCRIPTION</span></span>
<span data-ttu-id="7a791-106">Löscht eine Eventhub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="7a791-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="7a791-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a791-107">EXAMPLES</span></span>

### <span data-ttu-id="7a791-108">Beispiel 1 Entfernen der Eventhub-Consumergruppe aus dem Telemetrieereignishub</span><span class="sxs-lookup"><span data-stu-id="7a791-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="7a791-109">Entfernt die Consumergruppe mit dem Namen "myconsumergroup" aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7a791-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7a791-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a791-110">PARAMETERS</span></span>

### <span data-ttu-id="7a791-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a791-111">-DefaultProfile</span></span>
<span data-ttu-id="7a791-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7a791-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a791-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7a791-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="7a791-114">Name der EventHub ConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7a791-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="7a791-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7a791-115">-Name</span></span>
<span data-ttu-id="7a791-116">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="7a791-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="7a791-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a791-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a791-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7a791-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7a791-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a791-119">-Confirm</span></span>
<span data-ttu-id="7a791-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a791-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a791-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a791-121">-WhatIf</span></span>
<span data-ttu-id="7a791-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a791-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a791-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a791-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a791-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a791-124">CommonParameters</span></span>
<span data-ttu-id="7a791-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a791-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a791-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a791-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a791-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a791-127">INPUTS</span></span>

### <span data-ttu-id="7a791-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7a791-128">System.String</span></span>

## <span data-ttu-id="7a791-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a791-129">OUTPUTS</span></span>

### <span data-ttu-id="7a791-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7a791-130">System.String</span></span>

## <span data-ttu-id="7a791-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a791-131">NOTES</span></span>

## <span data-ttu-id="7a791-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a791-132">RELATED LINKS</span></span>
