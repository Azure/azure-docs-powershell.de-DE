---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: b47e87ef781138dabe5b2327227ee17f29e5a494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292264"
---
# <span data-ttu-id="3d5d8-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3d5d8-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="3d5d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5d8-103">Aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="3d5d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d5d8-104">SYNTAX</span></span>

### <span data-ttu-id="3d5d8-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d5d8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d5d8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3d5d8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d5d8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d5d8-107">DESCRIPTION</span></span>
<span data-ttu-id="3d5d8-108">Aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="3d5d8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d5d8-109">EXAMPLES</span></span>

### <span data-ttu-id="3d5d8-110">Beispiel 1: Aktualisieren eines MSIX-Pakets</span><span class="sxs-lookup"><span data-stu-id="3d5d8-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="3d5d8-111">Mit diesem Befehl wird ein "MSIX Package" in einem HostPool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="3d5d8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d5d8-112">PARAMETERS</span></span>

### <span data-ttu-id="3d5d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5d8-113">-DefaultProfile</span></span>
<span data-ttu-id="3d5d8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d5d8-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3d5d8-115">-DisplayName</span></span>
<span data-ttu-id="3d5d8-116">Anzeigename für MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="3d5d8-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="3d5d8-117">-FullName</span></span>
<span data-ttu-id="3d5d8-118">Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="3d5d8-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="3d5d8-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3d5d8-119">-HostPoolName</span></span>
<span data-ttu-id="3d5d8-120">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3d5d8-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3d5d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d5d8-121">-InputObject</span></span>
<span data-ttu-id="3d5d8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d5d8-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="3d5d8-123">-IsActive</span></span>
<span data-ttu-id="3d5d8-124">Legen Sie eine Version des Pakets so ein, dass sie hostpoolübergreifend aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="3d5d8-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="3d5d8-125">-IsRegularRegistration</span></span>
<span data-ttu-id="3d5d8-126">Legen Sie den Registrierungsmodus ein.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-126">Set Registration mode.</span></span>
<span data-ttu-id="3d5d8-127">Normal oder verzögert.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="3d5d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="3d5d8-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-129">The name of the resource group.</span></span>
<span data-ttu-id="3d5d8-130">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3d5d8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d5d8-131">-SubscriptionId</span></span>
<span data-ttu-id="3d5d8-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3d5d8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d5d8-133">-Confirm</span></span>
<span data-ttu-id="3d5d8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d5d8-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3d5d8-135">-WhatIf</span></span>
<span data-ttu-id="3d5d8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d5d8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d5d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5d8-138">CommonParameters</span></span>
<span data-ttu-id="3d5d8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5d8-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d5d8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5d8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d5d8-141">INPUTS</span></span>

### <span data-ttu-id="3d5d8-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3d5d8-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3d5d8-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d5d8-143">OUTPUTS</span></span>

### <span data-ttu-id="3d5d8-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3d5d8-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="3d5d8-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d5d8-145">NOTES</span></span>

<span data-ttu-id="3d5d8-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3d5d8-146">ALIASES</span></span>

<span data-ttu-id="3d5d8-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3d5d8-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d5d8-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d5d8-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d5d8-150">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3d5d8-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d5d8-151">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3d5d8-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3d5d8-152">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3d5d8-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3d5d8-153">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="3d5d8-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3d5d8-154">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3d5d8-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3d5d8-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3d5d8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d5d8-156">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="3d5d8-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3d5d8-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3d5d8-158">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="3d5d8-159">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="3d5d8-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3d5d8-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3d5d8-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3d5d8-161">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="3d5d8-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3d5d8-162">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3d5d8-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3d5d8-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d5d8-163">RELATED LINKS</span></span>

