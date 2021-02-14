---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174465"
---
# <span data-ttu-id="1166f-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="1166f-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="1166f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1166f-102">SYNOPSIS</span></span>
<span data-ttu-id="1166f-103">Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1166f-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="1166f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1166f-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1166f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1166f-105">DESCRIPTION</span></span>
<span data-ttu-id="1166f-106">Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1166f-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="1166f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1166f-107">EXAMPLES</span></span>

### <span data-ttu-id="1166f-108">Beispiel 1: Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveresources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1166f-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="1166f-109">Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveresources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1166f-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="1166f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1166f-110">PARAMETERS</span></span>

### <span data-ttu-id="1166f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1166f-111">-AsJob</span></span>
<span data-ttu-id="1166f-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1166f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1166f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1166f-113">-DefaultProfile</span></span>
<span data-ttu-id="1166f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1166f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1166f-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1166f-115">-MoveCollectionName</span></span>
<span data-ttu-id="1166f-116">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="1166f-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1166f-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1166f-117">-NoWait</span></span>
<span data-ttu-id="1166f-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1166f-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1166f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1166f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1166f-120">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1166f-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1166f-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1166f-121">-SubscriptionId</span></span>
<span data-ttu-id="1166f-122">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1166f-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="1166f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1166f-123">-Confirm</span></span>
<span data-ttu-id="1166f-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1166f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1166f-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1166f-125">-WhatIf</span></span>
<span data-ttu-id="1166f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1166f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1166f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1166f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1166f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1166f-128">CommonParameters</span></span>
<span data-ttu-id="1166f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1166f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1166f-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1166f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1166f-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1166f-131">INPUTS</span></span>

## <span data-ttu-id="1166f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1166f-132">OUTPUTS</span></span>

### <span data-ttu-id="1166f-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1166f-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="1166f-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1166f-134">NOTES</span></span>

<span data-ttu-id="1166f-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1166f-135">ALIASES</span></span>

## <span data-ttu-id="1166f-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1166f-136">RELATED LINKS</span></span>

