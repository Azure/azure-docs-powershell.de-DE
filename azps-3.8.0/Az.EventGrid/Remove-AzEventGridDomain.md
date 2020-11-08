---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 2eb9fc2575af16f6f0bc2d6e239f63d95a0c27d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996131"
---
# <span data-ttu-id="bc272-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bc272-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="bc272-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc272-102">SYNOPSIS</span></span>
<span data-ttu-id="bc272-103">Entfernt eine Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="bc272-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="bc272-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc272-104">SYNTAX</span></span>

### <span data-ttu-id="bc272-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc272-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc272-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc272-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc272-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc272-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc272-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc272-108">DESCRIPTION</span></span>
<span data-ttu-id="bc272-109">Entfernt eine Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="bc272-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="bc272-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc272-110">EXAMPLES</span></span>

### <span data-ttu-id="bc272-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc272-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="bc272-112">Entfernt das Ereignis Raster Domäne \` domain1 \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="bc272-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bc272-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bc272-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="bc272-114">Entfernt das Ereignis Raster Domäne \` domain1 \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="bc272-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="bc272-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc272-115">PARAMETERS</span></span>

### <span data-ttu-id="bc272-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc272-116">-DefaultProfile</span></span>
<span data-ttu-id="bc272-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc272-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc272-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc272-118">-InputObject</span></span>
<span data-ttu-id="bc272-119">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc272-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="bc272-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bc272-120">-Name</span></span>
<span data-ttu-id="bc272-121">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="bc272-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc272-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc272-122">-PassThru</span></span>
<span data-ttu-id="bc272-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bc272-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bc272-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc272-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc272-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc272-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc272-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bc272-126">-ResourceId</span></span>
<span data-ttu-id="bc272-127">Der Ressourcenbezeichner, der die Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc272-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="bc272-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc272-128">-Confirm</span></span>
<span data-ttu-id="bc272-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc272-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc272-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc272-130">-WhatIf</span></span>
<span data-ttu-id="bc272-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc272-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc272-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc272-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc272-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc272-133">CommonParameters</span></span>
<span data-ttu-id="bc272-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc272-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc272-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc272-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc272-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc272-136">INPUTS</span></span>

### <span data-ttu-id="bc272-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bc272-137">System.String</span></span>

### <span data-ttu-id="bc272-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="bc272-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="bc272-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc272-139">OUTPUTS</span></span>

### <span data-ttu-id="bc272-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc272-140">System.Boolean</span></span>

## <span data-ttu-id="bc272-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc272-141">NOTES</span></span>

## <span data-ttu-id="bc272-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc272-142">RELATED LINKS</span></span>
