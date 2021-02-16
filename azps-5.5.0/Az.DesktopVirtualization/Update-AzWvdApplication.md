---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175681"
---
# <span data-ttu-id="b33a8-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="b33a8-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="b33a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b33a8-103">Aktualisieren sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-103">Update an application.</span></span>

## <span data-ttu-id="b33a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b33a8-104">SYNTAX</span></span>

### <span data-ttu-id="b33a8-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b33a8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b33a8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b33a8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b33a8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b33a8-107">DESCRIPTION</span></span>
<span data-ttu-id="b33a8-108">Aktualisieren sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-108">Update an application.</span></span>

## <span data-ttu-id="b33a8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b33a8-109">EXAMPLES</span></span>

### <span data-ttu-id="b33a8-110">Beispiel 1: Aktualisieren einer virtuellen Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="b33a8-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="b33a8-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer Anwendungsgruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b33a8-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="b33a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b33a8-112">PARAMETERS</span></span>

### <span data-ttu-id="b33a8-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="b33a8-113">-ApplicationType</span></span>
<span data-ttu-id="b33a8-114">Ressourcentyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a8-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="b33a8-115">-CommandLineArgument</span></span>
<span data-ttu-id="b33a8-116">Befehlszeilenargumente für Die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="b33a8-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="b33a8-117">-CommandLineSetting</span></span>
<span data-ttu-id="b33a8-118">Gibt an, ob diese veröffentlichte Anwendung mit Vom Client bereitgestellten Befehlszeilenargumenten, Befehlszeilenargumenten, die zum Zeitpunkt der Veröffentlichung angegeben werden, oder überhaupt nicht mit Befehlszeilenargumenten gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b33a8-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33a8-119">-DefaultProfile</span></span>
<span data-ttu-id="b33a8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b33a8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33a8-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b33a8-121">-Description</span></span>
<span data-ttu-id="b33a8-122">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-122">Description of Application.</span></span>

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

### <span data-ttu-id="b33a8-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b33a8-123">-FilePath</span></span>
<span data-ttu-id="b33a8-124">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b33a8-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="b33a8-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b33a8-125">-FriendlyName</span></span>
<span data-ttu-id="b33a8-126">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b33a8-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="b33a8-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="b33a8-127">-GroupName</span></span>
<span data-ttu-id="b33a8-128">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-128">The name of the application group</span></span>

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

### <span data-ttu-id="b33a8-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="b33a8-129">-IconIndex</span></span>
<span data-ttu-id="b33a8-130">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="b33a8-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a8-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="b33a8-131">-IconPath</span></span>
<span data-ttu-id="b33a8-132">Symbol "Pfad zu".</span><span class="sxs-lookup"><span data-stu-id="b33a8-132">Path to icon.</span></span>

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

### <span data-ttu-id="b33a8-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b33a8-133">-InputObject</span></span>
<span data-ttu-id="b33a8-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b33a8-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b33a8-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="b33a8-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="b33a8-136">Gibt die Paketanwendungs-ID für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="b33a8-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="b33a8-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="b33a8-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="b33a8-138">Gibt den Paketfamiliennamen für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="b33a8-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="b33a8-139">-Name</span><span class="sxs-lookup"><span data-stu-id="b33a8-139">-Name</span></span>
<span data-ttu-id="b33a8-140">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33a8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33a8-141">-ResourceGroupName</span></span>
<span data-ttu-id="b33a8-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b33a8-142">The name of the resource group.</span></span>
<span data-ttu-id="b33a8-143">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="b33a8-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b33a8-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="b33a8-144">-ShowInPortal</span></span>
<span data-ttu-id="b33a8-145">Gibt an, ob das Programm "RemoteApp" auf dem RD Web Access Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b33a8-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="b33a8-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b33a8-146">-SubscriptionId</span></span>
<span data-ttu-id="b33a8-147">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b33a8-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b33a8-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b33a8-148">-Tag</span></span>
<span data-ttu-id="b33a8-149">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="b33a8-149">tags to be updated</span></span>

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

### <span data-ttu-id="b33a8-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b33a8-150">-Confirm</span></span>
<span data-ttu-id="b33a8-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b33a8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33a8-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b33a8-152">-WhatIf</span></span>
<span data-ttu-id="b33a8-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b33a8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33a8-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b33a8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33a8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33a8-155">CommonParameters</span></span>
<span data-ttu-id="b33a8-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b33a8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33a8-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b33a8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33a8-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b33a8-158">INPUTS</span></span>

### <span data-ttu-id="b33a8-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b33a8-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b33a8-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b33a8-160">OUTPUTS</span></span>

### <span data-ttu-id="b33a8-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="b33a8-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="b33a8-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b33a8-162">NOTES</span></span>

<span data-ttu-id="b33a8-163">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b33a8-163">ALIASES</span></span>

<span data-ttu-id="b33a8-164">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b33a8-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b33a8-165">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b33a8-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b33a8-166">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b33a8-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b33a8-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b33a8-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b33a8-168">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b33a8-169">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b33a8-170">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b33a8-171">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b33a8-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b33a8-172">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b33a8-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b33a8-173">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="b33a8-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b33a8-174">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b33a8-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b33a8-175">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="b33a8-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="b33a8-176">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="b33a8-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b33a8-177">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b33a8-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b33a8-178">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="b33a8-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b33a8-179">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="b33a8-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b33a8-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b33a8-180">RELATED LINKS</span></span>

