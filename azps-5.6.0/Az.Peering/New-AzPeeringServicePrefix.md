---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 24fcfc222d9d3cab1b0785c121e09b596aae16fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937635"
---
# <span data-ttu-id="c32b3-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c32b3-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="c32b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c32b3-103">Erstellt ein neues Peeringdienstpräfix</span><span class="sxs-lookup"><span data-stu-id="c32b3-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="c32b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c32b3-104">SYNTAX</span></span>

### <span data-ttu-id="c32b3-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="c32b3-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c32b3-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32b3-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c32b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c32b3-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c32b3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c32b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c32b3-109">Erstellt ein Peeringdienstpräfix, das einem Peeringdienstobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c32b3-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="c32b3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c32b3-110">EXAMPLES</span></span>

### <span data-ttu-id="c32b3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c32b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="c32b3-112">Erstellt ein Präfix aus einem Peeringdienstobjekt</span><span class="sxs-lookup"><span data-stu-id="c32b3-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="c32b3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c32b3-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="c32b3-114">Erstellt ein Präfix aus einer Peeringdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c32b3-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="c32b3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c32b3-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="c32b3-116">Erstellt ein Präfix aus dem Namen und Namen einer Peeringdienstressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c32b3-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="c32b3-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c32b3-117">PARAMETERS</span></span>

### <span data-ttu-id="c32b3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c32b3-118">-AsJob</span></span>
<span data-ttu-id="c32b3-119">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="c32b3-119">Run in the background.</span></span>

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

### <span data-ttu-id="c32b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32b3-120">-DefaultProfile</span></span>
<span data-ttu-id="c32b3-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c32b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c32b3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c32b3-122">-Name</span></span>
<span data-ttu-id="c32b3-123">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="c32b3-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="c32b3-124">-PeeringServiceId</span></span>
<span data-ttu-id="c32b3-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c32b3-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="c32b3-126">-PeeringServiceName</span></span>
<span data-ttu-id="c32b3-127">Der Name des Peeringdiensts.</span><span class="sxs-lookup"><span data-stu-id="c32b3-127">The peering service name.</span></span>
<span data-ttu-id="c32b3-128">Verwenden New-AzPeeringService cmdlet für einen neuen Peeringdienst oder Get-AzPeeringService für eine Liste.</span><span class="sxs-lookup"><span data-stu-id="c32b3-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="c32b3-129">-PeeringServiceObject</span></span>
<span data-ttu-id="c32b3-130">Verwenden eines Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c32b3-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c32b3-131">-Prefix</span></span>
<span data-ttu-id="c32b3-132">Das IPv4-Sitzungspräfix</span><span class="sxs-lookup"><span data-stu-id="c32b3-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32b3-133">-ResourceGroupName</span></span>
<span data-ttu-id="c32b3-134">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="c32b3-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="c32b3-135">-ServiceKey</span></span>
<span data-ttu-id="c32b3-136">Dies ist eine eindeutige GUID, die von Ihrem Dienstanbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c32b3-136">This is a unique GUID provided by your service provider</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32b3-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c32b3-137">-Confirm</span></span>
<span data-ttu-id="c32b3-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c32b3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c32b3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c32b3-139">-WhatIf</span></span>
<span data-ttu-id="c32b3-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c32b3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c32b3-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c32b3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c32b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32b3-142">CommonParameters</span></span>
<span data-ttu-id="c32b3-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32b3-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c32b3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32b3-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c32b3-145">INPUTS</span></span>

### <span data-ttu-id="c32b3-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="c32b3-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="c32b3-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c32b3-147">OUTPUTS</span></span>

### <span data-ttu-id="c32b3-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c32b3-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="c32b3-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c32b3-149">NOTES</span></span>

## <span data-ttu-id="c32b3-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c32b3-150">RELATED LINKS</span></span>
