---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458711"
---
# <span data-ttu-id="e20f1-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e20f1-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="e20f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e20f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e20f1-103">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e20f1-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="e20f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e20f1-104">SYNTAX</span></span>

### <span data-ttu-id="e20f1-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e20f1-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e20f1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e20f1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e20f1-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e20f1-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e20f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e20f1-108">DESCRIPTION</span></span>
<span data-ttu-id="e20f1-109">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e20f1-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="e20f1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e20f1-110">EXAMPLES</span></span>

### <span data-ttu-id="e20f1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e20f1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="e20f1-112">Entfernt "Event Grid \` \` Domain1" in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="e20f1-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e20f1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e20f1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="e20f1-114">Entfernt "Event Grid \` \` Domain1" in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="e20f1-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e20f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e20f1-115">PARAMETERS</span></span>

### <span data-ttu-id="e20f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20f1-116">-DefaultProfile</span></span>
<span data-ttu-id="e20f1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e20f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e20f1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e20f1-118">-InputObject</span></span>
<span data-ttu-id="e20f1-119">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e20f1-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e20f1-120">-Name</span></span>
<span data-ttu-id="e20f1-121">"EventGrid"-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="e20f1-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e20f1-122">-PassThru</span></span>
<span data-ttu-id="e20f1-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e20f1-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e20f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e20f1-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e20f1-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e20f1-126">-ResourceId</span></span>
<span data-ttu-id="e20f1-127">Ressourcenbezeichner, der die "Event Grid Domain" darstellt.</span><span class="sxs-lookup"><span data-stu-id="e20f1-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="e20f1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e20f1-128">-Confirm</span></span>
<span data-ttu-id="e20f1-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e20f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e20f1-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e20f1-130">-WhatIf</span></span>
<span data-ttu-id="e20f1-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e20f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e20f1-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e20f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e20f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20f1-133">CommonParameters</span></span>
<span data-ttu-id="e20f1-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e20f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20f1-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e20f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20f1-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e20f1-136">INPUTS</span></span>

### <span data-ttu-id="e20f1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e20f1-137">System.String</span></span>

### <span data-ttu-id="e20f1-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="e20f1-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="e20f1-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e20f1-139">OUTPUTS</span></span>

### <span data-ttu-id="e20f1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e20f1-140">System.Boolean</span></span>

## <span data-ttu-id="e20f1-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e20f1-141">NOTES</span></span>

## <span data-ttu-id="e20f1-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e20f1-142">RELATED LINKS</span></span>
