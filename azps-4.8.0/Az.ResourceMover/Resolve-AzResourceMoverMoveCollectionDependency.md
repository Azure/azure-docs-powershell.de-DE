---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173553"
---
# <span data-ttu-id="808e2-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="808e2-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="808e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="808e2-102">SYNOPSIS</span></span>
<span data-ttu-id="808e2-103">Berechnet, löst und überprüft die Abhängigkeiten von moveResources in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="808e2-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="808e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="808e2-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="808e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="808e2-105">DESCRIPTION</span></span>
<span data-ttu-id="808e2-106">Berechnet, löst und überprüft die Abhängigkeiten von moveResources in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="808e2-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="808e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="808e2-107">EXAMPLES</span></span>

### <span data-ttu-id="808e2-108">Beispiel 1: berechnet, behebt und überprüft die Abhängigkeiten der moveresources in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="808e2-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
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

<span data-ttu-id="808e2-109">Berechnet, löst und überprüft die Abhängigkeiten von moveresources in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="808e2-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="808e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="808e2-110">PARAMETERS</span></span>

### <span data-ttu-id="808e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="808e2-111">-AsJob</span></span>
<span data-ttu-id="808e2-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="808e2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="808e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808e2-113">-DefaultProfile</span></span>
<span data-ttu-id="808e2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="808e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808e2-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="808e2-115">-MoveCollectionName</span></span>
<span data-ttu-id="808e2-116">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="808e2-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="808e2-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="808e2-117">-NoWait</span></span>
<span data-ttu-id="808e2-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="808e2-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="808e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="808e2-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="808e2-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="808e2-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="808e2-121">-SubscriptionId</span></span>
<span data-ttu-id="808e2-122">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="808e2-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="808e2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="808e2-123">-Confirm</span></span>
<span data-ttu-id="808e2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="808e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808e2-125">-WhatIf</span></span>
<span data-ttu-id="808e2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="808e2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808e2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="808e2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808e2-128">CommonParameters</span></span>
<span data-ttu-id="808e2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808e2-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="808e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808e2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="808e2-131">INPUTS</span></span>

## <span data-ttu-id="808e2-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="808e2-132">OUTPUTS</span></span>

### <span data-ttu-id="808e2-133">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="808e2-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="808e2-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="808e2-134">NOTES</span></span>

<span data-ttu-id="808e2-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="808e2-135">ALIASES</span></span>

## <span data-ttu-id="808e2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="808e2-136">RELATED LINKS</span></span>

