---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469931"
---
# <span data-ttu-id="5073d-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5073d-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="5073d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5073d-102">SYNOPSIS</span></span>
<span data-ttu-id="5073d-103">Erstellen oder aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5073d-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="5073d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5073d-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5073d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5073d-105">DESCRIPTION</span></span>
<span data-ttu-id="5073d-106">Erstellen oder aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5073d-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="5073d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5073d-107">EXAMPLES</span></span>

### <span data-ttu-id="5073d-108">Beispiel 1: Erstellen einer Virtuellen Desktopanwendungsgruppe für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="5073d-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="5073d-109">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5073d-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="5073d-110">Beispiel 2: Erstellen einer Virtuellen Desktopanwendungsgruppe für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="5073d-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="5073d-111">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5073d-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="5073d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5073d-112">PARAMETERS</span></span>

### <span data-ttu-id="5073d-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="5073d-113">-ApplicationGroupType</span></span>
<span data-ttu-id="5073d-114">Ressourcentyp der Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5073d-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5073d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5073d-115">-DefaultProfile</span></span>
<span data-ttu-id="5073d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5073d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5073d-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5073d-117">-Description</span></span>
<span data-ttu-id="5073d-118">Beschreibung der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5073d-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5073d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5073d-119">-FriendlyName</span></span>
<span data-ttu-id="5073d-120">Anzeigename der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5073d-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5073d-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="5073d-121">-HostPoolArmPath</span></span>
<span data-ttu-id="5073d-122">HostPool arm path of ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5073d-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5073d-123">-Location</span><span class="sxs-lookup"><span data-stu-id="5073d-123">-Location</span></span>
<span data-ttu-id="5073d-124">Der geo-Standort, in dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="5073d-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="5073d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5073d-125">-Name</span></span>
<span data-ttu-id="5073d-126">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5073d-126">The name of the application group</span></span>

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

### <span data-ttu-id="5073d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5073d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5073d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5073d-128">The name of the resource group.</span></span>
<span data-ttu-id="5073d-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5073d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5073d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5073d-130">-SubscriptionId</span></span>
<span data-ttu-id="5073d-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5073d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5073d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="5073d-132">-Tag</span></span>
<span data-ttu-id="5073d-133">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="5073d-133">Resource tags.</span></span>

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

### <span data-ttu-id="5073d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5073d-134">-Confirm</span></span>
<span data-ttu-id="5073d-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5073d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5073d-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5073d-136">-WhatIf</span></span>
<span data-ttu-id="5073d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5073d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5073d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5073d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5073d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5073d-139">CommonParameters</span></span>
<span data-ttu-id="5073d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5073d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5073d-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5073d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5073d-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5073d-142">INPUTS</span></span>

## <span data-ttu-id="5073d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5073d-143">OUTPUTS</span></span>

### <span data-ttu-id="5073d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5073d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="5073d-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5073d-145">NOTES</span></span>

<span data-ttu-id="5073d-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5073d-146">ALIASES</span></span>

## <span data-ttu-id="5073d-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5073d-147">RELATED LINKS</span></span>

