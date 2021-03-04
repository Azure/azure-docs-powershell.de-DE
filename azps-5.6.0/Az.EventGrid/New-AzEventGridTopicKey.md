---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: aa59b4046a775c41dd3b44142d0a407c94ff1f4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938723"
---
# <span data-ttu-id="5145a-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="5145a-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="5145a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5145a-102">SYNOPSIS</span></span>
<span data-ttu-id="5145a-103">Regeneriert den freigegebenen Zugriffsschlüssel für ein Azure Event Grid Topic.</span><span class="sxs-lookup"><span data-stu-id="5145a-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5145a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5145a-104">SYNTAX</span></span>

### <span data-ttu-id="5145a-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5145a-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5145a-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5145a-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5145a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5145a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5145a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5145a-108">DESCRIPTION</span></span>
<span data-ttu-id="5145a-109">Regeneriert den freigegebenen Zugriffsschlüssel für ein Azure Event Grid Topic.</span><span class="sxs-lookup"><span data-stu-id="5145a-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="5145a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5145a-110">EXAMPLES</span></span>

### <span data-ttu-id="5145a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5145a-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="5145a-112">Regenerieren Sie den Schlüssel entsprechend \' schlüssel1'\ des Themas Ereignisrasterthema1 in der \` \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5145a-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5145a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5145a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="5145a-114">Regenerieren Sie den Schlüssel entsprechend \' schlüssel1'\ des Themas Ereignisrasterthema1 in der \` \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5145a-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5145a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5145a-115">PARAMETERS</span></span>

### <span data-ttu-id="5145a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5145a-116">-DefaultProfile</span></span>
<span data-ttu-id="5145a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5145a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5145a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5145a-118">-InputObject</span></span>
<span data-ttu-id="5145a-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5145a-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5145a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5145a-120">-KeyName</span></span>
<span data-ttu-id="5145a-121">Der Name des Schlüssels, der neu generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="5145a-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="5145a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5145a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5145a-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5145a-123">Resource group name.</span></span>

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

### <span data-ttu-id="5145a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5145a-124">-ResourceId</span></span>
<span data-ttu-id="5145a-125">Ressourcenbezeichner, der das Thema "Ereignisraster" darstellt.</span><span class="sxs-lookup"><span data-stu-id="5145a-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5145a-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5145a-126">-TopicName</span></span>
<span data-ttu-id="5145a-127">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="5145a-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5145a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5145a-128">-Confirm</span></span>
<span data-ttu-id="5145a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5145a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5145a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5145a-130">-WhatIf</span></span>
<span data-ttu-id="5145a-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5145a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5145a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5145a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5145a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5145a-133">CommonParameters</span></span>
<span data-ttu-id="5145a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5145a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5145a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5145a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5145a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5145a-136">INPUTS</span></span>

### <span data-ttu-id="5145a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5145a-137">System.String</span></span>

### <span data-ttu-id="5145a-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="5145a-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5145a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5145a-139">OUTPUTS</span></span>

### <span data-ttu-id="5145a-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5145a-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="5145a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5145a-141">NOTES</span></span>

## <span data-ttu-id="5145a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5145a-142">RELATED LINKS</span></span>
