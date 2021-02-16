---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153273"
---
# <span data-ttu-id="2efac-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="2efac-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="2efac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2efac-102">SYNOPSIS</span></span>
<span data-ttu-id="2efac-103">Entfernen Sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="2efac-103">Remove a userSession.</span></span>

## <span data-ttu-id="2efac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2efac-104">SYNTAX</span></span>

### <span data-ttu-id="2efac-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2efac-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2efac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2efac-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2efac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2efac-107">DESCRIPTION</span></span>
<span data-ttu-id="2efac-108">Entfernen Sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="2efac-108">Remove a userSession.</span></span>

## <span data-ttu-id="2efac-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2efac-109">EXAMPLES</span></span>

### <span data-ttu-id="2efac-110">Beispiel 1: Löschen einer Windows Virtual Desktop UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="2efac-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="2efac-111">Mit diesem Befehl wird eine Windows Virtual Desktop UserSession in einem Sitzungshost gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2efac-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="2efac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2efac-112">PARAMETERS</span></span>

### <span data-ttu-id="2efac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efac-113">-DefaultProfile</span></span>
<span data-ttu-id="2efac-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2efac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2efac-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2efac-115">-Force</span></span>
<span data-ttu-id="2efac-116">Erzwingen Sie das Kennzeichen zum Abmelden von userSession.</span><span class="sxs-lookup"><span data-stu-id="2efac-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="2efac-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2efac-117">-HostPoolName</span></span>
<span data-ttu-id="2efac-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2efac-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="2efac-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2efac-119">-Id</span></span>
<span data-ttu-id="2efac-120">Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="2efac-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2efac-121">-InputObject</span></span>
<span data-ttu-id="2efac-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2efac-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2efac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2efac-123">-PassThru</span></span>
<span data-ttu-id="2efac-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2efac-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2efac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efac-125">-ResourceGroupName</span></span>
<span data-ttu-id="2efac-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2efac-126">The name of the resource group.</span></span>
<span data-ttu-id="2efac-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2efac-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2efac-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="2efac-128">-SessionHostName</span></span>
<span data-ttu-id="2efac-129">Der Name des Sitzungshosts innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="2efac-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="2efac-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2efac-130">-SubscriptionId</span></span>
<span data-ttu-id="2efac-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2efac-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2efac-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2efac-132">-Confirm</span></span>
<span data-ttu-id="2efac-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2efac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efac-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2efac-134">-WhatIf</span></span>
<span data-ttu-id="2efac-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2efac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2efac-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2efac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2efac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efac-137">CommonParameters</span></span>
<span data-ttu-id="2efac-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efac-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2efac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efac-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2efac-140">INPUTS</span></span>

### <span data-ttu-id="2efac-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2efac-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2efac-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2efac-142">OUTPUTS</span></span>

### <span data-ttu-id="2efac-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2efac-143">System.Boolean</span></span>

## <span data-ttu-id="2efac-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2efac-144">NOTES</span></span>

<span data-ttu-id="2efac-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2efac-145">ALIASES</span></span>

<span data-ttu-id="2efac-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2efac-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2efac-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2efac-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2efac-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2efac-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2efac-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2efac-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2efac-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2efac-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2efac-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2efac-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2efac-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="2efac-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2efac-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2efac-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2efac-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2efac-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2efac-155">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="2efac-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2efac-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2efac-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2efac-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2efac-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2efac-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="2efac-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2efac-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2efac-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2efac-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="2efac-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2efac-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2efac-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2efac-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2efac-162">RELATED LINKS</span></span>

