---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302487"
---
# <span data-ttu-id="17574-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="17574-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="17574-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17574-102">SYNOPSIS</span></span>
<span data-ttu-id="17574-103">Löscht eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="17574-103">Deletes a move collection.</span></span>

## <span data-ttu-id="17574-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17574-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17574-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17574-105">DESCRIPTION</span></span>
<span data-ttu-id="17574-106">Löscht eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="17574-106">Deletes a move collection.</span></span>

## <span data-ttu-id="17574-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17574-107">EXAMPLES</span></span>

### <span data-ttu-id="17574-108">Beispiel 1: Entfernen der Move-Sammlung aus dem angegebenen Abonnement</span><span class="sxs-lookup"><span data-stu-id="17574-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="17574-109">Entfernen Sie die Move-Sammlung aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17574-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="17574-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="17574-110">PARAMETERS</span></span>

### <span data-ttu-id="17574-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17574-111">-AsJob</span></span>
<span data-ttu-id="17574-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="17574-112">Run the command as a job</span></span>

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

### <span data-ttu-id="17574-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17574-113">-DefaultProfile</span></span>
<span data-ttu-id="17574-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17574-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17574-115">-Name</span><span class="sxs-lookup"><span data-stu-id="17574-115">-Name</span></span>
<span data-ttu-id="17574-116">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="17574-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="17574-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="17574-117">-NoWait</span></span>
<span data-ttu-id="17574-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="17574-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="17574-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17574-119">-PassThru</span></span>
<span data-ttu-id="17574-120">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="17574-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="17574-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17574-121">-ResourceGroupName</span></span>
<span data-ttu-id="17574-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17574-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="17574-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="17574-123">-SubscriptionId</span></span>
<span data-ttu-id="17574-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="17574-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="17574-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17574-125">-Confirm</span></span>
<span data-ttu-id="17574-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17574-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17574-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17574-127">-WhatIf</span></span>
<span data-ttu-id="17574-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17574-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17574-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17574-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17574-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17574-130">CommonParameters</span></span>
<span data-ttu-id="17574-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17574-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17574-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17574-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17574-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17574-133">INPUTS</span></span>

## <span data-ttu-id="17574-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17574-134">OUTPUTS</span></span>

### <span data-ttu-id="17574-135">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="17574-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="17574-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="17574-136">NOTES</span></span>

<span data-ttu-id="17574-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="17574-137">ALIASES</span></span>

## <span data-ttu-id="17574-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17574-138">RELATED LINKS</span></span>

