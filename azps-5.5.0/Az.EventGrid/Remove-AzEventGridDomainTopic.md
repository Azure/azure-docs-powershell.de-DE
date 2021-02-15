---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155721"
---
# <span data-ttu-id="09055-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="09055-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="09055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09055-102">SYNOPSIS</span></span>
<span data-ttu-id="09055-103">Entfernt ein Azure Event Grid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="09055-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="09055-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09055-104">SYNTAX</span></span>

### <span data-ttu-id="09055-105">DomainTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09055-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09055-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="09055-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09055-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09055-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09055-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09055-108">DESCRIPTION</span></span>
<span data-ttu-id="09055-109">Entfernt ein Azure Event Grid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="09055-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="09055-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09055-110">EXAMPLES</span></span>

### <span data-ttu-id="09055-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09055-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="09055-112">Entfernt das "Event Grid Domain \` Topic1" \` unter \` "Domäne1" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="09055-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="09055-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="09055-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="09055-114">Entfernt das "Event Grid Domain \` Topic1" \` unter \` "Domäne1" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="09055-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="09055-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09055-115">PARAMETERS</span></span>

### <span data-ttu-id="09055-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09055-116">-DefaultProfile</span></span>
<span data-ttu-id="09055-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09055-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09055-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="09055-118">-DomainName</span></span>
<span data-ttu-id="09055-119">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="09055-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09055-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09055-120">-InputObject</span></span>
<span data-ttu-id="09055-121">EventGrid Domain Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="09055-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09055-122">-Name</span><span class="sxs-lookup"><span data-stu-id="09055-122">-Name</span></span>
<span data-ttu-id="09055-123">Name des Themas "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="09055-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09055-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09055-124">-PassThru</span></span>
<span data-ttu-id="09055-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="09055-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="09055-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09055-126">-ResourceGroupName</span></span>
<span data-ttu-id="09055-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09055-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09055-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09055-128">-ResourceId</span></span>
<span data-ttu-id="09055-129">Ressourcenbezeichner, der das Thema "Event Grid Domain" darstellt.</span><span class="sxs-lookup"><span data-stu-id="09055-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09055-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09055-130">-Confirm</span></span>
<span data-ttu-id="09055-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09055-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09055-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09055-132">-WhatIf</span></span>
<span data-ttu-id="09055-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09055-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09055-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09055-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09055-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09055-135">CommonParameters</span></span>
<span data-ttu-id="09055-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09055-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09055-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09055-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09055-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09055-138">INPUTS</span></span>

### <span data-ttu-id="09055-139">System.String</span><span class="sxs-lookup"><span data-stu-id="09055-139">System.String</span></span>

### <span data-ttu-id="09055-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="09055-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="09055-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09055-141">OUTPUTS</span></span>

### <span data-ttu-id="09055-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09055-142">System.Boolean</span></span>

## <span data-ttu-id="09055-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09055-143">NOTES</span></span>

## <span data-ttu-id="09055-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09055-144">RELATED LINKS</span></span>
