---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174489"
---
# <span data-ttu-id="ae6d1-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ae6d1-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ae6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6d1-103">Erstellt oder aktualisiert eine "Verschieben"-Ressource in der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="ae6d1-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ae6d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae6d1-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae6d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6d1-106">Erstellt oder aktualisiert eine "Verschieben"-Ressource in der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="ae6d1-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ae6d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6d1-108">Beispiel 1: Hinzufügen einer Ressource zur Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="ae6d1-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="ae6d1-109">Hinzufügen einer Ressource zur Sammlung zum Verschieben innerhalb des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="ae6d1-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="ae6d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae6d1-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6d1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae6d1-111">-AsJob</span></span>
<span data-ttu-id="ae6d1-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ae6d1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ae6d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6d1-113">-DefaultProfile</span></span>
<span data-ttu-id="ae6d1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6d1-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="ae6d1-115">-DependsOnOverride</span></span>
<span data-ttu-id="ae6d1-116">Ruft die Außerkraftsetzungen der Verschieberessourcenabhängigkeiten ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="ae6d1-117">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu DEN DEPENDSONOVERRIDE-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d1-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="ae6d1-118">-ExistingTargetId</span></span>
<span data-ttu-id="ae6d1-119">Ruft die vorhandene Ziel-ID ARM der Ressource ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ae6d1-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ae6d1-120">-MoveCollectionName</span></span>
<span data-ttu-id="ae6d1-121">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="ae6d1-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ae6d1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ae6d1-122">-Name</span></span>
<span data-ttu-id="ae6d1-123">Der Name der "Ressource verschieben".</span><span class="sxs-lookup"><span data-stu-id="ae6d1-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d1-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae6d1-124">-NoWait</span></span>
<span data-ttu-id="ae6d1-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ae6d1-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae6d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae6d1-127">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ae6d1-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ae6d1-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="ae6d1-129">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-129">The resource type.</span></span>
<span data-ttu-id="ae6d1-130">Der Wert kann z. B. "Microsoft.Compute/virtualMachines" sein.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ae6d1-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ae6d1-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ae6d1-132">Ruft den Zielressourcennamen ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ae6d1-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="ae6d1-133">-SourceId</span></span>
<span data-ttu-id="ae6d1-134">Ruft die Quell-ARM-ID der Ressource ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ae6d1-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ae6d1-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="ae6d1-136">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-136">The resource type.</span></span>
<span data-ttu-id="ae6d1-137">Der Wert kann z. B. "Microsoft.Compute/virtualMachines" sein.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ae6d1-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ae6d1-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ae6d1-139">Ruft den Zielressourcennamen ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ae6d1-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae6d1-140">-SubscriptionId</span></span>
<span data-ttu-id="ae6d1-141">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="ae6d1-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae6d1-142">-Confirm</span></span>
<span data-ttu-id="ae6d1-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6d1-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae6d1-144">-WhatIf</span></span>
<span data-ttu-id="ae6d1-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6d1-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6d1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6d1-147">CommonParameters</span></span>
<span data-ttu-id="ae6d1-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6d1-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae6d1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6d1-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae6d1-150">INPUTS</span></span>

## <span data-ttu-id="ae6d1-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae6d1-151">OUTPUTS</span></span>

### <span data-ttu-id="ae6d1-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="ae6d1-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="ae6d1-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae6d1-153">NOTES</span></span>

<span data-ttu-id="ae6d1-154">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ae6d1-154">ALIASES</span></span>

<span data-ttu-id="ae6d1-155">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ae6d1-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae6d1-156">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae6d1-157">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae6d1-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Ruft Außerkraftsetzungen für die Abhängigkeiten der Verschieberessourcen ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="ae6d1-159">`[Id <String>]`: Ruft die ARM der abhängigen Ressource ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="ae6d1-160">`[TargetId <String>]`: Ruft die Ressourcen-ID ARM der "MoveResource" oder der ARM der abhängigen Ressource ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="ae6d1-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="ae6d1-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae6d1-161">RELATED LINKS</span></span>

