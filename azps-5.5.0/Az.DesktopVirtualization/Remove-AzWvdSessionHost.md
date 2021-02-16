---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147993"
---
# <span data-ttu-id="25fb1-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="25fb1-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="25fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="25fb1-103">Entfernen Sie einen SessionHost.</span><span class="sxs-lookup"><span data-stu-id="25fb1-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="25fb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25fb1-104">SYNTAX</span></span>

### <span data-ttu-id="25fb1-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="25fb1-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="25fb1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25fb1-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25fb1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25fb1-107">DESCRIPTION</span></span>
<span data-ttu-id="25fb1-108">Entfernen Sie einen SessionHost.</span><span class="sxs-lookup"><span data-stu-id="25fb1-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="25fb1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25fb1-109">EXAMPLES</span></span>

### <span data-ttu-id="25fb1-110">Beispiel 1: Löschen eines virtuellen Windows-Desktop-SessionHosts nach Name</span><span class="sxs-lookup"><span data-stu-id="25fb1-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="25fb1-111">Mit diesem Befehl wird sessionHost für den virtuellen Windows-Desktop in einem Hostpool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="25fb1-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="25fb1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25fb1-112">PARAMETERS</span></span>

### <span data-ttu-id="25fb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fb1-113">-DefaultProfile</span></span>
<span data-ttu-id="25fb1-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25fb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25fb1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="25fb1-115">-Force</span></span>
<span data-ttu-id="25fb1-116">Erzwingen Sie das Kennzeichen, um das Löschen von "sessionHost" auch dann zu erzwingen, wenn "userSession" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="25fb1-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="25fb1-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="25fb1-117">-HostPoolName</span></span>
<span data-ttu-id="25fb1-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="25fb1-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="25fb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25fb1-119">-InputObject</span></span>
<span data-ttu-id="25fb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="25fb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25fb1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="25fb1-121">-Name</span></span>
<span data-ttu-id="25fb1-122">Der Name des Sitzungshosts innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="25fb1-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25fb1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25fb1-123">-PassThru</span></span>
<span data-ttu-id="25fb1-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="25fb1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25fb1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25fb1-125">-ResourceGroupName</span></span>
<span data-ttu-id="25fb1-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25fb1-126">The name of the resource group.</span></span>
<span data-ttu-id="25fb1-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="25fb1-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="25fb1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25fb1-128">-SubscriptionId</span></span>
<span data-ttu-id="25fb1-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="25fb1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="25fb1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25fb1-130">-Confirm</span></span>
<span data-ttu-id="25fb1-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25fb1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25fb1-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25fb1-132">-WhatIf</span></span>
<span data-ttu-id="25fb1-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25fb1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25fb1-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25fb1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25fb1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fb1-135">CommonParameters</span></span>
<span data-ttu-id="25fb1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fb1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fb1-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25fb1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fb1-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25fb1-138">INPUTS</span></span>

### <span data-ttu-id="25fb1-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="25fb1-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="25fb1-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25fb1-140">OUTPUTS</span></span>

### <span data-ttu-id="25fb1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25fb1-141">System.Boolean</span></span>

## <span data-ttu-id="25fb1-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25fb1-142">NOTES</span></span>

<span data-ttu-id="25fb1-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="25fb1-143">ALIASES</span></span>

<span data-ttu-id="25fb1-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="25fb1-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25fb1-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25fb1-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25fb1-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25fb1-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25fb1-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="25fb1-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25fb1-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="25fb1-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="25fb1-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="25fb1-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="25fb1-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="25fb1-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="25fb1-151">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="25fb1-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="25fb1-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="25fb1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25fb1-153">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="25fb1-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="25fb1-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25fb1-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="25fb1-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="25fb1-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="25fb1-156">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="25fb1-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="25fb1-157">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="25fb1-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="25fb1-158">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="25fb1-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="25fb1-159">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="25fb1-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="25fb1-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25fb1-160">RELATED LINKS</span></span>

