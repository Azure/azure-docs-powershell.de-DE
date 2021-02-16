---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163673"
---
# <span data-ttu-id="a9da8-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a9da8-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="a9da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9da8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9da8-103">Erstellen oder aktualisieren Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-103">Create or update an application.</span></span>

## <span data-ttu-id="a9da8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9da8-104">SYNTAX</span></span>

### <span data-ttu-id="a9da8-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9da8-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9da8-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="a9da8-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9da8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9da8-107">DESCRIPTION</span></span>
<span data-ttu-id="a9da8-108">Erstellen oder aktualisieren Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-108">Create or update an application.</span></span>

## <span data-ttu-id="a9da8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9da8-109">EXAMPLES</span></span>

### <span data-ttu-id="a9da8-110">Beispiel 1: Erstellen einer virtuellen Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="a9da8-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="a9da8-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer Anwendungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9da8-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a9da8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9da8-112">PARAMETERS</span></span>

### <span data-ttu-id="a9da8-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="a9da8-113">-AppAlias</span></span>
<span data-ttu-id="a9da8-114">"App-Alias" im Startmenüelement</span><span class="sxs-lookup"><span data-stu-id="a9da8-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="a9da8-115">-ApplicationType</span></span>
<span data-ttu-id="a9da8-116">Ressourcentyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="a9da8-117">-CommandLineArgument</span></span>
<span data-ttu-id="a9da8-118">Befehlszeilenargumente für Die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="a9da8-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="a9da8-119">-CommandLineSetting</span></span>
<span data-ttu-id="a9da8-120">Gibt an, ob diese veröffentlichte Anwendung mit Vom Client bereitgestellten Befehlszeilenargumenten, Befehlszeilenargumenten, die zum Zeitpunkt der Veröffentlichung angegeben werden, oder überhaupt nicht mit Befehlszeilenargumenten gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9da8-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9da8-121">-DefaultProfile</span></span>
<span data-ttu-id="a9da8-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9da8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9da8-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9da8-123">-Description</span></span>
<span data-ttu-id="a9da8-124">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-124">Description of Application.</span></span>

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

### <span data-ttu-id="a9da8-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a9da8-125">-FilePath</span></span>
<span data-ttu-id="a9da8-126">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="a9da8-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="a9da8-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9da8-127">-FriendlyName</span></span>
<span data-ttu-id="a9da8-128">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a9da8-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="a9da8-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a9da8-129">-GroupName</span></span>
<span data-ttu-id="a9da8-130">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9da8-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="a9da8-131">-IconIndex</span></span>
<span data-ttu-id="a9da8-132">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="a9da8-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="a9da8-133">-IconPath</span></span>
<span data-ttu-id="a9da8-134">Symbol "Pfad zu".</span><span class="sxs-lookup"><span data-stu-id="a9da8-134">Path to icon.</span></span>

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

### <span data-ttu-id="a9da8-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9da8-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="a9da8-136">Gibt die Paketanwendungs-ID für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="a9da8-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="a9da8-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="a9da8-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="a9da8-138">Gibt den Paketfamiliennamen für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="a9da8-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="a9da8-139">-Name</span><span class="sxs-lookup"><span data-stu-id="a9da8-139">-Name</span></span>
<span data-ttu-id="a9da8-140">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9da8-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9da8-141">-ResourceGroupName</span></span>
<span data-ttu-id="a9da8-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a9da8-142">The name of the resource group.</span></span>
<span data-ttu-id="a9da8-143">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a9da8-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9da8-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="a9da8-144">-ShowInPortal</span></span>
<span data-ttu-id="a9da8-145">Gibt an, ob das Programm "RemoteApp" auf dem RD Web Access Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9da8-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="a9da8-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9da8-146">-SubscriptionId</span></span>
<span data-ttu-id="a9da8-147">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a9da8-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9da8-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9da8-148">-Confirm</span></span>
<span data-ttu-id="a9da8-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9da8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9da8-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a9da8-150">-WhatIf</span></span>
<span data-ttu-id="a9da8-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9da8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9da8-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9da8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9da8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9da8-153">CommonParameters</span></span>
<span data-ttu-id="a9da8-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9da8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9da8-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9da8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9da8-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9da8-156">INPUTS</span></span>

## <span data-ttu-id="a9da8-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9da8-157">OUTPUTS</span></span>

### <span data-ttu-id="a9da8-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="a9da8-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="a9da8-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9da8-159">NOTES</span></span>

<span data-ttu-id="a9da8-160">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a9da8-160">ALIASES</span></span>

## <span data-ttu-id="a9da8-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9da8-161">RELATED LINKS</span></span>

