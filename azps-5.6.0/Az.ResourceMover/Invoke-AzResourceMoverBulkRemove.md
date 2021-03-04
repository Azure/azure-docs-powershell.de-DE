---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943582"
---
# <span data-ttu-id="c088f-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="c088f-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="c088f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c088f-102">SYNOPSIS</span></span>
<span data-ttu-id="c088f-103">Entfernt den Satz der im Anforderungstext enthaltenen Verschieberessourcen aus der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c088f-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="c088f-104">Die Orchestrierung erfolgt nach Dienst.</span><span class="sxs-lookup"><span data-stu-id="c088f-104">The orchestration is done by service.</span></span>
<span data-ttu-id="c088f-105">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c088f-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c088f-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c088f-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c088f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c088f-107">DESCRIPTION</span></span>
<span data-ttu-id="c088f-108">Entfernt den Satz der im Anforderungstext enthaltenen Verschieberessourcen aus der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c088f-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="c088f-109">Die Orchestrierung erfolgt nach Dienst.</span><span class="sxs-lookup"><span data-stu-id="c088f-109">The orchestration is done by service.</span></span>
<span data-ttu-id="c088f-110">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c088f-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c088f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c088f-111">EXAMPLES</span></span>

### <span data-ttu-id="c088f-112">Beispiel 1: Überprüfen der Abhängigkeiten vor dem Entfernen der Verschieben von Ressourcen aus der Sammlung "Verschieben"</span><span class="sxs-lookup"><span data-stu-id="c088f-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="c088f-113">Überprüfen Sie die Abhängigkeiten, bevor Sie die Ressourcen aus der Sammlung verschieben entfernen.</span><span class="sxs-lookup"><span data-stu-id="c088f-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="c088f-114">Beispiel 2: Entfernen der Move Resource from Move Collection mit "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="c088f-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="c088f-115">Entfernen der Move Resource from Move Collection mithilfe von "MoveResource Name" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="c088f-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="c088f-116">Beispiel 3: Entfernen der Move Resource from Move Collection mit "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="c088f-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="c088f-117">Entfernen der Move Resource from Move Collection mithilfe von "SourceARMID" als Eingabe</span><span class="sxs-lookup"><span data-stu-id="c088f-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="c088f-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c088f-118">PARAMETERS</span></span>

### <span data-ttu-id="c088f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c088f-119">-AsJob</span></span>
<span data-ttu-id="c088f-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c088f-120">Run the command as a job</span></span>

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

### <span data-ttu-id="c088f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c088f-121">-DefaultProfile</span></span>
<span data-ttu-id="c088f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c088f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c088f-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c088f-123">-MoveCollectionName</span></span>
<span data-ttu-id="c088f-124">.</span><span class="sxs-lookup"><span data-stu-id="c088f-124">.</span></span>

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

### <span data-ttu-id="c088f-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="c088f-125">-MoveResource</span></span>
<span data-ttu-id="c088f-126">Ruft die Liste der Ressourcen-ID ab oder legt sie fest, standardmäßig akzeptiert sie die verschieben-Ressourcen-ID, es sei denn, der Eingabetyp wird über die moveResourceInputType-Eigenschaft gewechselt.</span><span class="sxs-lookup"><span data-stu-id="c088f-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c088f-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="c088f-127">-MoveResourceInputType</span></span>
<span data-ttu-id="c088f-128">Definiert den Eingabetyp der Verschieberessource.</span><span class="sxs-lookup"><span data-stu-id="c088f-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="c088f-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c088f-129">-NoWait</span></span>
<span data-ttu-id="c088f-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c088f-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c088f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c088f-131">-ResourceGroupName</span></span>
<span data-ttu-id="c088f-132">.</span><span class="sxs-lookup"><span data-stu-id="c088f-132">.</span></span>

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

### <span data-ttu-id="c088f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c088f-133">-SubscriptionId</span></span>
<span data-ttu-id="c088f-134">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c088f-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="c088f-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="c088f-135">-ValidateOnly</span></span>
<span data-ttu-id="c088f-136">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Vorgang nur die Erforderliche ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="c088f-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="c088f-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c088f-137">-Confirm</span></span>
<span data-ttu-id="c088f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c088f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c088f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c088f-139">-WhatIf</span></span>
<span data-ttu-id="c088f-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c088f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c088f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c088f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c088f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c088f-142">CommonParameters</span></span>
<span data-ttu-id="c088f-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c088f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c088f-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c088f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c088f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c088f-145">INPUTS</span></span>

## <span data-ttu-id="c088f-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c088f-146">OUTPUTS</span></span>

### <span data-ttu-id="c088f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c088f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="c088f-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c088f-148">NOTES</span></span>

<span data-ttu-id="c088f-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c088f-149">ALIASES</span></span>

## <span data-ttu-id="c088f-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c088f-150">RELATED LINKS</span></span>

