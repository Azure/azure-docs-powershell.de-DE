---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943541"
---
# <span data-ttu-id="a7dd6-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="a7dd6-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="a7dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dd6-103">Löscht eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-103">Deletes a move collection.</span></span>

## <span data-ttu-id="a7dd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7dd6-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7dd6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="a7dd6-106">Löscht eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-106">Deletes a move collection.</span></span>

## <span data-ttu-id="a7dd6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7dd6-107">EXAMPLES</span></span>

### <span data-ttu-id="a7dd6-108">Beispiel 1: Entfernen der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="a7dd6-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="a7dd6-109">Entfernen Sie die Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="a7dd6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7dd6-110">PARAMETERS</span></span>

### <span data-ttu-id="a7dd6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7dd6-111">-AsJob</span></span>
<span data-ttu-id="a7dd6-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a7dd6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a7dd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dd6-113">-DefaultProfile</span></span>
<span data-ttu-id="a7dd6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dd6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a7dd6-115">-Name</span></span>
<span data-ttu-id="a7dd6-116">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a7dd6-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7dd6-117">-NoWait</span></span>
<span data-ttu-id="a7dd6-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a7dd6-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a7dd6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7dd6-119">-PassThru</span></span>
<span data-ttu-id="a7dd6-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a7dd6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7dd6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7dd6-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a7dd6-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7dd6-123">-SubscriptionId</span></span>
<span data-ttu-id="a7dd6-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="a7dd6-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7dd6-125">-Confirm</span></span>
<span data-ttu-id="a7dd6-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7dd6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7dd6-127">-WhatIf</span></span>
<span data-ttu-id="a7dd6-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7dd6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7dd6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dd6-130">CommonParameters</span></span>
<span data-ttu-id="a7dd6-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7dd6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dd6-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7dd6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dd6-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7dd6-133">INPUTS</span></span>

## <span data-ttu-id="a7dd6-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7dd6-134">OUTPUTS</span></span>

### <span data-ttu-id="a7dd6-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a7dd6-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="a7dd6-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7dd6-136">NOTES</span></span>

<span data-ttu-id="a7dd6-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a7dd6-137">ALIASES</span></span>

## <span data-ttu-id="a7dd6-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7dd6-138">RELATED LINKS</span></span>

