---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298731"
---
# <span data-ttu-id="7a00d-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7a00d-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="7a00d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a00d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a00d-103">Entfernt ein Azure-Ereignisrasterthema.</span><span class="sxs-lookup"><span data-stu-id="7a00d-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7a00d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a00d-104">SYNTAX</span></span>

### <span data-ttu-id="7a00d-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a00d-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a00d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a00d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a00d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a00d-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a00d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a00d-108">DESCRIPTION</span></span>
<span data-ttu-id="7a00d-109">Entfernt ein Azure-Veranstaltungsrasterthema.</span><span class="sxs-lookup"><span data-stu-id="7a00d-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7a00d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a00d-110">EXAMPLES</span></span>

### <span data-ttu-id="7a00d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a00d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="7a00d-112">Entfernt das Thema "Veranstaltungsraster", \` "Topic1" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="7a00d-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7a00d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7a00d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="7a00d-114">Entfernt das Thema "Veranstaltungsraster", \` "Topic1" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="7a00d-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7a00d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a00d-115">PARAMETERS</span></span>

### <span data-ttu-id="7a00d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a00d-116">-DefaultProfile</span></span>
<span data-ttu-id="7a00d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7a00d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a00d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a00d-118">-InputObject</span></span>
<span data-ttu-id="7a00d-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a00d-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7a00d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7a00d-120">-Name</span></span>
<span data-ttu-id="7a00d-121">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="7a00d-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="7a00d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a00d-122">-PassThru</span></span>
<span data-ttu-id="7a00d-123">Gibt den Status des Vorgangs "Entfernen" zurück.</span><span class="sxs-lookup"><span data-stu-id="7a00d-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7a00d-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7a00d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a00d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a00d-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a00d-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7a00d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="7a00d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a00d-127">-ResourceId</span></span>
<span data-ttu-id="7a00d-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7a00d-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="7a00d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a00d-129">-Confirm</span></span>
<span data-ttu-id="7a00d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a00d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a00d-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a00d-131">-WhatIf</span></span>
<span data-ttu-id="7a00d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a00d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a00d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a00d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a00d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a00d-134">CommonParameters</span></span>
<span data-ttu-id="7a00d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a00d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a00d-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a00d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a00d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a00d-137">INPUTS</span></span>

### <span data-ttu-id="7a00d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7a00d-138">System.String</span></span>

### <span data-ttu-id="7a00d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="7a00d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7a00d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a00d-140">OUTPUTS</span></span>

### <span data-ttu-id="7a00d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a00d-141">System.Boolean</span></span>

## <span data-ttu-id="7a00d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a00d-142">NOTES</span></span>

## <span data-ttu-id="7a00d-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a00d-143">RELATED LINKS</span></span>
