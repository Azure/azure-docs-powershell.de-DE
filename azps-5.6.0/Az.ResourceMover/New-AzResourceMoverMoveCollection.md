---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943546"
---
# <span data-ttu-id="f3c51-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f3c51-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f3c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c51-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c51-103">Erstellt oder aktualisiert eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="f3c51-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f3c51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3c51-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3c51-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3c51-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c51-106">Erstellt oder aktualisiert eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="f3c51-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="f3c51-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3c51-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c51-108">Beispiel 1: Erstellen einer neuen Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="f3c51-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="f3c51-109">Erstellen Sie eine neue Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="f3c51-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="f3c51-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3c51-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c51-111">-DefaultProfile</span></span>
<span data-ttu-id="f3c51-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3c51-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f3c51-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="f3c51-114">Ruft die Prinzipal-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f3c51-114">Gets or sets the principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="f3c51-115">-IdentityTenantId</span></span>
<span data-ttu-id="f3c51-116">Ruft die Mandanten-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f3c51-116">Gets or sets the tenant id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f3c51-117">-IdentityType</span></span>
<span data-ttu-id="f3c51-118">Der Identitätstyp, der für den Ressourcen-Moverdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3c51-118">The type of identity used for the resource mover service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f3c51-119">-Location</span></span>
<span data-ttu-id="f3c51-120">Der Geospeicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="f3c51-120">The geo-location where the resource lives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c51-121">-Name</span></span>
<span data-ttu-id="f3c51-122">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="f3c51-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c51-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3c51-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3c51-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f3c51-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="f3c51-125">-SourceRegion</span></span>
<span data-ttu-id="f3c51-126">Ruft den Quellbereich ab oder legt den Quellbereich fest.</span><span class="sxs-lookup"><span data-stu-id="f3c51-126">Gets or sets the source region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3c51-127">-SubscriptionId</span></span>
<span data-ttu-id="f3c51-128">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f3c51-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3c51-129">-Tag</span></span>
<span data-ttu-id="f3c51-130">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="f3c51-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f3c51-131">-TargetRegion</span></span>
<span data-ttu-id="f3c51-132">Ruft den Zielbereich ab oder legt den Zielbereich fest.</span><span class="sxs-lookup"><span data-stu-id="f3c51-132">Gets or sets the target region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c51-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3c51-133">-Confirm</span></span>
<span data-ttu-id="f3c51-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3c51-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c51-135">-WhatIf</span></span>
<span data-ttu-id="f3c51-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3c51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c51-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3c51-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c51-138">CommonParameters</span></span>
<span data-ttu-id="f3c51-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c51-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c51-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c51-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3c51-141">INPUTS</span></span>

## <span data-ttu-id="f3c51-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3c51-142">OUTPUTS</span></span>

### <span data-ttu-id="f3c51-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f3c51-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="f3c51-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3c51-144">NOTES</span></span>

<span data-ttu-id="f3c51-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f3c51-145">ALIASES</span></span>

## <span data-ttu-id="f3c51-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3c51-146">RELATED LINKS</span></span>

