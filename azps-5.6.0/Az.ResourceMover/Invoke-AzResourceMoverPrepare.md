---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943564"
---
# <span data-ttu-id="d5de3-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="d5de3-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="d5de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5de3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5de3-103">Initiiert die Vorbereitung für den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d5de3-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="d5de3-104">Der Vorbereitungsvorgang befindet sich auf den moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="d5de3-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d5de3-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d5de3-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d5de3-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5de3-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5de3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5de3-107">DESCRIPTION</span></span>
<span data-ttu-id="d5de3-108">Initiiert die Vorbereitung für den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d5de3-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="d5de3-109">Der Vorbereitungsvorgang befindet sich auf den moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="d5de3-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d5de3-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d5de3-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d5de3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5de3-111">EXAMPLES</span></span>

### <span data-ttu-id="d5de3-112">Beispiel 1: Überprüfen Sie die Abhängigkeiten, bevor Sie die Ressourcen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="d5de3-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="d5de3-113">Holen Sie sich die erforderlichen abhängigen Ressourcen, die ebenfalls vorbereitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d5de3-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="d5de3-114">Überprüfen Sie die Abhängigkeiten, bevor Sie die Ressourcen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="d5de3-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="d5de3-115">Holen Sie sich die erforderlichen abhängigen Ressourcen, die ebenfalls vorbereitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d5de3-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="d5de3-116">Beispiel 2: Initiieren der Vorbereitung für den Satz von Ressourcen in der Sammlung "Verschieben" mithilfe von "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="d5de3-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="d5de3-117">Starten Sie die Vorbereitung für den Satz von Ressourcen in der Sammlung Verschieben mit "MoveResource-Name" als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="d5de3-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="d5de3-118">Beispiel 3: Initiieren der Vorbereitung für den Satz von Ressourcen in der Sammlung "Verschieben" mit "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="d5de3-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="d5de3-119">Starten Sie die Vorbereitung für den Satz von Ressourcen in der Sammlung Verschieben mit "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="d5de3-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="d5de3-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5de3-120">PARAMETERS</span></span>

### <span data-ttu-id="d5de3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5de3-121">-AsJob</span></span>
<span data-ttu-id="d5de3-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d5de3-122">Run the command as a job</span></span>

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

### <span data-ttu-id="d5de3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5de3-123">-DefaultProfile</span></span>
<span data-ttu-id="d5de3-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5de3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5de3-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d5de3-125">-MoveCollectionName</span></span>
<span data-ttu-id="d5de3-126">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="d5de3-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d5de3-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="d5de3-127">-MoveResource</span></span>
<span data-ttu-id="d5de3-128">Ruft die Liste der Ressourcen-ID ab oder legt sie fest, standardmäßig akzeptiert sie die verschieben-Ressourcen-ID, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="d5de3-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="d5de3-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="d5de3-129">-MoveResourceInputType</span></span>
<span data-ttu-id="d5de3-130">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="d5de3-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="d5de3-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5de3-131">-NoWait</span></span>
<span data-ttu-id="d5de3-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d5de3-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5de3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5de3-133">-ResourceGroupName</span></span>
<span data-ttu-id="d5de3-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d5de3-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d5de3-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5de3-135">-SubscriptionId</span></span>
<span data-ttu-id="d5de3-136">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d5de3-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="d5de3-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="d5de3-137">-ValidateOnly</span></span>
<span data-ttu-id="d5de3-138">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur die Erforderliche ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="d5de3-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="d5de3-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5de3-139">-Confirm</span></span>
<span data-ttu-id="d5de3-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5de3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5de3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5de3-141">-WhatIf</span></span>
<span data-ttu-id="d5de3-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5de3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5de3-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5de3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5de3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5de3-144">CommonParameters</span></span>
<span data-ttu-id="d5de3-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5de3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5de3-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5de3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5de3-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5de3-147">INPUTS</span></span>

## <span data-ttu-id="d5de3-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5de3-148">OUTPUTS</span></span>

### <span data-ttu-id="d5de3-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d5de3-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="d5de3-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5de3-150">NOTES</span></span>

<span data-ttu-id="d5de3-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d5de3-151">ALIASES</span></span>

## <span data-ttu-id="d5de3-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5de3-152">RELATED LINKS</span></span>

