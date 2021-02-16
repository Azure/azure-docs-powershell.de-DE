---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169124"
---
# <span data-ttu-id="70a5a-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="70a5a-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="70a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="70a5a-103">Verwirft die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="70a5a-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="70a5a-104">Der Verwerfenvorgang wird für die moveResources im moveState-Element "CommitPending" oder "DiscardFailed" ausgelöst. Bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="70a5a-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="70a5a-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70a5a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="70a5a-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70a5a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70a5a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70a5a-107">DESCRIPTION</span></span>
<span data-ttu-id="70a5a-108">Verwirft die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="70a5a-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="70a5a-109">Der Verwerfenvorgang wird für die moveResources im moveState-Element "CommitPending" oder "DiscardFailed" ausgelöst. Bei einem erfolgreichen Abschluss übertäft moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="70a5a-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="70a5a-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70a5a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="70a5a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70a5a-111">EXAMPLES</span></span>

### <span data-ttu-id="70a5a-112">Beispiel 1: Überprüfen Sie die Abhängigkeiten vor dem Verwerfen der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="70a5a-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="70a5a-113">Überprüfen Sie die Abhängigkeiten vor dem Verwerfen der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="70a5a-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="70a5a-114">Beispiel 2: Verwirft die Verlagerung der Ressourcen unter Verwendung von "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="70a5a-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="70a5a-115">Verwirft die Bewegung der Ressourcen unter Verwendung von "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="70a5a-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="70a5a-116">Beispiel 3: Verwirft die Bewegung der Ressourcen mit "SourceARMID" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="70a5a-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="70a5a-117">Verwirft die Bewegung der Ressourcen, die "SourceARMID" als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="70a5a-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="70a5a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70a5a-118">PARAMETERS</span></span>

### <span data-ttu-id="70a5a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a5a-119">-AsJob</span></span>
<span data-ttu-id="70a5a-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="70a5a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="70a5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a5a-121">-DefaultProfile</span></span>
<span data-ttu-id="70a5a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70a5a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70a5a-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="70a5a-123">-MoveResource</span></span>
<span data-ttu-id="70a5a-124">Ruft die Liste der Ressourcen-ID ab oder legt sie fest. Standardmäßig werden die ID der verschiebten Ressourcen akzeptiert, es sei denn, der Eingabetyp wird über die "moveResourceInputType"-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="70a5a-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="70a5a-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="70a5a-125">-MoveResourceInputType</span></span>
<span data-ttu-id="70a5a-126">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="70a5a-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="70a5a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="70a5a-127">-Name</span></span>
<span data-ttu-id="70a5a-128">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="70a5a-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="70a5a-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="70a5a-129">-NoWait</span></span>
<span data-ttu-id="70a5a-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="70a5a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70a5a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a5a-131">-ResourceGroupName</span></span>
<span data-ttu-id="70a5a-132">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="70a5a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="70a5a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70a5a-133">-SubscriptionId</span></span>
<span data-ttu-id="70a5a-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="70a5a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="70a5a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="70a5a-135">-ValidateOnly</span></span>
<span data-ttu-id="70a5a-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur eine Voraussetzung ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="70a5a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="70a5a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70a5a-137">-Confirm</span></span>
<span data-ttu-id="70a5a-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70a5a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a5a-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70a5a-139">-WhatIf</span></span>
<span data-ttu-id="70a5a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70a5a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70a5a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70a5a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a5a-142">CommonParameters</span></span>
<span data-ttu-id="70a5a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a5a-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70a5a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a5a-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70a5a-145">INPUTS</span></span>

## <span data-ttu-id="70a5a-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70a5a-146">OUTPUTS</span></span>

### <span data-ttu-id="70a5a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="70a5a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="70a5a-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70a5a-148">NOTES</span></span>

<span data-ttu-id="70a5a-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="70a5a-149">ALIASES</span></span>

## <span data-ttu-id="70a5a-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70a5a-150">RELATED LINKS</span></span>

