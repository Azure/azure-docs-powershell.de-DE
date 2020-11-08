---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178426"
---
# <span data-ttu-id="ac481-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ac481-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ac481-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac481-102">SYNOPSIS</span></span>
<span data-ttu-id="ac481-103">Erstellt oder aktualisiert eine Verschiebungs Ressource in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ac481-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ac481-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac481-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac481-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac481-105">DESCRIPTION</span></span>
<span data-ttu-id="ac481-106">Erstellt oder aktualisiert eine Verschiebungs Ressource in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ac481-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ac481-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac481-107">EXAMPLES</span></span>

### <span data-ttu-id="ac481-108">Beispiel 1: Hinzufügen einer Ressource zur Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ac481-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="ac481-109">Hinzufügen einer Ressource zur Move-Sammlung innerhalb des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="ac481-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="ac481-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac481-110">PARAMETERS</span></span>

### <span data-ttu-id="ac481-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac481-111">-AsJob</span></span>
<span data-ttu-id="ac481-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ac481-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ac481-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac481-113">-DefaultProfile</span></span>
<span data-ttu-id="ac481-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac481-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac481-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="ac481-115">-DependsOnOverride</span></span>
<span data-ttu-id="ac481-116">Ruft die Außerkraftsetzungen zum Verschieben von Ressourcen ab oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="ac481-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="ac481-117">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für DEPENDSONOVERRIDE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ac481-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac481-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="ac481-118">-ExistingTargetId</span></span>
<span data-ttu-id="ac481-119">Ruft die vorhandene Ziel Armlänge-ID der Ressource ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ac481-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ac481-120">-MoveCollectionName</span></span>
<span data-ttu-id="ac481-121">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ac481-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ac481-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ac481-122">-Name</span></span>
<span data-ttu-id="ac481-123">Der Name der Verschiebungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac481-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="ac481-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ac481-124">-NoWait</span></span>
<span data-ttu-id="ac481-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ac481-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac481-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac481-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac481-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac481-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ac481-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ac481-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="ac481-129">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ac481-129">The resource type.</span></span>
<span data-ttu-id="ac481-130">Der Wert kann beispielsweise Microsoft. Compute/virtualMachines sein.</span><span class="sxs-lookup"><span data-stu-id="ac481-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ac481-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ac481-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ac481-132">Ruft den Namen der Zielressource ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ac481-133">-Quellpfad</span><span class="sxs-lookup"><span data-stu-id="ac481-133">-SourceId</span></span>
<span data-ttu-id="ac481-134">Ruft die ID des Quell Armes der Ressource ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ac481-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ac481-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="ac481-136">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ac481-136">The resource type.</span></span>
<span data-ttu-id="ac481-137">Der Wert kann beispielsweise Microsoft. Compute/virtualMachines sein.</span><span class="sxs-lookup"><span data-stu-id="ac481-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ac481-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ac481-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ac481-139">Ruft den Namen der Zielressource ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ac481-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ac481-140">-SubscriptionId</span></span>
<span data-ttu-id="ac481-141">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ac481-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="ac481-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac481-142">-Confirm</span></span>
<span data-ttu-id="ac481-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac481-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac481-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac481-144">-WhatIf</span></span>
<span data-ttu-id="ac481-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac481-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac481-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac481-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac481-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac481-147">CommonParameters</span></span>
<span data-ttu-id="ac481-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac481-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac481-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac481-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac481-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac481-150">INPUTS</span></span>

## <span data-ttu-id="ac481-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac481-151">OUTPUTS</span></span>

### <span data-ttu-id="ac481-152">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="ac481-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="ac481-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac481-153">NOTES</span></span>

<span data-ttu-id="ac481-154">Aliase</span><span class="sxs-lookup"><span data-stu-id="ac481-154">ALIASES</span></span>

<span data-ttu-id="ac481-155">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac481-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac481-156">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac481-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac481-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ac481-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac481-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: Ruft die Außerkraftsetzungen für das Verschieben von Ressourcenabhängigkeiten ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="ac481-159">`[Id <String>]`: Ruft die Arm-ID der abhängigen Ressource ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="ac481-160">`[TargetId <String>]`: Ruft die ID des Ressourcen Armes der MoveResource oder der Ressourcen-Arm-ID der abhängigen Ressource ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="ac481-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="ac481-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac481-161">RELATED LINKS</span></span>

