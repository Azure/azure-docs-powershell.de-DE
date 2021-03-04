---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930040"
---
# <span data-ttu-id="c6a22-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c6a22-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c6a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a22-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a22-103">Löscht eine Eventhub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="c6a22-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c6a22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6a22-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a22-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6a22-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a22-106">Löscht eine Eventhub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="c6a22-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c6a22-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6a22-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a22-108">Beispiel 1 Entfernen der Ereignishub-Consumergruppe aus dem Telemetrieereignishub</span><span class="sxs-lookup"><span data-stu-id="c6a22-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="c6a22-109">Entfernt die Consumergruppe mit dem Namen "myconsumergroup" aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="c6a22-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c6a22-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6a22-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a22-111">-DefaultProfile</span></span>
<span data-ttu-id="c6a22-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c6a22-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6a22-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a22-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c6a22-114">EventHub ConsumerGroup Name.</span><span class="sxs-lookup"><span data-stu-id="c6a22-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="c6a22-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a22-115">-Name</span></span>
<span data-ttu-id="c6a22-116">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="c6a22-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="c6a22-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a22-117">-ResourceGroupName</span></span>
<span data-ttu-id="c6a22-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c6a22-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c6a22-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6a22-119">-Confirm</span></span>
<span data-ttu-id="c6a22-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6a22-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a22-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a22-121">-WhatIf</span></span>
<span data-ttu-id="c6a22-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6a22-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a22-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6a22-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a22-124">CommonParameters</span></span>
<span data-ttu-id="c6a22-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a22-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a22-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a22-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6a22-127">INPUTS</span></span>

### <span data-ttu-id="c6a22-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a22-128">System.String</span></span>

## <span data-ttu-id="c6a22-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6a22-129">OUTPUTS</span></span>

### <span data-ttu-id="c6a22-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a22-130">System.String</span></span>

## <span data-ttu-id="c6a22-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6a22-131">NOTES</span></span>

## <span data-ttu-id="c6a22-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6a22-132">RELATED LINKS</span></span>
