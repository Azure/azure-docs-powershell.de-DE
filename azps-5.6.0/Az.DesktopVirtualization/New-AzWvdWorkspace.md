---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: 9335bb4c3177fa405d65038255f43dbba5fb88fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925656"
---
# <span data-ttu-id="1ba14-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ba14-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="1ba14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba14-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba14-103">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1ba14-103">Create or update a workspace.</span></span>

## <span data-ttu-id="1ba14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba14-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ba14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ba14-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba14-106">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1ba14-106">Create or update a workspace.</span></span>

## <span data-ttu-id="1ba14-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ba14-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba14-108">Beispiel 1: Erstellen eines virtuellen Windows-Desktoparbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="1ba14-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="1ba14-109">Mit diesem Befehl wird ein virtueller Windows-Desktoparbeitsbereich in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ba14-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="1ba14-110">Beispiel 2: Erstellen eines virtuellen Windows-Desktoparbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="1ba14-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="1ba14-111">Mit diesem Befehl wird ein virtueller Windows-Desktoparbeitsbereich in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ba14-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="1ba14-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ba14-112">PARAMETERS</span></span>

### <span data-ttu-id="1ba14-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="1ba14-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="1ba14-114">Liste der applicationGroup-Ressourcen-Ids.</span><span class="sxs-lookup"><span data-stu-id="1ba14-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="1ba14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba14-115">-DefaultProfile</span></span>
<span data-ttu-id="1ba14-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ba14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba14-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ba14-117">-Description</span></span>
<span data-ttu-id="1ba14-118">Beschreibung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1ba14-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="1ba14-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1ba14-119">-FriendlyName</span></span>
<span data-ttu-id="1ba14-120">Anzeigename des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1ba14-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="1ba14-121">-Location</span><span class="sxs-lookup"><span data-stu-id="1ba14-121">-Location</span></span>
<span data-ttu-id="1ba14-122">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="1ba14-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="1ba14-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ba14-123">-Name</span></span>
<span data-ttu-id="1ba14-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1ba14-124">The name of the workspace</span></span>

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

### <span data-ttu-id="1ba14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba14-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ba14-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ba14-126">The name of the resource group.</span></span>
<span data-ttu-id="1ba14-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1ba14-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1ba14-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ba14-128">-SubscriptionId</span></span>
<span data-ttu-id="1ba14-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1ba14-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ba14-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ba14-130">-Tag</span></span>
<span data-ttu-id="1ba14-131">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="1ba14-131">Resource tags.</span></span>

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

### <span data-ttu-id="1ba14-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ba14-132">-Confirm</span></span>
<span data-ttu-id="1ba14-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ba14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba14-134">-WhatIf</span></span>
<span data-ttu-id="1ba14-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ba14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba14-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ba14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba14-137">CommonParameters</span></span>
<span data-ttu-id="1ba14-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba14-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ba14-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba14-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba14-140">INPUTS</span></span>

## <span data-ttu-id="1ba14-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba14-141">OUTPUTS</span></span>

### <span data-ttu-id="1ba14-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ba14-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="1ba14-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ba14-143">NOTES</span></span>

<span data-ttu-id="1ba14-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1ba14-144">ALIASES</span></span>

## <span data-ttu-id="1ba14-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ba14-145">RELATED LINKS</span></span>

