---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8770b9e3b07b677f0f4bd4f59a6c38928421523e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944194"
---
# <span data-ttu-id="9cbfb-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="9cbfb-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="9cbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbfb-103">Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="9cbfb-103">Update an application.</span></span>

## <span data-ttu-id="9cbfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cbfb-104">SYNTAX</span></span>

### <span data-ttu-id="9cbfb-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9cbfb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9cbfb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cbfb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cbfb-107">DESCRIPTION</span></span>
<span data-ttu-id="9cbfb-108">Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="9cbfb-108">Update an application.</span></span>

## <span data-ttu-id="9cbfb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9cbfb-109">EXAMPLES</span></span>

### <span data-ttu-id="9cbfb-110">Beispiel 1: Aktualisieren einer virtuellen Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="9cbfb-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="9cbfb-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer applicaton-Gruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="9cbfb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9cbfb-112">PARAMETERS</span></span>

### <span data-ttu-id="9cbfb-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="9cbfb-113">-ApplicationType</span></span>
<span data-ttu-id="9cbfb-114">Ressourcentyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="9cbfb-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="9cbfb-115">-CommandLineArgument</span></span>
<span data-ttu-id="9cbfb-116">Befehlszeilenargumente für Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="9cbfb-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="9cbfb-117">-CommandLineSetting</span></span>
<span data-ttu-id="9cbfb-118">Gibt an, ob diese veröffentlichte Anwendung mit Befehlszeilenargumenten gestartet werden kann, die vom Client bereitgestellt werden, Befehlszeilenargumente, die zum Zeitpunkt der Veröffentlichung angegeben wurden, oder gar keine Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="9cbfb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbfb-119">-DefaultProfile</span></span>
<span data-ttu-id="9cbfb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbfb-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cbfb-121">-Description</span></span>
<span data-ttu-id="9cbfb-122">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-122">Description of Application.</span></span>

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

### <span data-ttu-id="9cbfb-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9cbfb-123">-FilePath</span></span>
<span data-ttu-id="9cbfb-124">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="9cbfb-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9cbfb-125">-FriendlyName</span></span>
<span data-ttu-id="9cbfb-126">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="9cbfb-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9cbfb-127">-GroupName</span></span>
<span data-ttu-id="9cbfb-128">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-128">The name of the application group</span></span>

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

### <span data-ttu-id="9cbfb-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="9cbfb-129">-IconIndex</span></span>
<span data-ttu-id="9cbfb-130">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-130">Index of the icon.</span></span>

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

### <span data-ttu-id="9cbfb-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="9cbfb-131">-IconPath</span></span>
<span data-ttu-id="9cbfb-132">Pfad zum Symbol.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-132">Path to icon.</span></span>

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

### <span data-ttu-id="9cbfb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cbfb-133">-InputObject</span></span>
<span data-ttu-id="9cbfb-134">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cbfb-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="9cbfb-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="9cbfb-136">Gibt die Paketanwendungs-ID für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="9cbfb-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="9cbfb-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="9cbfb-138">Gibt den Paketfamiliennamen für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="9cbfb-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9cbfb-139">-Name</span></span>
<span data-ttu-id="9cbfb-140">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="9cbfb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbfb-141">-ResourceGroupName</span></span>
<span data-ttu-id="9cbfb-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-142">The name of the resource group.</span></span>
<span data-ttu-id="9cbfb-143">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9cbfb-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="9cbfb-144">-ShowInPortal</span></span>
<span data-ttu-id="9cbfb-145">Gibt an, ob das RemoteApp-Programm auf dem RD Web Access-Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="9cbfb-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cbfb-146">-SubscriptionId</span></span>
<span data-ttu-id="9cbfb-147">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9cbfb-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cbfb-148">-Tag</span></span>
<span data-ttu-id="9cbfb-149">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="9cbfb-149">tags to be updated</span></span>

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

### <span data-ttu-id="9cbfb-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cbfb-150">-Confirm</span></span>
<span data-ttu-id="9cbfb-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbfb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbfb-152">-WhatIf</span></span>
<span data-ttu-id="9cbfb-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cbfb-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbfb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbfb-155">CommonParameters</span></span>
<span data-ttu-id="9cbfb-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbfb-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbfb-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9cbfb-158">INPUTS</span></span>

### <span data-ttu-id="9cbfb-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9cbfb-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9cbfb-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9cbfb-160">OUTPUTS</span></span>

### <span data-ttu-id="9cbfb-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="9cbfb-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="9cbfb-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9cbfb-162">NOTES</span></span>

<span data-ttu-id="9cbfb-163">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9cbfb-163">ALIASES</span></span>

<span data-ttu-id="9cbfb-164">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9cbfb-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cbfb-165">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cbfb-166">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cbfb-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="9cbfb-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cbfb-168">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9cbfb-169">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9cbfb-170">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9cbfb-171">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9cbfb-172">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9cbfb-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cbfb-173">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="9cbfb-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="9cbfb-174">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9cbfb-175">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="9cbfb-176">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="9cbfb-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9cbfb-177">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9cbfb-178">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="9cbfb-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9cbfb-179">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9cbfb-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9cbfb-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9cbfb-180">RELATED LINKS</span></span>

