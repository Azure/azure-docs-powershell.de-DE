---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302499"
---
# <span data-ttu-id="b4849-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="b4849-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="b4849-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4849-102">SYNOPSIS</span></span>
<span data-ttu-id="b4849-103">Verwirft den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4849-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b4849-104">Der verwerfen-Vorgang wird auf der moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="b4849-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b4849-105">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b4849-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b4849-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4849-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4849-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4849-107">DESCRIPTION</span></span>
<span data-ttu-id="b4849-108">Verwirft den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4849-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="b4849-109">Der verwerfen-Vorgang wird auf der moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="b4849-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b4849-110">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b4849-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b4849-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4849-111">EXAMPLES</span></span>

### <span data-ttu-id="b4849-112">Beispiel 1: Überprüfen Sie die dependecies vor dem verwerfen der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b4849-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
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

<span data-ttu-id="b4849-113">Überprüfen Sie die dependecies vor dem verwerfen der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b4849-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="b4849-114">Beispiel 2: verwirft den Umzug der Ressourcen mit "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4849-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="b4849-115">Verwirft den Umzug der Ressourcen mit "MoveResource Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="b4849-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="b4849-116">Beispiel 3: verwirft den Umzug der Ressourcen mit "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4849-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
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

<span data-ttu-id="b4849-117">Verwirft den Umzug der Ressourcen mit "SourceARMID" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="b4849-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="b4849-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4849-118">PARAMETERS</span></span>

### <span data-ttu-id="b4849-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4849-119">-AsJob</span></span>
<span data-ttu-id="b4849-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b4849-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b4849-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4849-121">-DefaultProfile</span></span>
<span data-ttu-id="b4849-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4849-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4849-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b4849-123">-MoveResource</span></span>
<span data-ttu-id="b4849-124">Ruft die Liste der Ressourcen-IDs ab oder legt Sie fest, akzeptiert standardmäßig die Move-Ressourcen-IDs, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="b4849-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="b4849-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="b4849-125">-MoveResourceInputType</span></span>
<span data-ttu-id="b4849-126">Definiert den Eingabetyp "Ressource verschieben".</span><span class="sxs-lookup"><span data-stu-id="b4849-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="b4849-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b4849-127">-Name</span></span>
<span data-ttu-id="b4849-128">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b4849-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b4849-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b4849-129">-NoWait</span></span>
<span data-ttu-id="b4849-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b4849-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b4849-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4849-131">-ResourceGroupName</span></span>
<span data-ttu-id="b4849-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4849-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b4849-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b4849-133">-SubscriptionId</span></span>
<span data-ttu-id="b4849-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b4849-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="b4849-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="b4849-135">-ValidateOnly</span></span>
<span data-ttu-id="b4849-136">Ruft einen Wert ab, der angibt, ob der Vorgang nur Voraussetzungen ausführen muss, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b4849-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b4849-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4849-137">-Confirm</span></span>
<span data-ttu-id="b4849-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4849-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4849-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4849-139">-WhatIf</span></span>
<span data-ttu-id="b4849-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4849-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4849-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4849-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4849-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4849-142">CommonParameters</span></span>
<span data-ttu-id="b4849-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4849-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4849-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4849-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4849-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4849-145">INPUTS</span></span>

## <span data-ttu-id="b4849-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4849-146">OUTPUTS</span></span>

### <span data-ttu-id="b4849-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b4849-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="b4849-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4849-148">NOTES</span></span>

<span data-ttu-id="b4849-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="b4849-149">ALIASES</span></span>

## <span data-ttu-id="b4849-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4849-150">RELATED LINKS</span></span>

