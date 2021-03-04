---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943577"
---
# <span data-ttu-id="9f6d7-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="9f6d7-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="9f6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6d7-103">Über commits the set of resources included in the request body.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="9f6d7-104">Der Commitvorgang wird für die moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu Committed.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="9f6d7-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9f6d7-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f6d7-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f6d7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f6d7-107">DESCRIPTION</span></span>
<span data-ttu-id="9f6d7-108">Über commits the set of resources included in the request body.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="9f6d7-109">Der Commitvorgang wird für die moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu Committed.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="9f6d7-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9f6d7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f6d7-111">EXAMPLES</span></span>

### <span data-ttu-id="9f6d7-112">Beispiel 1: Überprüfen Sie die Abhängigkeiten vor dem Commit der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="9f6d7-113">Überprüfen Sie die Abhängigkeiten vor dem Commit der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="9f6d7-114">Beispiel 2: Legen Sie den Satz von Ressourcen in der Sammlung Verschieben mithilfe von "MoveResource-Name" als Eingabe fest.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="9f6d7-115">Legen Sie die Gruppe von Ressourcen in der Sammlung Verschieben fest, indem Sie "MoveResource-Name" als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="9f6d7-116">Beispiel 3: Legen Sie den Satz von Ressourcen in der Sammlung "Verschieben" mithilfe von "SourceARMID" als Eingabe fest.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="9f6d7-117">Legen Sie die Gruppe von Ressourcen in der Sammlung Verschieben fest, indem Sie "SourceARMID" als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="9f6d7-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f6d7-118">PARAMETERS</span></span>

### <span data-ttu-id="9f6d7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f6d7-119">-AsJob</span></span>
<span data-ttu-id="9f6d7-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9f6d7-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9f6d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6d7-121">-DefaultProfile</span></span>
<span data-ttu-id="9f6d7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6d7-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9f6d7-123">-MoveCollectionName</span></span>
<span data-ttu-id="9f6d7-124">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9f6d7-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="9f6d7-125">-MoveResource</span></span>
<span data-ttu-id="9f6d7-126">Ruft die Liste der Ressourcen-ID ab oder legt sie fest, standardmäßig akzeptiert sie die verschieben-Ressourcen-ID, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="9f6d7-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="9f6d7-127">-MoveResourceInputType</span></span>
<span data-ttu-id="9f6d7-128">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="9f6d7-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f6d7-129">-NoWait</span></span>
<span data-ttu-id="9f6d7-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9f6d7-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f6d7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6d7-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f6d7-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9f6d7-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f6d7-133">-SubscriptionId</span></span>
<span data-ttu-id="9f6d7-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="9f6d7-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9f6d7-135">-ValidateOnly</span></span>
<span data-ttu-id="9f6d7-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur die Erforderliche ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="9f6d7-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f6d7-137">-Confirm</span></span>
<span data-ttu-id="9f6d7-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6d7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6d7-139">-WhatIf</span></span>
<span data-ttu-id="9f6d7-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6d7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6d7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6d7-142">CommonParameters</span></span>
<span data-ttu-id="9f6d7-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6d7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6d7-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f6d7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6d7-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f6d7-145">INPUTS</span></span>

## <span data-ttu-id="9f6d7-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f6d7-146">OUTPUTS</span></span>

### <span data-ttu-id="9f6d7-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9f6d7-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="9f6d7-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f6d7-148">NOTES</span></span>

<span data-ttu-id="9f6d7-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9f6d7-149">ALIASES</span></span>

## <span data-ttu-id="9f6d7-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f6d7-150">RELATED LINKS</span></span>

