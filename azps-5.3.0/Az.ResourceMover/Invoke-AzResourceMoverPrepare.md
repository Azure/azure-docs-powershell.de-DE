---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459564"
---
# <span data-ttu-id="d9507-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="d9507-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="d9507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9507-102">SYNOPSIS</span></span>
<span data-ttu-id="d9507-103">Initiieren bereiten die Gruppe von Ressourcen vor, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d9507-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="d9507-104">Der Vorbereitungsvorgang befindet sich in den moveResources, die sich im moveState-Element "PreparePending" oder "PrepareFailed" befinden, und nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="d9507-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d9507-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9507-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d9507-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9507-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9507-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9507-107">DESCRIPTION</span></span>
<span data-ttu-id="d9507-108">Initiieren bereiten die Gruppe von Ressourcen vor, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d9507-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="d9507-109">Der Vorbereitungsvorgang befindet sich in den moveResources, die sich im moveState-Element "PreparePending" oder "PrepareFailed" befinden, und nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="d9507-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d9507-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9507-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d9507-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9507-111">EXAMPLES</span></span>

### <span data-ttu-id="d9507-112">Beispiel 1: Überprüfen der Abhängigkeiten vor der Vorbereitung auf die Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d9507-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="d9507-113">Überprüfen Sie die Abhängigkeiten, bevor Sie sich auf die Ressourcen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="d9507-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="d9507-114">Beispiel 2: Initiieren der Vorbereitung für die Gruppe von Ressourcen in der "Move Collection" mithilfe von "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9507-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="d9507-115">Initiieren Sie die Vorbereitung der Gruppe von Ressourcen in der Sammlung "Verschieben", indem Sie "MoveResource-Name" als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9507-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="d9507-116">Beispiel 3: Initiieren der Vorbereitung für die Gruppe von Ressourcen in der Sammlung "Verschieben" mithilfe von "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="d9507-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="d9507-117">Initiieren Sie die Vorbereitung der Gruppe von Ressourcen in der Sammlung "Verschieben" mit "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="d9507-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="d9507-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9507-118">PARAMETERS</span></span>

### <span data-ttu-id="d9507-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9507-119">-AsJob</span></span>
<span data-ttu-id="d9507-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d9507-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d9507-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9507-121">-DefaultProfile</span></span>
<span data-ttu-id="d9507-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9507-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9507-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d9507-123">-MoveCollectionName</span></span>
<span data-ttu-id="d9507-124">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="d9507-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d9507-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="d9507-125">-MoveResource</span></span>
<span data-ttu-id="d9507-126">Ruft die Liste der Ressourcen-ID ab oder legt sie fest. Standardmäßig werden die ID der verschiebten Ressourcen akzeptiert, es sei denn, der Eingabetyp wird über die "moveResourceInputType"-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="d9507-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9507-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="d9507-127">-MoveResourceInputType</span></span>
<span data-ttu-id="d9507-128">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="d9507-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9507-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9507-129">-NoWait</span></span>
<span data-ttu-id="d9507-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d9507-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9507-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9507-131">-ResourceGroupName</span></span>
<span data-ttu-id="d9507-132">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d9507-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d9507-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9507-133">-SubscriptionId</span></span>
<span data-ttu-id="d9507-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d9507-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="d9507-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="d9507-135">-ValidateOnly</span></span>
<span data-ttu-id="d9507-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur eine Voraussetzung ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="d9507-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="d9507-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9507-137">-Confirm</span></span>
<span data-ttu-id="d9507-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9507-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9507-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9507-139">-WhatIf</span></span>
<span data-ttu-id="d9507-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9507-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9507-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9507-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9507-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9507-142">CommonParameters</span></span>
<span data-ttu-id="d9507-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9507-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9507-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9507-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9507-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9507-145">INPUTS</span></span>

## <span data-ttu-id="d9507-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9507-146">OUTPUTS</span></span>

### <span data-ttu-id="d9507-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d9507-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d9507-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9507-148">NOTES</span></span>

<span data-ttu-id="d9507-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d9507-149">ALIASES</span></span>

## <span data-ttu-id="d9507-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9507-150">RELATED LINKS</span></span>

