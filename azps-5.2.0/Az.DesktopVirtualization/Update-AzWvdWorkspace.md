---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 04e7c192659ec1f1aa71b0bf1b97e61030cd9b4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292258"
---
# <span data-ttu-id="2e323-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e323-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="2e323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e323-102">SYNOPSIS</span></span>
<span data-ttu-id="2e323-103">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2e323-103">Update a workspace.</span></span>

## <span data-ttu-id="2e323-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e323-104">SYNTAX</span></span>

### <span data-ttu-id="2e323-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e323-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2e323-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2e323-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e323-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e323-107">DESCRIPTION</span></span>
<span data-ttu-id="2e323-108">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2e323-108">Update a workspace.</span></span>

## <span data-ttu-id="2e323-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e323-109">EXAMPLES</span></span>

### <span data-ttu-id="2e323-110">Beispiel 1: Aktualisieren eines virtuellen Desktoparbeitsbereichs für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="2e323-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="2e323-111">Mit diesem Befehl wird ein virtueller Windows-Desktoparbeitsbereich in einer Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2e323-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="2e323-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e323-112">PARAMETERS</span></span>

### <span data-ttu-id="2e323-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="2e323-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="2e323-114">Liste der Anwendungsgruppenlinks.</span><span class="sxs-lookup"><span data-stu-id="2e323-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="2e323-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e323-115">-DefaultProfile</span></span>
<span data-ttu-id="2e323-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e323-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e323-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e323-117">-Description</span></span>
<span data-ttu-id="2e323-118">Beschreibung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2e323-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="2e323-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2e323-119">-FriendlyName</span></span>
<span data-ttu-id="2e323-120">Anzeigename des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2e323-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="2e323-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e323-121">-InputObject</span></span>
<span data-ttu-id="2e323-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2e323-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e323-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e323-123">-Name</span></span>
<span data-ttu-id="2e323-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2e323-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e323-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e323-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e323-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e323-126">The name of the resource group.</span></span>
<span data-ttu-id="2e323-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2e323-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e323-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e323-128">-SubscriptionId</span></span>
<span data-ttu-id="2e323-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2e323-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e323-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e323-130">-Tag</span></span>
<span data-ttu-id="2e323-131">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="2e323-131">tags to be updated</span></span>

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

### <span data-ttu-id="2e323-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e323-132">-Confirm</span></span>
<span data-ttu-id="2e323-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e323-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e323-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2e323-134">-WhatIf</span></span>
<span data-ttu-id="2e323-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e323-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e323-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e323-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e323-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e323-137">CommonParameters</span></span>
<span data-ttu-id="2e323-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e323-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e323-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e323-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e323-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e323-140">INPUTS</span></span>

### <span data-ttu-id="2e323-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2e323-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2e323-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e323-142">OUTPUTS</span></span>

### <span data-ttu-id="2e323-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e323-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="2e323-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2e323-144">NOTES</span></span>

<span data-ttu-id="2e323-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2e323-145">ALIASES</span></span>

<span data-ttu-id="2e323-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2e323-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e323-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e323-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e323-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e323-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e323-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2e323-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e323-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2e323-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2e323-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2e323-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2e323-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="2e323-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2e323-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2e323-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2e323-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2e323-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e323-155">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="2e323-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2e323-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e323-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e323-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2e323-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e323-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="2e323-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2e323-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2e323-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2e323-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="2e323-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2e323-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2e323-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2e323-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2e323-162">RELATED LINKS</span></span>

