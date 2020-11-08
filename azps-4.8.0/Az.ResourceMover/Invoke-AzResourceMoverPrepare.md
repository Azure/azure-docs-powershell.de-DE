---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009559"
---
# <span data-ttu-id="641d3-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="641d3-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="641d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="641d3-102">SYNOPSIS</span></span>
<span data-ttu-id="641d3-103">Initiiert vorbereiten für die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="641d3-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="641d3-104">Der Prepare-Vorgang befindet sich auf der moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="641d3-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="641d3-105">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="641d3-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="641d3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="641d3-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="641d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="641d3-107">DESCRIPTION</span></span>
<span data-ttu-id="641d3-108">Initiiert vorbereiten für die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="641d3-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="641d3-109">Der Prepare-Vorgang befindet sich auf der moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="641d3-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="641d3-110">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="641d3-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="641d3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="641d3-111">EXAMPLES</span></span>

### <span data-ttu-id="641d3-112">Beispiel 1: Überprüfen des dependecies vor dem Vorbereiten der Ressourcen</span><span class="sxs-lookup"><span data-stu-id="641d3-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
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

<span data-ttu-id="641d3-113">Überprüfen Sie die dependecies, bevor Sie die Ressourcen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="641d3-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="641d3-114">Beispiel 2: Initiieren der Vorbereitung auf die Gruppe von Ressourcen in der Move-Sammlung unter Verwendung von "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="641d3-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="641d3-115">Initiieren Sie Vorbereiten der Gruppe von Ressourcen in der Move-Sammlung unter Verwendung von "MoveResource Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="641d3-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="641d3-116">Beispiel 3: Initiieren der Vorbereitung auf die Gruppe von Ressourcen in der Move-Sammlung mit "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="641d3-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
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

<span data-ttu-id="641d3-117">Initiieren Sie vorbereiten für den Satz von Ressourcen in der Move-Sammlung mit "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="641d3-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="641d3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="641d3-118">PARAMETERS</span></span>

### <span data-ttu-id="641d3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="641d3-119">-AsJob</span></span>
<span data-ttu-id="641d3-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="641d3-120">Run the command as a job</span></span>

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

### <span data-ttu-id="641d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641d3-121">-DefaultProfile</span></span>
<span data-ttu-id="641d3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="641d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="641d3-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="641d3-123">-MoveCollectionName</span></span>
<span data-ttu-id="641d3-124">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="641d3-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="641d3-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="641d3-125">-MoveResource</span></span>
<span data-ttu-id="641d3-126">Ruft die Liste der Ressourcen-IDs ab oder legt Sie fest, akzeptiert standardmäßig die Move-Ressourcen-IDs, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="641d3-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="641d3-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="641d3-127">-MoveResourceInputType</span></span>
<span data-ttu-id="641d3-128">Definiert den Eingabetyp "Ressource verschieben".</span><span class="sxs-lookup"><span data-stu-id="641d3-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="641d3-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="641d3-129">-NoWait</span></span>
<span data-ttu-id="641d3-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="641d3-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="641d3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641d3-131">-ResourceGroupName</span></span>
<span data-ttu-id="641d3-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="641d3-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="641d3-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="641d3-133">-SubscriptionId</span></span>
<span data-ttu-id="641d3-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="641d3-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="641d3-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="641d3-135">-ValidateOnly</span></span>
<span data-ttu-id="641d3-136">Ruft einen Wert ab, der angibt, ob der Vorgang nur Voraussetzungen ausführen muss, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="641d3-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="641d3-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="641d3-137">-Confirm</span></span>
<span data-ttu-id="641d3-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="641d3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="641d3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="641d3-139">-WhatIf</span></span>
<span data-ttu-id="641d3-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="641d3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="641d3-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="641d3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="641d3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641d3-142">CommonParameters</span></span>
<span data-ttu-id="641d3-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641d3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641d3-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="641d3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641d3-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="641d3-145">INPUTS</span></span>

## <span data-ttu-id="641d3-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="641d3-146">OUTPUTS</span></span>

### <span data-ttu-id="641d3-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="641d3-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="641d3-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="641d3-148">NOTES</span></span>

<span data-ttu-id="641d3-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="641d3-149">ALIASES</span></span>

## <span data-ttu-id="641d3-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="641d3-150">RELATED LINKS</span></span>

