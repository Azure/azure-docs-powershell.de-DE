---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377878"
---
# <span data-ttu-id="142fc-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="142fc-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="142fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="142fc-102">SYNOPSIS</span></span>
<span data-ttu-id="142fc-103">Über committ die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="142fc-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="142fc-104">Der Commitvorgang wird für die moveResources im moveState-Element "CommitPending" oder "CommitFailed" ausgelöst, und bei einem erfolgreichen Abschluss übergeht "moveResource moveState" zu "Committed".</span><span class="sxs-lookup"><span data-stu-id="142fc-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="142fc-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="142fc-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="142fc-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="142fc-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="142fc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="142fc-107">DESCRIPTION</span></span>
<span data-ttu-id="142fc-108">Über committ die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="142fc-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="142fc-109">Der Commitvorgang wird für die moveResources im moveState-Element "CommitPending" oder "CommitFailed" ausgelöst, und bei einem erfolgreichen Abschluss übergeht "moveResource moveState" zu "Committed".</span><span class="sxs-lookup"><span data-stu-id="142fc-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="142fc-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="142fc-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="142fc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="142fc-111">EXAMPLES</span></span>

### <span data-ttu-id="142fc-112">Beispiel 1: Überprüfen der Abhängigkeiten vor dem Commit für die Ressourcen</span><span class="sxs-lookup"><span data-stu-id="142fc-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="142fc-113">Überprüfen Sie die Abhängigkeiten vor dem Commit für die Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="142fc-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="142fc-114">Beispiel 2: Commit für den Satz von Ressourcen in der "Move Collection" mithilfe von "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="142fc-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="142fc-115">Commit für die Gruppe von Ressourcen in der Sammlung "Verschieben" unter Verwendung von "MoveResource-Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="142fc-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="142fc-116">Beispiel 3: Commit für den Satz von Ressourcen in der Sammlung "Verschieben" mithilfe von "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="142fc-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="142fc-117">Commit für die Gruppe von Ressourcen in der Sammlung "Verschieben" mithilfe von "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="142fc-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="142fc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="142fc-118">PARAMETERS</span></span>

### <span data-ttu-id="142fc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="142fc-119">-AsJob</span></span>
<span data-ttu-id="142fc-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="142fc-120">Run the command as a job</span></span>

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

### <span data-ttu-id="142fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142fc-121">-DefaultProfile</span></span>
<span data-ttu-id="142fc-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="142fc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="142fc-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="142fc-123">-MoveCollectionName</span></span>
<span data-ttu-id="142fc-124">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="142fc-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="142fc-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="142fc-125">-MoveResource</span></span>
<span data-ttu-id="142fc-126">Ruft die Liste der Ressourcen-ID ab oder legt sie fest. Standardmäßig werden die ID der verschiebten Ressourcen akzeptiert, es sei denn, der Eingabetyp wird über die "moveResourceInputType"-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="142fc-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="142fc-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="142fc-127">-MoveResourceInputType</span></span>
<span data-ttu-id="142fc-128">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="142fc-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="142fc-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="142fc-129">-NoWait</span></span>
<span data-ttu-id="142fc-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="142fc-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="142fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="142fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="142fc-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="142fc-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="142fc-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="142fc-133">-SubscriptionId</span></span>
<span data-ttu-id="142fc-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="142fc-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="142fc-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="142fc-135">-ValidateOnly</span></span>
<span data-ttu-id="142fc-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur eine Voraussetzung ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="142fc-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="142fc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="142fc-137">-Confirm</span></span>
<span data-ttu-id="142fc-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="142fc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="142fc-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="142fc-139">-WhatIf</span></span>
<span data-ttu-id="142fc-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="142fc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="142fc-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="142fc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="142fc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142fc-142">CommonParameters</span></span>
<span data-ttu-id="142fc-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="142fc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142fc-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="142fc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142fc-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="142fc-145">INPUTS</span></span>

## <span data-ttu-id="142fc-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="142fc-146">OUTPUTS</span></span>

### <span data-ttu-id="142fc-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="142fc-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="142fc-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="142fc-148">NOTES</span></span>

<span data-ttu-id="142fc-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="142fc-149">ALIASES</span></span>

## <span data-ttu-id="142fc-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="142fc-150">RELATED LINKS</span></span>

