---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: 239d1a5a38d2eb344f584e006d465598b43dd546
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298515"
---
# <span data-ttu-id="f305b-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f305b-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f305b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f305b-102">SYNOPSIS</span></span>
<span data-ttu-id="f305b-103">Aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="f305b-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="f305b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f305b-104">SYNTAX</span></span>

### <span data-ttu-id="f305b-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f305b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f305b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f305b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f305b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f305b-107">DESCRIPTION</span></span>
<span data-ttu-id="f305b-108">Aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="f305b-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="f305b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f305b-109">EXAMPLES</span></span>

### <span data-ttu-id="f305b-110">Beispiel 1: Erstellen einer Virtuellen Desktopanwendungsgruppe für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="f305b-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f305b-111">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f305b-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="f305b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f305b-112">PARAMETERS</span></span>

### <span data-ttu-id="f305b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f305b-113">-DefaultProfile</span></span>
<span data-ttu-id="f305b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f305b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f305b-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f305b-115">-Description</span></span>
<span data-ttu-id="f305b-116">Beschreibung der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="f305b-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="f305b-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f305b-117">-FriendlyName</span></span>
<span data-ttu-id="f305b-118">Anzeigename der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="f305b-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="f305b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f305b-119">-InputObject</span></span>
<span data-ttu-id="f305b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f305b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f305b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f305b-121">-Name</span></span>
<span data-ttu-id="f305b-122">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f305b-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f305b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f305b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f305b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f305b-124">The name of the resource group.</span></span>
<span data-ttu-id="f305b-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f305b-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f305b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f305b-126">-SubscriptionId</span></span>
<span data-ttu-id="f305b-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f305b-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f305b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="f305b-128">-Tag</span></span>
<span data-ttu-id="f305b-129">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="f305b-129">tags to be updated</span></span>

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

### <span data-ttu-id="f305b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f305b-130">-Confirm</span></span>
<span data-ttu-id="f305b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f305b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f305b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f305b-132">-WhatIf</span></span>
<span data-ttu-id="f305b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f305b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f305b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f305b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f305b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f305b-135">CommonParameters</span></span>
<span data-ttu-id="f305b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f305b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f305b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f305b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f305b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f305b-138">INPUTS</span></span>

### <span data-ttu-id="f305b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f305b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f305b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f305b-140">OUTPUTS</span></span>

### <span data-ttu-id="f305b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f305b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="f305b-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f305b-142">NOTES</span></span>

<span data-ttu-id="f305b-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f305b-143">ALIASES</span></span>

<span data-ttu-id="f305b-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f305b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f305b-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f305b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f305b-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f305b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f305b-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f305b-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f305b-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f305b-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f305b-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f305b-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f305b-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="f305b-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f305b-151">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f305b-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f305b-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f305b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f305b-153">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="f305b-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f305b-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f305b-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f305b-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f305b-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="f305b-156">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="f305b-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f305b-157">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f305b-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f305b-158">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="f305b-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f305b-159">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f305b-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f305b-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f305b-160">RELATED LINKS</span></span>

