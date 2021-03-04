---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 1da28d0003de88d9e8c10da1692ca4f61079f488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947432"
---
# <span data-ttu-id="cf4af-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf4af-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="cf4af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf4af-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4af-103">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cf4af-103">Update a workspace.</span></span>

## <span data-ttu-id="cf4af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf4af-104">SYNTAX</span></span>

### <span data-ttu-id="cf4af-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf4af-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf4af-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cf4af-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf4af-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf4af-107">DESCRIPTION</span></span>
<span data-ttu-id="cf4af-108">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cf4af-108">Update a workspace.</span></span>

## <span data-ttu-id="cf4af-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf4af-109">EXAMPLES</span></span>

### <span data-ttu-id="cf4af-110">Beispiel 1: Aktualisieren eines virtuellen Windows-Desktoparbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="cf4af-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="cf4af-111">Mit diesem Befehl wird ein virtueller Windows-Desktoparbeitsbereich in einer Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf4af-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="cf4af-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf4af-112">PARAMETERS</span></span>

### <span data-ttu-id="cf4af-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="cf4af-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="cf4af-114">Liste der ApplicationGroup-Links.</span><span class="sxs-lookup"><span data-stu-id="cf4af-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="cf4af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4af-115">-DefaultProfile</span></span>
<span data-ttu-id="cf4af-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf4af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf4af-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf4af-117">-Description</span></span>
<span data-ttu-id="cf4af-118">Beschreibung des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="cf4af-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="cf4af-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf4af-119">-FriendlyName</span></span>
<span data-ttu-id="cf4af-120">Anzeigename des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="cf4af-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="cf4af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf4af-121">-InputObject</span></span>
<span data-ttu-id="cf4af-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cf4af-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf4af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cf4af-123">-Name</span></span>
<span data-ttu-id="cf4af-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cf4af-124">The name of the workspace</span></span>

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

### <span data-ttu-id="cf4af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4af-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf4af-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf4af-126">The name of the resource group.</span></span>
<span data-ttu-id="cf4af-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cf4af-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cf4af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf4af-128">-SubscriptionId</span></span>
<span data-ttu-id="cf4af-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cf4af-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cf4af-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf4af-130">-Tag</span></span>
<span data-ttu-id="cf4af-131">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="cf4af-131">tags to be updated</span></span>

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

### <span data-ttu-id="cf4af-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf4af-132">-Confirm</span></span>
<span data-ttu-id="cf4af-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf4af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf4af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf4af-134">-WhatIf</span></span>
<span data-ttu-id="cf4af-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf4af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf4af-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf4af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf4af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4af-137">CommonParameters</span></span>
<span data-ttu-id="cf4af-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf4af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4af-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf4af-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4af-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf4af-140">INPUTS</span></span>

### <span data-ttu-id="cf4af-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4af-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cf4af-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf4af-142">OUTPUTS</span></span>

### <span data-ttu-id="cf4af-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf4af-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="cf4af-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cf4af-144">NOTES</span></span>

<span data-ttu-id="cf4af-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cf4af-145">ALIASES</span></span>

<span data-ttu-id="cf4af-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cf4af-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf4af-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cf4af-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf4af-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf4af-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf4af-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="cf4af-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf4af-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf4af-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cf4af-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf4af-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cf4af-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="cf4af-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cf4af-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cf4af-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cf4af-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cf4af-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf4af-155">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="cf4af-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cf4af-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf4af-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cf4af-157">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cf4af-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="cf4af-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="cf4af-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cf4af-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cf4af-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cf4af-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="cf4af-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cf4af-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="cf4af-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cf4af-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cf4af-162">RELATED LINKS</span></span>

