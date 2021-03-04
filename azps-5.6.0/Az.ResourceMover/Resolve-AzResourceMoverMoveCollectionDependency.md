---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: 6812849fc8fe4aa8dab21f9bbcfc13891c45e0ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943529"
---
# <span data-ttu-id="9341c-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="9341c-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="9341c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9341c-102">SYNOPSIS</span></span>
<span data-ttu-id="9341c-103">Berechnet, löst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9341c-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="9341c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9341c-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9341c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9341c-105">DESCRIPTION</span></span>
<span data-ttu-id="9341c-106">Berechnet, löst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9341c-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="9341c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9341c-107">EXAMPLES</span></span>

### <span data-ttu-id="9341c-108">Beispiel 1: Berechnen, Auflösen und Überprüfen der Abhängigkeiten der Ressourcen verschieben in der Sammlung Verschieben.</span><span class="sxs-lookup"><span data-stu-id="9341c-108">Example 1: Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 2/9/2021 2:05:04 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/c2ad006
                 6-6a69-45fe-aa70-193c240a9bc0
Message        : The resolve dependencies operation of one or more resources has failed. Check the move status of the resource for more details.
                     Possible Causes: The resolve dependencies operation of one ore more resources has failed.
                     Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : c2ad0066-6a69-45fe-aa70-193c240a9bc0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 2:05:00 AM
Status         : Succeeded
```

<span data-ttu-id="9341c-109">Berechnen, Auflösen und Überprüfen der Abhängigkeiten der Ressourcen verschieben in der Sammlung Verschieben.</span><span class="sxs-lookup"><span data-stu-id="9341c-109">Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>

## <span data-ttu-id="9341c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9341c-110">PARAMETERS</span></span>

### <span data-ttu-id="9341c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9341c-111">-AsJob</span></span>
<span data-ttu-id="9341c-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9341c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9341c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9341c-113">-DefaultProfile</span></span>
<span data-ttu-id="9341c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9341c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9341c-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9341c-115">-MoveCollectionName</span></span>
<span data-ttu-id="9341c-116">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="9341c-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9341c-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9341c-117">-NoWait</span></span>
<span data-ttu-id="9341c-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9341c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9341c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9341c-119">-ResourceGroupName</span></span>
<span data-ttu-id="9341c-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9341c-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9341c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9341c-121">-SubscriptionId</span></span>
<span data-ttu-id="9341c-122">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="9341c-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="9341c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9341c-123">-Confirm</span></span>
<span data-ttu-id="9341c-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9341c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9341c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9341c-125">-WhatIf</span></span>
<span data-ttu-id="9341c-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9341c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9341c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9341c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9341c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9341c-128">CommonParameters</span></span>
<span data-ttu-id="9341c-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9341c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9341c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9341c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9341c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9341c-131">INPUTS</span></span>

## <span data-ttu-id="9341c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9341c-132">OUTPUTS</span></span>

### <span data-ttu-id="9341c-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9341c-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="9341c-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9341c-134">NOTES</span></span>

<span data-ttu-id="9341c-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9341c-135">ALIASES</span></span>

## <span data-ttu-id="9341c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9341c-136">RELATED LINKS</span></span>

