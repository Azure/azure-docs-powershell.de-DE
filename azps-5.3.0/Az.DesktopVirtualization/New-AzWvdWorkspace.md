---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469923"
---
# <span data-ttu-id="7e4c1-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e4c1-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="7e4c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4c1-103">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7e4c1-103">Create or update a workspace.</span></span>

## <span data-ttu-id="7e4c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e4c1-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e4c1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e4c1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4c1-106">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7e4c1-106">Create or update a workspace.</span></span>

## <span data-ttu-id="7e4c1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e4c1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4c1-108">Beispiel 1: Erstellen eines virtuellen Desktoparbeitsbereichs für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="7e4c1-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="7e4c1-109">Dieser Befehl erstellt einen virtuellen Windows-Desktoparbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="7e4c1-110">Beispiel 2: Erstellen eines virtuellen Desktoparbeitsbereichs für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="7e4c1-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="7e4c1-111">Dieser Befehl erstellt einen virtuellen Windows-Desktoparbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="7e4c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e4c1-112">PARAMETERS</span></span>

### <span data-ttu-id="7e4c1-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="7e4c1-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="7e4c1-114">Liste der ApplicationGroup-Ressourcen-IDs.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="7e4c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c1-115">-DefaultProfile</span></span>
<span data-ttu-id="7e4c1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e4c1-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e4c1-117">-Description</span></span>
<span data-ttu-id="7e4c1-118">Beschreibung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4c1-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7e4c1-119">-FriendlyName</span></span>
<span data-ttu-id="7e4c1-120">Anzeigename des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4c1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="7e4c1-121">-Location</span></span>
<span data-ttu-id="7e4c1-122">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="7e4c1-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="7e4c1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7e4c1-123">-Name</span></span>
<span data-ttu-id="7e4c1-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7e4c1-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e4c1-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-126">The name of the resource group.</span></span>
<span data-ttu-id="7e4c1-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7e4c1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e4c1-128">-SubscriptionId</span></span>
<span data-ttu-id="7e4c1-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7e4c1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e4c1-130">-Tag</span></span>
<span data-ttu-id="7e4c1-131">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4c1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e4c1-132">-Confirm</span></span>
<span data-ttu-id="7e4c1-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4c1-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7e4c1-134">-WhatIf</span></span>
<span data-ttu-id="7e4c1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4c1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4c1-137">CommonParameters</span></span>
<span data-ttu-id="7e4c1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e4c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4c1-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e4c1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4c1-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e4c1-140">INPUTS</span></span>

## <span data-ttu-id="7e4c1-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e4c1-141">OUTPUTS</span></span>

### <span data-ttu-id="7e4c1-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e4c1-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="7e4c1-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7e4c1-143">NOTES</span></span>

<span data-ttu-id="7e4c1-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7e4c1-144">ALIASES</span></span>

## <span data-ttu-id="7e4c1-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7e4c1-145">RELATED LINKS</span></span>

