---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387203"
---
# <span data-ttu-id="dbe96-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="dbe96-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="dbe96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe96-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe96-103">Aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="dbe96-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="dbe96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbe96-104">SYNTAX</span></span>

### <span data-ttu-id="dbe96-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbe96-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dbe96-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dbe96-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dbe96-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbe96-107">DESCRIPTION</span></span>
<span data-ttu-id="dbe96-108">Aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="dbe96-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="dbe96-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbe96-109">EXAMPLES</span></span>

### <span data-ttu-id="dbe96-110">Beispiel 1: Aktualisieren eines MSIX-Pakets</span><span class="sxs-lookup"><span data-stu-id="dbe96-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="dbe96-111">Mit diesem Befehl wird ein "MSIX Package" in einem HostPool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dbe96-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="dbe96-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbe96-112">PARAMETERS</span></span>

### <span data-ttu-id="dbe96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe96-113">-DefaultProfile</span></span>
<span data-ttu-id="dbe96-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe96-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbe96-115">-DisplayName</span></span>
<span data-ttu-id="dbe96-116">Anzeigename für MSIX Package.</span><span class="sxs-lookup"><span data-stu-id="dbe96-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="dbe96-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="dbe96-117">-FullName</span></span>
<span data-ttu-id="dbe96-118">Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="dbe96-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe96-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="dbe96-119">-HostPoolName</span></span>
<span data-ttu-id="dbe96-120">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dbe96-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="dbe96-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbe96-121">-InputObject</span></span>
<span data-ttu-id="dbe96-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dbe96-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dbe96-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="dbe96-123">-IsActive</span></span>
<span data-ttu-id="dbe96-124">Legen Sie eine Version des Pakets so ein, dass sie hostpoolübergreifend aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="dbe96-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="dbe96-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="dbe96-125">-IsRegularRegistration</span></span>
<span data-ttu-id="dbe96-126">Legen Sie den Registrierungsmodus ein.</span><span class="sxs-lookup"><span data-stu-id="dbe96-126">Set Registration mode.</span></span>
<span data-ttu-id="dbe96-127">Normal oder verzögert.</span><span class="sxs-lookup"><span data-stu-id="dbe96-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="dbe96-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe96-128">-ResourceGroupName</span></span>
<span data-ttu-id="dbe96-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbe96-129">The name of the resource group.</span></span>
<span data-ttu-id="dbe96-130">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dbe96-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dbe96-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbe96-131">-SubscriptionId</span></span>
<span data-ttu-id="dbe96-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dbe96-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dbe96-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbe96-133">-Confirm</span></span>
<span data-ttu-id="dbe96-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbe96-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe96-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dbe96-135">-WhatIf</span></span>
<span data-ttu-id="dbe96-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbe96-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe96-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbe96-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe96-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe96-138">CommonParameters</span></span>
<span data-ttu-id="dbe96-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe96-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe96-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbe96-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe96-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbe96-141">INPUTS</span></span>

### <span data-ttu-id="dbe96-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dbe96-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dbe96-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbe96-143">OUTPUTS</span></span>

### <span data-ttu-id="dbe96-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="dbe96-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="dbe96-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbe96-145">NOTES</span></span>

<span data-ttu-id="dbe96-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dbe96-146">ALIASES</span></span>

<span data-ttu-id="dbe96-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dbe96-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbe96-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbe96-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbe96-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dbe96-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbe96-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dbe96-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbe96-151">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="dbe96-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dbe96-152">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="dbe96-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dbe96-153">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="dbe96-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dbe96-154">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dbe96-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dbe96-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dbe96-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbe96-156">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="dbe96-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dbe96-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbe96-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dbe96-158">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dbe96-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="dbe96-159">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="dbe96-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dbe96-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dbe96-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dbe96-161">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="dbe96-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dbe96-162">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="dbe96-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dbe96-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbe96-163">RELATED LINKS</span></span>

