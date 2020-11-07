---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: d9b1fd2f9161f9a717295d0995605eb6f75b8799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661070"
---
# <span data-ttu-id="f9a07-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="f9a07-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="f9a07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9a07-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a07-103">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="f9a07-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="f9a07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9a07-104">SYNTAX</span></span>

### <span data-ttu-id="f9a07-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9a07-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a07-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9a07-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a07-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9a07-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9a07-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9a07-108">DESCRIPTION</span></span>
<span data-ttu-id="f9a07-109">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="f9a07-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="f9a07-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9a07-110">EXAMPLES</span></span>

### <span data-ttu-id="f9a07-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9a07-111">Example 1</span></span>
```
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="f9a07-112">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f9a07-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f9a07-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f9a07-113">Example 2</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="f9a07-114">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f9a07-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f9a07-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9a07-115">PARAMETERS</span></span>

### <span data-ttu-id="f9a07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a07-116">-DefaultProfile</span></span>
<span data-ttu-id="f9a07-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f9a07-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9a07-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9a07-118">-InputObject</span></span>
<span data-ttu-id="f9a07-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9a07-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f9a07-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9a07-120">-Name</span></span>
<span data-ttu-id="f9a07-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="f9a07-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f9a07-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9a07-122">-PassThru</span></span>
<span data-ttu-id="f9a07-123">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a07-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="f9a07-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f9a07-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9a07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a07-125">-ResourceGroupName</span></span>
<span data-ttu-id="f9a07-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9a07-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9a07-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f9a07-127">-ResourceId</span></span>
<span data-ttu-id="f9a07-128">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="f9a07-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="f9a07-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9a07-129">-Confirm</span></span>
<span data-ttu-id="f9a07-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9a07-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a07-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a07-131">-WhatIf</span></span>
<span data-ttu-id="f9a07-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9a07-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9a07-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9a07-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a07-134">CommonParameters</span></span>
<span data-ttu-id="f9a07-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a07-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a07-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a07-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9a07-137">INPUTS</span></span>

### <span data-ttu-id="f9a07-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f9a07-138">System.String</span></span>

### <span data-ttu-id="f9a07-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f9a07-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f9a07-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9a07-140">OUTPUTS</span></span>

### <span data-ttu-id="f9a07-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9a07-141">System.Boolean</span></span>

## <span data-ttu-id="f9a07-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9a07-142">NOTES</span></span>

## <span data-ttu-id="f9a07-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9a07-143">RELATED LINKS</span></span>
