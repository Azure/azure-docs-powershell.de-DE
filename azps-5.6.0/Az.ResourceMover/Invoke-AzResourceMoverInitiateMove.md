---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943565"
---
# <span data-ttu-id="ddbca-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="ddbca-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="ddbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddbca-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbca-103">Verschiebt den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ddbca-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ddbca-104">Der Verschiebenvorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden. Bei erfolgreichem Abschluss übergeht moveResource moveState einen Übergang zu CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ddbca-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ddbca-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ddbca-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ddbca-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddbca-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddbca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddbca-107">DESCRIPTION</span></span>
<span data-ttu-id="ddbca-108">Verschiebt den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ddbca-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ddbca-109">Der Verschiebenvorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden. Bei erfolgreichem Abschluss übergeht moveResource moveState einen Übergang zu CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ddbca-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ddbca-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ddbca-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ddbca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddbca-111">EXAMPLES</span></span>

### <span data-ttu-id="ddbca-112">Beispiel 1: Überprüfen Sie die Abhängigkeiten, bevor Sie verschieben für die Ressourcen initiieren.</span><span class="sxs-lookup"><span data-stu-id="ddbca-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="ddbca-113">Überprüfen Sie die Abhängigkeiten, bevor Sie verschieben für die Ressourcen initiieren.</span><span class="sxs-lookup"><span data-stu-id="ddbca-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="ddbca-114">Beispiel 2: Initiieren von Verschieben für den Satz von Ressourcen in der Sammlung Verschieben mit "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="ddbca-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="ddbca-115">Initiieren Sie Verschieben für den Satz von Ressourcen in der Sammlung Verschieben mit "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="ddbca-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ddbca-116">Beispiel 3: Initiieren von Verschieben für den Satz von Ressourcen in der Sammlung "Verschieben" mit "SourceARMID" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="ddbca-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="ddbca-117">Initiieren Sie Verschieben für den Satz von Ressourcen in der Sammlung Verschieben mit "SourceARMID" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="ddbca-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="ddbca-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ddbca-118">PARAMETERS</span></span>

### <span data-ttu-id="ddbca-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddbca-119">-AsJob</span></span>
<span data-ttu-id="ddbca-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ddbca-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ddbca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbca-121">-DefaultProfile</span></span>
<span data-ttu-id="ddbca-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddbca-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbca-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ddbca-123">-MoveCollectionName</span></span>
<span data-ttu-id="ddbca-124">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="ddbca-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ddbca-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ddbca-125">-MoveResource</span></span>
<span data-ttu-id="ddbca-126">Ruft die Liste der Ressourcen-ID ab oder legt sie fest, standardmäßig akzeptiert sie die verschieben-Ressourcen-ID, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="ddbca-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ddbca-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ddbca-127">-MoveResourceInputType</span></span>
<span data-ttu-id="ddbca-128">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="ddbca-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ddbca-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddbca-129">-NoWait</span></span>
<span data-ttu-id="ddbca-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ddbca-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddbca-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbca-131">-ResourceGroupName</span></span>
<span data-ttu-id="ddbca-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddbca-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ddbca-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddbca-133">-SubscriptionId</span></span>
<span data-ttu-id="ddbca-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ddbca-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="ddbca-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ddbca-135">-ValidateOnly</span></span>
<span data-ttu-id="ddbca-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur die Erforderliche ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="ddbca-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ddbca-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddbca-137">-Confirm</span></span>
<span data-ttu-id="ddbca-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddbca-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbca-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbca-139">-WhatIf</span></span>
<span data-ttu-id="ddbca-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddbca-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddbca-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddbca-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbca-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbca-142">CommonParameters</span></span>
<span data-ttu-id="ddbca-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbca-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbca-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddbca-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbca-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddbca-145">INPUTS</span></span>

## <span data-ttu-id="ddbca-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddbca-146">OUTPUTS</span></span>

### <span data-ttu-id="ddbca-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ddbca-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="ddbca-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ddbca-148">NOTES</span></span>

<span data-ttu-id="ddbca-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ddbca-149">ALIASES</span></span>

## <span data-ttu-id="ddbca-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ddbca-150">RELATED LINKS</span></span>

