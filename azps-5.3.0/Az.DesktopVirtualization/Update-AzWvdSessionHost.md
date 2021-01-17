---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ddc8dee2e553701fc8f7660fe72b4070ff9eafa1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469895"
---
# <span data-ttu-id="096af-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="096af-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="096af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096af-102">SYNOPSIS</span></span>
<span data-ttu-id="096af-103">Aktualisieren sie einen Sitzungshost.</span><span class="sxs-lookup"><span data-stu-id="096af-103">Update a session host.</span></span>

## <span data-ttu-id="096af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="096af-104">SYNTAX</span></span>

### <span data-ttu-id="096af-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="096af-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="096af-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="096af-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="096af-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="096af-107">DESCRIPTION</span></span>
<span data-ttu-id="096af-108">Aktualisieren sie einen Sitzungshost.</span><span class="sxs-lookup"><span data-stu-id="096af-108">Update a session host.</span></span>

## <span data-ttu-id="096af-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="096af-109">EXAMPLES</span></span>

### <span data-ttu-id="096af-110">Beispiel 1: Aktualisieren eines virtuellen Windows-Desktop-SessionHosts nach Name</span><span class="sxs-lookup"><span data-stu-id="096af-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="096af-111">Mit diesem Befehl wird sessionHost für den virtuellen Windows-Desktop in einem Hostpool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="096af-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="096af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="096af-112">PARAMETERS</span></span>

### <span data-ttu-id="096af-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="096af-113">-AllowNewSession</span></span>
<span data-ttu-id="096af-114">Eine neue Sitzung zulassen.</span><span class="sxs-lookup"><span data-stu-id="096af-114">Allow a new session.</span></span>

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

### <span data-ttu-id="096af-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="096af-115">-AssignedUser</span></span>
<span data-ttu-id="096af-116">Benutzer, der SessionHost zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="096af-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="096af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096af-117">-DefaultProfile</span></span>
<span data-ttu-id="096af-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="096af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="096af-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="096af-119">-HostPoolName</span></span>
<span data-ttu-id="096af-120">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="096af-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="096af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="096af-121">-InputObject</span></span>
<span data-ttu-id="096af-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="096af-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="096af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="096af-123">-Name</span></span>
<span data-ttu-id="096af-124">Der Name des Sitzungshosts innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="096af-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="096af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096af-125">-ResourceGroupName</span></span>
<span data-ttu-id="096af-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="096af-126">The name of the resource group.</span></span>
<span data-ttu-id="096af-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="096af-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="096af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="096af-128">-SubscriptionId</span></span>
<span data-ttu-id="096af-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="096af-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="096af-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="096af-130">-Confirm</span></span>
<span data-ttu-id="096af-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="096af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096af-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="096af-132">-WhatIf</span></span>
<span data-ttu-id="096af-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="096af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="096af-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="096af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096af-135">CommonParameters</span></span>
<span data-ttu-id="096af-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096af-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="096af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096af-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="096af-138">INPUTS</span></span>

### <span data-ttu-id="096af-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="096af-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="096af-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="096af-140">OUTPUTS</span></span>

### <span data-ttu-id="096af-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="096af-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="096af-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="096af-142">NOTES</span></span>

<span data-ttu-id="096af-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="096af-143">ALIASES</span></span>

<span data-ttu-id="096af-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="096af-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="096af-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="096af-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="096af-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="096af-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="096af-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="096af-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="096af-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="096af-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="096af-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="096af-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="096af-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="096af-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="096af-151">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="096af-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="096af-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="096af-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="096af-153">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="096af-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="096af-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="096af-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="096af-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="096af-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="096af-156">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="096af-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="096af-157">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="096af-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="096af-158">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="096af-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="096af-159">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="096af-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="096af-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="096af-160">RELATED LINKS</span></span>

