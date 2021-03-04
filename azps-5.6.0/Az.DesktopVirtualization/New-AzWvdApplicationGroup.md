---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 38292351f091528ef4e153f9374dff75ccbfe941
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925691"
---
# <span data-ttu-id="c1525-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c1525-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c1525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1525-102">SYNOPSIS</span></span>
<span data-ttu-id="c1525-103">Erstellen oder Aktualisieren einer ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c1525-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="c1525-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1525-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1525-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1525-105">DESCRIPTION</span></span>
<span data-ttu-id="c1525-106">Erstellen oder Aktualisieren einer ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c1525-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="c1525-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1525-107">EXAMPLES</span></span>

### <span data-ttu-id="c1525-108">Beispiel 1: Erstellen einer Windows Virtual Desktop ApplicationGroup nach Name</span><span class="sxs-lookup"><span data-stu-id="c1525-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c1525-109">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1525-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="c1525-110">Beispiel 2: Erstellen einer Windows Virtual Desktop ApplicationGroup nach Name</span><span class="sxs-lookup"><span data-stu-id="c1525-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c1525-111">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1525-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="c1525-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1525-112">PARAMETERS</span></span>

### <span data-ttu-id="c1525-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="c1525-113">-ApplicationGroupType</span></span>
<span data-ttu-id="c1525-114">Ressourcentyp der Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c1525-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1525-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1525-115">-DefaultProfile</span></span>
<span data-ttu-id="c1525-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1525-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1525-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1525-117">-Description</span></span>
<span data-ttu-id="c1525-118">Beschreibung von ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c1525-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c1525-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c1525-119">-FriendlyName</span></span>
<span data-ttu-id="c1525-120">Anzeigename der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c1525-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c1525-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="c1525-121">-HostPoolArmPath</span></span>
<span data-ttu-id="c1525-122">HostPool-Armpfad der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c1525-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="c1525-123">-Location</span><span class="sxs-lookup"><span data-stu-id="c1525-123">-Location</span></span>
<span data-ttu-id="c1525-124">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="c1525-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="c1525-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1525-125">-Name</span></span>
<span data-ttu-id="c1525-126">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c1525-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1525-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1525-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1525-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1525-128">The name of the resource group.</span></span>
<span data-ttu-id="c1525-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="c1525-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c1525-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1525-130">-SubscriptionId</span></span>
<span data-ttu-id="c1525-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c1525-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c1525-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1525-132">-Tag</span></span>
<span data-ttu-id="c1525-133">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="c1525-133">Resource tags.</span></span>

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

### <span data-ttu-id="c1525-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1525-134">-Confirm</span></span>
<span data-ttu-id="c1525-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1525-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1525-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1525-136">-WhatIf</span></span>
<span data-ttu-id="c1525-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1525-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1525-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1525-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1525-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1525-139">CommonParameters</span></span>
<span data-ttu-id="c1525-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1525-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1525-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1525-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1525-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1525-142">INPUTS</span></span>

## <span data-ttu-id="c1525-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1525-143">OUTPUTS</span></span>

### <span data-ttu-id="c1525-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c1525-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="c1525-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1525-145">NOTES</span></span>

<span data-ttu-id="c1525-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c1525-146">ALIASES</span></span>

## <span data-ttu-id="c1525-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1525-147">RELATED LINKS</span></span>

