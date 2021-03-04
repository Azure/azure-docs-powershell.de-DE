---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943534"
---
# <span data-ttu-id="386d3-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="386d3-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="386d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386d3-102">SYNOPSIS</span></span>
<span data-ttu-id="386d3-103">Löscht eine Ressource verschieben aus der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="386d3-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="386d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="386d3-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="386d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="386d3-105">DESCRIPTION</span></span>
<span data-ttu-id="386d3-106">Löscht eine Ressource verschieben aus der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="386d3-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="386d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="386d3-107">EXAMPLES</span></span>

### <span data-ttu-id="386d3-108">Beispiel 1: Entfernen sie eine Move Rresource aus der Move Collection.</span><span class="sxs-lookup"><span data-stu-id="386d3-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="386d3-109">Entfernen Sie eine Move Rresource aus der Move Collection.</span><span class="sxs-lookup"><span data-stu-id="386d3-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="386d3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="386d3-110">PARAMETERS</span></span>

### <span data-ttu-id="386d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="386d3-111">-AsJob</span></span>
<span data-ttu-id="386d3-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="386d3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="386d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386d3-113">-DefaultProfile</span></span>
<span data-ttu-id="386d3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="386d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="386d3-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="386d3-115">-MoveCollectionName</span></span>
<span data-ttu-id="386d3-116">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="386d3-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="386d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="386d3-117">-Name</span></span>
<span data-ttu-id="386d3-118">Der Name der Ressource verschieben.</span><span class="sxs-lookup"><span data-stu-id="386d3-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386d3-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="386d3-119">-NoWait</span></span>
<span data-ttu-id="386d3-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="386d3-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="386d3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="386d3-121">-PassThru</span></span>
<span data-ttu-id="386d3-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="386d3-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="386d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="386d3-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="386d3-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="386d3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="386d3-125">-SubscriptionId</span></span>
<span data-ttu-id="386d3-126">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="386d3-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="386d3-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="386d3-127">-Confirm</span></span>
<span data-ttu-id="386d3-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="386d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386d3-129">-WhatIf</span></span>
<span data-ttu-id="386d3-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="386d3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386d3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="386d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386d3-132">CommonParameters</span></span>
<span data-ttu-id="386d3-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386d3-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="386d3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386d3-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="386d3-135">INPUTS</span></span>

## <span data-ttu-id="386d3-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="386d3-136">OUTPUTS</span></span>

### <span data-ttu-id="386d3-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="386d3-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="386d3-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="386d3-138">NOTES</span></span>

<span data-ttu-id="386d3-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="386d3-139">ALIASES</span></span>

## <span data-ttu-id="386d3-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="386d3-140">RELATED LINKS</span></span>

