---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302482"
---
# <span data-ttu-id="dfc09-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="dfc09-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="dfc09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfc09-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc09-103">Löscht eine Verschiebungs Ressource aus der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dfc09-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="dfc09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc09-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfc09-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc09-106">Löscht eine Verschiebungs Ressource aus der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dfc09-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="dfc09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfc09-107">EXAMPLES</span></span>

### <span data-ttu-id="dfc09-108">Beispiel 1: Entfernen der Ressource aus der Move-Sammlung</span><span class="sxs-lookup"><span data-stu-id="dfc09-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="dfc09-109">Entfernen Sie die Ressource aus der Move-Sammlung innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="dfc09-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="dfc09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfc09-110">PARAMETERS</span></span>

### <span data-ttu-id="dfc09-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfc09-111">-AsJob</span></span>
<span data-ttu-id="dfc09-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dfc09-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dfc09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc09-113">-DefaultProfile</span></span>
<span data-ttu-id="dfc09-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfc09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc09-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="dfc09-115">-MoveCollectionName</span></span>
<span data-ttu-id="dfc09-116">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="dfc09-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="dfc09-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dfc09-117">-Name</span></span>
<span data-ttu-id="dfc09-118">Der Name der Verschiebungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="dfc09-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="dfc09-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dfc09-119">-NoWait</span></span>
<span data-ttu-id="dfc09-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dfc09-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfc09-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfc09-121">-PassThru</span></span>
<span data-ttu-id="dfc09-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="dfc09-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dfc09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc09-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfc09-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfc09-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="dfc09-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dfc09-125">-SubscriptionId</span></span>
<span data-ttu-id="dfc09-126">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="dfc09-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="dfc09-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfc09-127">-Confirm</span></span>
<span data-ttu-id="dfc09-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfc09-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc09-129">-WhatIf</span></span>
<span data-ttu-id="dfc09-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc09-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfc09-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfc09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc09-132">CommonParameters</span></span>
<span data-ttu-id="dfc09-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc09-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfc09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc09-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfc09-135">INPUTS</span></span>

## <span data-ttu-id="dfc09-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfc09-136">OUTPUTS</span></span>

### <span data-ttu-id="dfc09-137">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="dfc09-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="dfc09-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfc09-138">NOTES</span></span>

<span data-ttu-id="dfc09-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="dfc09-139">ALIASES</span></span>

## <span data-ttu-id="dfc09-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfc09-140">RELATED LINKS</span></span>

