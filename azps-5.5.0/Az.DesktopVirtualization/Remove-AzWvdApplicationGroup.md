---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170741"
---
# <span data-ttu-id="c8544-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c8544-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c8544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8544-102">SYNOPSIS</span></span>
<span data-ttu-id="c8544-103">Entfernen Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c8544-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="c8544-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8544-104">SYNTAX</span></span>

### <span data-ttu-id="c8544-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8544-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8544-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8544-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8544-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8544-107">DESCRIPTION</span></span>
<span data-ttu-id="c8544-108">Entfernen Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="c8544-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="c8544-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8544-109">EXAMPLES</span></span>

### <span data-ttu-id="c8544-110">Beispiel 1: Löschen einer Windows Virtual Desktop ApplicationGroup nach Name</span><span class="sxs-lookup"><span data-stu-id="c8544-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="c8544-111">Mit diesem Befehl wird eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c8544-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="c8544-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8544-112">PARAMETERS</span></span>

### <span data-ttu-id="c8544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8544-113">-DefaultProfile</span></span>
<span data-ttu-id="c8544-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8544-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8544-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8544-115">-InputObject</span></span>
<span data-ttu-id="c8544-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c8544-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8544-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8544-117">-Name</span></span>
<span data-ttu-id="c8544-118">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c8544-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8544-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8544-119">-PassThru</span></span>
<span data-ttu-id="c8544-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8544-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8544-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8544-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8544-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8544-122">The name of the resource group.</span></span>
<span data-ttu-id="c8544-123">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c8544-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c8544-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8544-124">-SubscriptionId</span></span>
<span data-ttu-id="c8544-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c8544-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8544-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8544-126">-Confirm</span></span>
<span data-ttu-id="c8544-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8544-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8544-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c8544-128">-WhatIf</span></span>
<span data-ttu-id="c8544-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8544-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8544-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8544-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8544-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8544-131">CommonParameters</span></span>
<span data-ttu-id="c8544-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8544-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8544-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8544-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8544-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8544-134">INPUTS</span></span>

### <span data-ttu-id="c8544-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c8544-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c8544-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8544-136">OUTPUTS</span></span>

### <span data-ttu-id="c8544-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8544-137">System.Boolean</span></span>

## <span data-ttu-id="c8544-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8544-138">NOTES</span></span>

<span data-ttu-id="c8544-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c8544-139">ALIASES</span></span>

<span data-ttu-id="c8544-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c8544-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8544-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8544-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8544-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8544-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8544-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c8544-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8544-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c8544-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c8544-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c8544-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c8544-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="c8544-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c8544-147">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c8544-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c8544-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c8544-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8544-149">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="c8544-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c8544-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c8544-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c8544-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c8544-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="c8544-152">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="c8544-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c8544-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c8544-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c8544-154">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="c8544-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c8544-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c8544-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c8544-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8544-156">RELATED LINKS</span></span>

