---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459556"
---
# <span data-ttu-id="87f00-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="87f00-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="87f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f00-102">SYNOPSIS</span></span>
<span data-ttu-id="87f00-103">Erstellt oder aktualisiert eine Sammlung zum Verschieben.</span><span class="sxs-lookup"><span data-stu-id="87f00-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="87f00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87f00-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87f00-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87f00-105">DESCRIPTION</span></span>
<span data-ttu-id="87f00-106">Erstellt oder aktualisiert eine Sammlung zum Verschieben.</span><span class="sxs-lookup"><span data-stu-id="87f00-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="87f00-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87f00-107">EXAMPLES</span></span>

### <span data-ttu-id="87f00-108">Beispiel 1: Erstellen einer neuen "Move"-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="87f00-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="87f00-109">Erstellen Sie eine neue "Move"-Sammlung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87f00-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="87f00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87f00-110">PARAMETERS</span></span>

### <span data-ttu-id="87f00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f00-111">-DefaultProfile</span></span>
<span data-ttu-id="87f00-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87f00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f00-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="87f00-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="87f00-114">Ruft die Prinzipal-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="87f00-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="87f00-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="87f00-115">-IdentityTenantId</span></span>
<span data-ttu-id="87f00-116">Ruft die Mandanten-ID ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="87f00-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="87f00-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="87f00-117">-IdentityType</span></span>
<span data-ttu-id="87f00-118">Der für den Verschiebedienst der Region verwendete Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="87f00-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="87f00-119">-Location</span><span class="sxs-lookup"><span data-stu-id="87f00-119">-Location</span></span>
<span data-ttu-id="87f00-120">Der geo-Standort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="87f00-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="87f00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87f00-121">-Name</span></span>
<span data-ttu-id="87f00-122">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="87f00-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="87f00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f00-123">-ResourceGroupName</span></span>
<span data-ttu-id="87f00-124">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="87f00-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="87f00-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="87f00-125">-SourceRegion</span></span>
<span data-ttu-id="87f00-126">Ruft die Quellregion ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="87f00-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="87f00-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87f00-127">-SubscriptionId</span></span>
<span data-ttu-id="87f00-128">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="87f00-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="87f00-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="87f00-129">-Tag</span></span>
<span data-ttu-id="87f00-130">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="87f00-130">Resource tags.</span></span>

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

### <span data-ttu-id="87f00-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="87f00-131">-TargetRegion</span></span>
<span data-ttu-id="87f00-132">Ruft die Zielregion ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="87f00-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="87f00-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87f00-133">-Confirm</span></span>
<span data-ttu-id="87f00-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87f00-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f00-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="87f00-135">-WhatIf</span></span>
<span data-ttu-id="87f00-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87f00-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f00-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87f00-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f00-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f00-138">CommonParameters</span></span>
<span data-ttu-id="87f00-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f00-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f00-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87f00-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f00-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87f00-141">INPUTS</span></span>

## <span data-ttu-id="87f00-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87f00-142">OUTPUTS</span></span>

### <span data-ttu-id="87f00-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="87f00-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="87f00-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87f00-144">NOTES</span></span>

<span data-ttu-id="87f00-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="87f00-145">ALIASES</span></span>

## <span data-ttu-id="87f00-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87f00-146">RELATED LINKS</span></span>

