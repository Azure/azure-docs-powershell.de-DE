---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357620"
---
# <span data-ttu-id="7f382-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="7f382-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="7f382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f382-102">SYNOPSIS</span></span>
<span data-ttu-id="7f382-103">Erstellen oder aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="7f382-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="7f382-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f382-104">SYNTAX</span></span>

### <span data-ttu-id="7f382-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f382-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7f382-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="7f382-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7f382-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f382-107">DESCRIPTION</span></span>
<span data-ttu-id="7f382-108">Erstellen oder aktualisieren Sie ein MSIX-Paket.</span><span class="sxs-lookup"><span data-stu-id="7f382-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="7f382-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f382-109">EXAMPLES</span></span>

### <span data-ttu-id="7f382-110">Beispiel 1: Erstellt ein neues "MSIX"-Paket im HostPool über "Paketalias".</span><span class="sxs-lookup"><span data-stu-id="7f382-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="7f382-111">Dieser Befehl fügt hostpool das "MSIX"-Paket aus dem angegebenen Bildpfad hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f382-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="7f382-112">Beispiel 2: Erstellt ein neues "MSIX"-Paket im HostPool</span><span class="sxs-lookup"><span data-stu-id="7f382-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="7f382-113">Dieser Befehl fügt "MSIX Package" im angegebenen HostPool hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f382-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="7f382-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f382-114">PARAMETERS</span></span>

### <span data-ttu-id="7f382-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f382-115">-DefaultProfile</span></span>
<span data-ttu-id="7f382-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f382-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f382-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f382-117">-DisplayName</span></span>
<span data-ttu-id="7f382-118">Benutzerfreundlicher Name, der im Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7f382-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="7f382-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="7f382-119">-FullName</span></span>
<span data-ttu-id="7f382-120">Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="7f382-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="7f382-121">-HostPoolName</span></span>
<span data-ttu-id="7f382-122">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f382-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="7f382-123">-ImagePath</span></span>
<span data-ttu-id="7f382-124">VHD/CIM-Bildpfad auf der Netzwerkfreigabe.</span><span class="sxs-lookup"><span data-stu-id="7f382-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="7f382-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="7f382-125">-IsActive</span></span>
<span data-ttu-id="7f382-126">Machen Sie diese Version des Pakets über die Hostpool hinweg zum aktiven Paket.</span><span class="sxs-lookup"><span data-stu-id="7f382-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="7f382-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="7f382-127">-IsRegularRegistration</span></span>
<span data-ttu-id="7f382-128">Gibt an, wie "Paket" im Feed registriert wird.</span><span class="sxs-lookup"><span data-stu-id="7f382-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="7f382-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="7f382-129">-LastUpdated</span></span>
<span data-ttu-id="7f382-130">Date Package was last updated, found in the appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="7f382-131">-PackageAlias</span></span>
<span data-ttu-id="7f382-132">Paketalias aus "MSIX-Bild extrahieren"</span><span class="sxs-lookup"><span data-stu-id="7f382-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="7f382-133">-PackageApplication</span></span>
<span data-ttu-id="7f382-134">Liste der Paketanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7f382-134">List of package applications.</span></span>

<span data-ttu-id="7f382-135">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7f382-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="7f382-136">-PackageDependency</span></span>
<span data-ttu-id="7f382-137">Liste der Paketabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="7f382-137">List of package dependencies.</span></span>

<span data-ttu-id="7f382-138">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7f382-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="7f382-139">-PackageFamilyName</span></span>
<span data-ttu-id="7f382-140">Paketfamilienname von appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="7f382-141">Enthält den Paketnamen und den Herausgebernamen.</span><span class="sxs-lookup"><span data-stu-id="7f382-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="7f382-142">-PackageName</span></span>
<span data-ttu-id="7f382-143">Paketname aus appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="7f382-144">-PackageRelativePath</span></span>
<span data-ttu-id="7f382-145">Relativer Pfad zu dem Paket innerhalb des Bilds.</span><span class="sxs-lookup"><span data-stu-id="7f382-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f382-146">-ResourceGroupName</span></span>
<span data-ttu-id="7f382-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7f382-147">The name of the resource group.</span></span>
<span data-ttu-id="7f382-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7f382-148">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f382-149">-SubscriptionId</span></span>
<span data-ttu-id="7f382-150">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7f382-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-151">-Version</span><span class="sxs-lookup"><span data-stu-id="7f382-151">-Version</span></span>
<span data-ttu-id="7f382-152">Paketversion im appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f382-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f382-153">-Confirm</span></span>
<span data-ttu-id="7f382-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f382-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f382-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f382-155">-WhatIf</span></span>
<span data-ttu-id="7f382-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f382-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f382-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f382-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f382-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f382-158">CommonParameters</span></span>
<span data-ttu-id="7f382-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f382-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f382-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f382-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f382-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f382-161">INPUTS</span></span>

## <span data-ttu-id="7f382-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f382-162">OUTPUTS</span></span>

### <span data-ttu-id="7f382-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="7f382-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="7f382-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f382-164">NOTES</span></span>

<span data-ttu-id="7f382-165">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7f382-165">ALIASES</span></span>

<span data-ttu-id="7f382-166">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7f382-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f382-167">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f382-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f382-168">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f382-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f382-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: Liste der Paketanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7f382-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="7f382-170">`[AppId <String>]`: Paketanwendungs-ID, die in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="7f382-171">`[AppUserModelId <String>]`: Wird zum Aktivieren der Paketanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f382-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="7f382-172">Besteht aus "Paketname" und "ApplicationID".</span><span class="sxs-lookup"><span data-stu-id="7f382-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="7f382-173">Gefunden in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7f382-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="7f382-174">`[Description <String>]`: Beschreibung der Paketanwendung.</span><span class="sxs-lookup"><span data-stu-id="7f382-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="7f382-175">`[FriendlyName <String>]`: Benutzerfreundlicher Name.</span><span class="sxs-lookup"><span data-stu-id="7f382-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="7f382-176">`[IconImageName <String>]`: Benutzerfreundlicher Name.</span><span class="sxs-lookup"><span data-stu-id="7f382-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="7f382-177">`[RawIcon <Byte[]>]`: Das Symbol einer 64-Bit-Zeichenfolge als Bytearray.</span><span class="sxs-lookup"><span data-stu-id="7f382-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="7f382-178">`[RawPng <Byte[]>]`: Das Symbol einer 64-Bit-Zeichenfolge als Bytearray.</span><span class="sxs-lookup"><span data-stu-id="7f382-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="7f382-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span><span class="sxs-lookup"><span data-stu-id="7f382-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="7f382-180">`[DependencyName <String>]`: Name der Paketabhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="7f382-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="7f382-181">`[MinVersion <String>]`: Abhängigkeitsversion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f382-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="7f382-182">`[Publisher <String>]`: Name des Herausgebers der Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="7f382-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="7f382-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f382-183">RELATED LINKS</span></span>

