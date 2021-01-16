---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: bd266bf6fe8a4239a1e2f10a5b462afd0fcc3577
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298523"
---
# <span data-ttu-id="80e8e-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="80e8e-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="80e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="80e8e-103">Entfernen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="80e8e-103">Remove a workspace.</span></span>

## <span data-ttu-id="80e8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80e8e-104">SYNTAX</span></span>

### <span data-ttu-id="80e8e-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="80e8e-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80e8e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80e8e-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80e8e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="80e8e-108">Entfernen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="80e8e-108">Remove a workspace.</span></span>

## <span data-ttu-id="80e8e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80e8e-109">EXAMPLES</span></span>

### <span data-ttu-id="80e8e-110">Beispiel 1: Löschen eines virtuellen Windows-Desktoparbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="80e8e-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="80e8e-111">Mit diesem Befehl wird ein virtueller Windows-Desktoparbeitsbereich in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="80e8e-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="80e8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80e8e-112">PARAMETERS</span></span>

### <span data-ttu-id="80e8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e8e-113">-DefaultProfile</span></span>
<span data-ttu-id="80e8e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80e8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80e8e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80e8e-115">-InputObject</span></span>
<span data-ttu-id="80e8e-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="80e8e-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80e8e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="80e8e-117">-Name</span></span>
<span data-ttu-id="80e8e-118">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="80e8e-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e8e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80e8e-119">-PassThru</span></span>
<span data-ttu-id="80e8e-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="80e8e-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80e8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="80e8e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80e8e-122">The name of the resource group.</span></span>
<span data-ttu-id="80e8e-123">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="80e8e-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e8e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80e8e-124">-SubscriptionId</span></span>
<span data-ttu-id="80e8e-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="80e8e-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e8e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80e8e-126">-Confirm</span></span>
<span data-ttu-id="80e8e-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80e8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e8e-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80e8e-128">-WhatIf</span></span>
<span data-ttu-id="80e8e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80e8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e8e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80e8e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80e8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e8e-131">CommonParameters</span></span>
<span data-ttu-id="80e8e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e8e-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80e8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e8e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80e8e-134">INPUTS</span></span>

### <span data-ttu-id="80e8e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="80e8e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="80e8e-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80e8e-136">OUTPUTS</span></span>

### <span data-ttu-id="80e8e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80e8e-137">System.Boolean</span></span>

## <span data-ttu-id="80e8e-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80e8e-138">NOTES</span></span>

<span data-ttu-id="80e8e-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="80e8e-139">ALIASES</span></span>

<span data-ttu-id="80e8e-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="80e8e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80e8e-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80e8e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80e8e-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80e8e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80e8e-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="80e8e-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80e8e-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="80e8e-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="80e8e-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="80e8e-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="80e8e-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="80e8e-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="80e8e-147">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="80e8e-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="80e8e-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="80e8e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80e8e-149">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="80e8e-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="80e8e-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80e8e-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80e8e-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="80e8e-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="80e8e-152">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="80e8e-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="80e8e-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="80e8e-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80e8e-154">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="80e8e-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="80e8e-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="80e8e-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="80e8e-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80e8e-156">RELATED LINKS</span></span>

