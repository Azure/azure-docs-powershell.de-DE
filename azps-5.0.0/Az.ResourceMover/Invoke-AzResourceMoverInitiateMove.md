---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302494"
---
# <span data-ttu-id="35688-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="35688-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="35688-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35688-102">SYNOPSIS</span></span>
<span data-ttu-id="35688-103">Verschiebt die im Anforderungstext enthaltene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35688-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="35688-104">Der Verschiebevorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu CommitPending durchführen.</span><span class="sxs-lookup"><span data-stu-id="35688-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="35688-105">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="35688-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="35688-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="35688-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35688-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35688-107">DESCRIPTION</span></span>
<span data-ttu-id="35688-108">Verschiebt die im Anforderungstext enthaltene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35688-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="35688-109">Der Verschiebevorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu CommitPending durchführen.</span><span class="sxs-lookup"><span data-stu-id="35688-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="35688-110">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="35688-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="35688-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35688-111">EXAMPLES</span></span>

### <span data-ttu-id="35688-112">Beispiel 1: Überprüfen Sie die dependecies vor dem Initiieren von Move für die Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="35688-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="35688-113">Überprüfen Sie die dependecies, bevor Sie Move für die Ressourcen initiieren.</span><span class="sxs-lookup"><span data-stu-id="35688-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="35688-114">Beispiel 2: Initiieren der Bewegung für den Satz von Ressourcen in der Move-Sammlung unter Verwendung von "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="35688-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="35688-115">Initiieren Sie die Bewegung für die Gruppe von Ressourcen in der Move-Sammlung unter Verwendung von "MoveResource Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="35688-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="35688-116">Beispiel 3: Initiieren der Bewegung für den Satz von Ressourcen in der Move-Sammlung mit "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="35688-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="35688-117">Initiieren Sie die Bewegung für den Satz von Ressourcen in der Move-Sammlung mit "SourceARMID" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="35688-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="35688-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="35688-118">PARAMETERS</span></span>

### <span data-ttu-id="35688-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35688-119">-AsJob</span></span>
<span data-ttu-id="35688-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="35688-120">Run the command as a job</span></span>

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

### <span data-ttu-id="35688-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35688-121">-DefaultProfile</span></span>
<span data-ttu-id="35688-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35688-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35688-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="35688-123">-MoveCollectionName</span></span>
<span data-ttu-id="35688-124">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="35688-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="35688-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="35688-125">-MoveResource</span></span>
<span data-ttu-id="35688-126">Ruft die Liste der Ressourcen-IDs ab oder legt Sie fest, akzeptiert standardmäßig die Move-Ressourcen-IDs, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="35688-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="35688-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="35688-127">-MoveResourceInputType</span></span>
<span data-ttu-id="35688-128">Definiert den Eingabetyp "Ressource verschieben".</span><span class="sxs-lookup"><span data-stu-id="35688-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="35688-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="35688-129">-NoWait</span></span>
<span data-ttu-id="35688-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="35688-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35688-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35688-131">-ResourceGroupName</span></span>
<span data-ttu-id="35688-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35688-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="35688-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="35688-133">-SubscriptionId</span></span>
<span data-ttu-id="35688-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="35688-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="35688-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="35688-135">-ValidateOnly</span></span>
<span data-ttu-id="35688-136">Ruft einen Wert ab, der angibt, ob der Vorgang nur Voraussetzungen ausführen muss, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="35688-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="35688-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35688-137">-Confirm</span></span>
<span data-ttu-id="35688-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35688-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35688-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35688-139">-WhatIf</span></span>
<span data-ttu-id="35688-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35688-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35688-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35688-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35688-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35688-142">CommonParameters</span></span>
<span data-ttu-id="35688-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35688-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35688-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35688-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35688-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35688-145">INPUTS</span></span>

## <span data-ttu-id="35688-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35688-146">OUTPUTS</span></span>

### <span data-ttu-id="35688-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="35688-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="35688-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="35688-148">NOTES</span></span>

<span data-ttu-id="35688-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="35688-149">ALIASES</span></span>

## <span data-ttu-id="35688-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35688-150">RELATED LINKS</span></span>

