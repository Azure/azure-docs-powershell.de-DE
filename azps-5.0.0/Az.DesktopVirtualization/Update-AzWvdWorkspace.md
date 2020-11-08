---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175776"
---
# <span data-ttu-id="17d2a-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="17d2a-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="17d2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="17d2a-103">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-103">Update a workspace.</span></span>

## <span data-ttu-id="17d2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d2a-104">SYNTAX</span></span>

### <span data-ttu-id="17d2a-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="17d2a-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17d2a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="17d2a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17d2a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d2a-107">DESCRIPTION</span></span>
<span data-ttu-id="17d2a-108">Aktualisieren eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-108">Update a workspace.</span></span>

## <span data-ttu-id="17d2a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17d2a-109">EXAMPLES</span></span>

### <span data-ttu-id="17d2a-110">Beispiel 1: Aktualisieren eines Windows Virtual Desktop-Worksapce nach Name</span><span class="sxs-lookup"><span data-stu-id="17d2a-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="17d2a-111">Dieser Befehl aktualisiert einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17d2a-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="17d2a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="17d2a-112">PARAMETERS</span></span>

### <span data-ttu-id="17d2a-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="17d2a-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="17d2a-114">Liste der Anwendungs Gruppenlinks</span><span class="sxs-lookup"><span data-stu-id="17d2a-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="17d2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d2a-115">-DefaultProfile</span></span>
<span data-ttu-id="17d2a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17d2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17d2a-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17d2a-117">-Description</span></span>
<span data-ttu-id="17d2a-118">Beschreibung des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="17d2a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="17d2a-119">-FriendlyName</span></span>
<span data-ttu-id="17d2a-120">Anzeigename des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="17d2a-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17d2a-121">-InputObject</span></span>
<span data-ttu-id="17d2a-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="17d2a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17d2a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="17d2a-123">-Name</span></span>
<span data-ttu-id="17d2a-124">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-124">The name of the workspace</span></span>

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

### <span data-ttu-id="17d2a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d2a-125">-ResourceGroupName</span></span>
<span data-ttu-id="17d2a-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17d2a-126">The name of the resource group.</span></span>
<span data-ttu-id="17d2a-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="17d2a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="17d2a-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="17d2a-128">-SubscriptionId</span></span>
<span data-ttu-id="17d2a-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="17d2a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="17d2a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="17d2a-130">-Tag</span></span>
<span data-ttu-id="17d2a-131">Tags, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="17d2a-131">tags to be updated</span></span>

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

### <span data-ttu-id="17d2a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17d2a-132">-Confirm</span></span>
<span data-ttu-id="17d2a-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17d2a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17d2a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d2a-134">-WhatIf</span></span>
<span data-ttu-id="17d2a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17d2a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d2a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17d2a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17d2a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d2a-137">CommonParameters</span></span>
<span data-ttu-id="17d2a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17d2a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d2a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17d2a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d2a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17d2a-140">INPUTS</span></span>

### <span data-ttu-id="17d2a-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="17d2a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="17d2a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17d2a-142">OUTPUTS</span></span>

### <span data-ttu-id="17d2a-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="17d2a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="17d2a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="17d2a-144">NOTES</span></span>

<span data-ttu-id="17d2a-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="17d2a-145">ALIASES</span></span>

<span data-ttu-id="17d2a-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17d2a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17d2a-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17d2a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17d2a-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="17d2a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17d2a-149">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="17d2a-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17d2a-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="17d2a-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="17d2a-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="17d2a-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="17d2a-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="17d2a-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="17d2a-153">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="17d2a-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="17d2a-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="17d2a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17d2a-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17d2a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="17d2a-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="17d2a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="17d2a-157">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="17d2a-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="17d2a-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="17d2a-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="17d2a-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="17d2a-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="17d2a-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="17d2a-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="17d2a-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17d2a-161">RELATED LINKS</span></span>

