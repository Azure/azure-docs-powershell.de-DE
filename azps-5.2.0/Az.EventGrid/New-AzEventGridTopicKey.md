---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363711"
---
# <span data-ttu-id="35984-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="35984-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="35984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35984-102">SYNOPSIS</span></span>
<span data-ttu-id="35984-103">Generiert den freigegebenen Zugriffsschlüssel für ein Azure-Ereignisrasterthema erneut.</span><span class="sxs-lookup"><span data-stu-id="35984-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="35984-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35984-104">SYNTAX</span></span>

### <span data-ttu-id="35984-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="35984-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35984-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35984-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35984-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="35984-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35984-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35984-108">DESCRIPTION</span></span>
<span data-ttu-id="35984-109">Generiert den freigegebenen Zugriffsschlüssel für ein Azure-Ereignisrasterthema erneut.</span><span class="sxs-lookup"><span data-stu-id="35984-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="35984-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="35984-110">EXAMPLES</span></span>

### <span data-ttu-id="35984-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35984-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="35984-112">Regenerieren Sie den Schlüssel entsprechend "key1'\" des Themas "Event Grid Topic1" in der Ressourcengruppe \' \` \` \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="35984-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="35984-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35984-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="35984-114">Regenerieren Sie den Schlüssel entsprechend "key1'\" des Themas "Event Grid Topic1" in der Ressourcengruppe \' \` \` \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="35984-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="35984-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35984-115">PARAMETERS</span></span>

### <span data-ttu-id="35984-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35984-116">-DefaultProfile</span></span>
<span data-ttu-id="35984-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="35984-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35984-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35984-118">-InputObject</span></span>
<span data-ttu-id="35984-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="35984-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="35984-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="35984-120">-KeyName</span></span>
<span data-ttu-id="35984-121">Der Name des Schlüssels, der erneut generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="35984-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="35984-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35984-122">-ResourceGroupName</span></span>
<span data-ttu-id="35984-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="35984-123">Resource group name.</span></span>

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

### <span data-ttu-id="35984-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35984-124">-ResourceId</span></span>
<span data-ttu-id="35984-125">Ressourcenbezeichner, der das Thema "Veranstaltungsraster" darstellt.</span><span class="sxs-lookup"><span data-stu-id="35984-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="35984-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="35984-126">-TopicName</span></span>
<span data-ttu-id="35984-127">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="35984-127">The name of the topic.</span></span>

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

### <span data-ttu-id="35984-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35984-128">-Confirm</span></span>
<span data-ttu-id="35984-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35984-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35984-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="35984-130">-WhatIf</span></span>
<span data-ttu-id="35984-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35984-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35984-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35984-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35984-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35984-133">CommonParameters</span></span>
<span data-ttu-id="35984-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35984-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35984-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35984-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35984-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="35984-136">INPUTS</span></span>

### <span data-ttu-id="35984-137">System.String</span><span class="sxs-lookup"><span data-stu-id="35984-137">System.String</span></span>

### <span data-ttu-id="35984-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="35984-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="35984-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="35984-139">OUTPUTS</span></span>

### <span data-ttu-id="35984-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="35984-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="35984-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="35984-141">NOTES</span></span>

## <span data-ttu-id="35984-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="35984-142">RELATED LINKS</span></span>
