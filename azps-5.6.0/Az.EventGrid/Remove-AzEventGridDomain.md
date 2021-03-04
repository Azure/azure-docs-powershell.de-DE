---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924976"
---
# <span data-ttu-id="f3930-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f3930-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="f3930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3930-102">SYNOPSIS</span></span>
<span data-ttu-id="f3930-103">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="f3930-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f3930-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3930-104">SYNTAX</span></span>

### <span data-ttu-id="f3930-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3930-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3930-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3930-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3930-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3930-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3930-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3930-108">DESCRIPTION</span></span>
<span data-ttu-id="f3930-109">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="f3930-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="f3930-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3930-110">EXAMPLES</span></span>

### <span data-ttu-id="f3930-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3930-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="f3930-112">Entfernt die Ereignisrasterdomäne \` Domäne1 \` in der Ressourcengruppe \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f3930-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f3930-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f3930-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="f3930-114">Entfernt die Ereignisrasterdomäne \` Domäne1 \` in der Ressourcengruppe \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f3930-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f3930-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3930-115">PARAMETERS</span></span>

### <span data-ttu-id="f3930-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3930-116">-DefaultProfile</span></span>
<span data-ttu-id="f3930-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3930-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3930-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3930-118">-InputObject</span></span>
<span data-ttu-id="f3930-119">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3930-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="f3930-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3930-120">-Name</span></span>
<span data-ttu-id="f3930-121">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="f3930-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="f3930-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3930-122">-PassThru</span></span>
<span data-ttu-id="f3930-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f3930-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f3930-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3930-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3930-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3930-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3930-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3930-126">-ResourceId</span></span>
<span data-ttu-id="f3930-127">Ressourcenbezeichner, der die Ereignisrasterdomäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3930-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="f3930-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3930-128">-Confirm</span></span>
<span data-ttu-id="f3930-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3930-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3930-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3930-130">-WhatIf</span></span>
<span data-ttu-id="f3930-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3930-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3930-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3930-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3930-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3930-133">CommonParameters</span></span>
<span data-ttu-id="f3930-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3930-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3930-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3930-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3930-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3930-136">INPUTS</span></span>

### <span data-ttu-id="f3930-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f3930-137">System.String</span></span>

### <span data-ttu-id="f3930-138">Microsoft.Azure.Commands.EventGrid.Models.PSDOmain</span><span class="sxs-lookup"><span data-stu-id="f3930-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="f3930-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3930-139">OUTPUTS</span></span>

### <span data-ttu-id="f3930-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3930-140">System.Boolean</span></span>

## <span data-ttu-id="f3930-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3930-141">NOTES</span></span>

## <span data-ttu-id="f3930-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3930-142">RELATED LINKS</span></span>
