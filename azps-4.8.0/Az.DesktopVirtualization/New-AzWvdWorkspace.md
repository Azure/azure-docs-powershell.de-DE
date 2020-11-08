---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175218"
---
# <span data-ttu-id="a8c48-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8c48-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="a8c48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8c48-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c48-103">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a8c48-103">Create or update a workspace.</span></span>

## <span data-ttu-id="a8c48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8c48-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8c48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8c48-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c48-106">Erstellen oder Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a8c48-106">Create or update a workspace.</span></span>

## <span data-ttu-id="a8c48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8c48-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c48-108">Beispiel 1: Erstellen einer virtuellen Windows-Desktop-Worksapce nach Namen</span><span class="sxs-lookup"><span data-stu-id="a8c48-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="a8c48-109">Dieser Befehl erstellt einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8c48-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="a8c48-110">Beispiel 2: Erstellen eines virtuellen Windows-Desktop-Worksapce nach Name</span><span class="sxs-lookup"><span data-stu-id="a8c48-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="a8c48-111">Dieser Befehl erstellt einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8c48-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="a8c48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8c48-112">PARAMETERS</span></span>

### <span data-ttu-id="a8c48-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="a8c48-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="a8c48-114">Liste der Ressourcen-IDs der Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="a8c48-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="a8c48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c48-115">-DefaultProfile</span></span>
<span data-ttu-id="a8c48-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8c48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8c48-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8c48-117">-Description</span></span>
<span data-ttu-id="a8c48-118">Beschreibung des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a8c48-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="a8c48-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8c48-119">-FriendlyName</span></span>
<span data-ttu-id="a8c48-120">Anzeigename des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a8c48-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="a8c48-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="a8c48-121">-Location</span></span>
<span data-ttu-id="a8c48-122">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="a8c48-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="a8c48-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a8c48-123">-Name</span></span>
<span data-ttu-id="a8c48-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a8c48-124">The name of the workspace</span></span>

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

### <span data-ttu-id="a8c48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c48-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8c48-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8c48-126">The name of the resource group.</span></span>
<span data-ttu-id="a8c48-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a8c48-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a8c48-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a8c48-128">-SubscriptionId</span></span>
<span data-ttu-id="a8c48-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a8c48-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a8c48-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8c48-130">-Tag</span></span>
<span data-ttu-id="a8c48-131">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="a8c48-131">Resource tags.</span></span>

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

### <span data-ttu-id="a8c48-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8c48-132">-Confirm</span></span>
<span data-ttu-id="a8c48-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8c48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8c48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c48-134">-WhatIf</span></span>
<span data-ttu-id="a8c48-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8c48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8c48-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8c48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8c48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c48-137">CommonParameters</span></span>
<span data-ttu-id="a8c48-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c48-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8c48-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c48-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8c48-140">INPUTS</span></span>

## <span data-ttu-id="a8c48-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8c48-141">OUTPUTS</span></span>

### <span data-ttu-id="a8c48-142">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8c48-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="a8c48-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8c48-143">NOTES</span></span>

<span data-ttu-id="a8c48-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="a8c48-144">ALIASES</span></span>

## <span data-ttu-id="a8c48-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8c48-145">RELATED LINKS</span></span>

