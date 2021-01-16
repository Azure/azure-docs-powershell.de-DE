---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467887"
---
# <span data-ttu-id="7a055-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="7a055-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="7a055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a055-102">SYNOPSIS</span></span>
<span data-ttu-id="7a055-103">Entfernen Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="7a055-103">Remove a host pool.</span></span>

## <span data-ttu-id="7a055-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a055-104">SYNTAX</span></span>

### <span data-ttu-id="7a055-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a055-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a055-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a055-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a055-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a055-107">DESCRIPTION</span></span>
<span data-ttu-id="7a055-108">Entfernen Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="7a055-108">Remove a host pool.</span></span>

## <span data-ttu-id="7a055-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a055-109">EXAMPLES</span></span>

### <span data-ttu-id="7a055-110">Beispiel 1: Löschen eines Virtuellen Desktophostpools für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="7a055-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="7a055-111">Mit diesem Befehl wird ein Windows Virtual Desktop HostPool in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a055-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="7a055-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a055-112">PARAMETERS</span></span>

### <span data-ttu-id="7a055-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a055-113">-DefaultProfile</span></span>
<span data-ttu-id="7a055-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a055-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a055-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a055-115">-Force</span></span>
<span data-ttu-id="7a055-116">Erzwingen Sie das Löschen von "sessionHost".</span><span class="sxs-lookup"><span data-stu-id="7a055-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="7a055-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a055-117">-InputObject</span></span>
<span data-ttu-id="7a055-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7a055-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a055-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7a055-119">-Name</span></span>
<span data-ttu-id="7a055-120">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7a055-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a055-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a055-121">-PassThru</span></span>
<span data-ttu-id="7a055-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a055-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7a055-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a055-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a055-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a055-124">The name of the resource group.</span></span>
<span data-ttu-id="7a055-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a055-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7a055-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a055-126">-SubscriptionId</span></span>
<span data-ttu-id="7a055-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7a055-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7a055-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a055-128">-Confirm</span></span>
<span data-ttu-id="7a055-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a055-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a055-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a055-130">-WhatIf</span></span>
<span data-ttu-id="7a055-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a055-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a055-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a055-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a055-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a055-133">CommonParameters</span></span>
<span data-ttu-id="7a055-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a055-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a055-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a055-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a055-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a055-136">INPUTS</span></span>

### <span data-ttu-id="7a055-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7a055-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7a055-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a055-138">OUTPUTS</span></span>

### <span data-ttu-id="7a055-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a055-139">System.Boolean</span></span>

## <span data-ttu-id="7a055-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a055-140">NOTES</span></span>

<span data-ttu-id="7a055-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7a055-141">ALIASES</span></span>

<span data-ttu-id="7a055-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7a055-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a055-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a055-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a055-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a055-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a055-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7a055-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a055-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7a055-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7a055-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7a055-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7a055-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="7a055-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7a055-149">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7a055-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7a055-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7a055-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a055-151">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="7a055-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="7a055-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a055-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7a055-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a055-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="7a055-154">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="7a055-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7a055-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7a055-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7a055-156">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="7a055-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7a055-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7a055-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7a055-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a055-158">RELATED LINKS</span></span>

