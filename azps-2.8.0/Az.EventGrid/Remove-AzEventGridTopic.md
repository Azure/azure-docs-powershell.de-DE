---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3cc0d587713bf287d9cc3bfa720d867e81370a8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651212"
---
# <span data-ttu-id="e6f01-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e6f01-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="e6f01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6f01-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f01-103">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="e6f01-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e6f01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6f01-104">SYNTAX</span></span>

### <span data-ttu-id="e6f01-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6f01-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f01-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f01-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f01-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f01-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f01-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6f01-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f01-109">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="e6f01-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e6f01-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6f01-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f01-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6f01-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e6f01-112">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e6f01-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e6f01-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e6f01-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="e6f01-114">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e6f01-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e6f01-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6f01-115">PARAMETERS</span></span>

### <span data-ttu-id="e6f01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f01-116">-DefaultProfile</span></span>
<span data-ttu-id="e6f01-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e6f01-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6f01-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6f01-118">-InputObject</span></span>
<span data-ttu-id="e6f01-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6f01-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e6f01-120">-Name</span></span>
<span data-ttu-id="e6f01-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="e6f01-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f01-122">-PassThru</span></span>
<span data-ttu-id="e6f01-123">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="e6f01-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e6f01-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e6f01-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f01-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6f01-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e6f01-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e6f01-127">-ResourceId</span></span>
<span data-ttu-id="e6f01-128">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="e6f01-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6f01-129">-Confirm</span></span>
<span data-ttu-id="e6f01-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6f01-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f01-131">-WhatIf</span></span>
<span data-ttu-id="e6f01-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6f01-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f01-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6f01-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f01-134">CommonParameters</span></span>
<span data-ttu-id="e6f01-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f01-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f01-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f01-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6f01-137">INPUTS</span></span>

### <span data-ttu-id="e6f01-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f01-138">System.String</span></span>

### <span data-ttu-id="e6f01-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e6f01-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e6f01-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6f01-140">OUTPUTS</span></span>

### <span data-ttu-id="e6f01-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6f01-141">System.Boolean</span></span>

## <span data-ttu-id="e6f01-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6f01-142">NOTES</span></span>

## <span data-ttu-id="e6f01-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6f01-143">RELATED LINKS</span></span>
