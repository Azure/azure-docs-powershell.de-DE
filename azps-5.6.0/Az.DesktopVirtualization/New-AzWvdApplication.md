---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: af0073a94401ce8c260027fcf905fd763d89326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932883"
---
# <span data-ttu-id="072f9-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="072f9-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="072f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="072f9-102">SYNOPSIS</span></span>
<span data-ttu-id="072f9-103">Erstellen oder Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="072f9-103">Create or update an application.</span></span>

## <span data-ttu-id="072f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="072f9-104">SYNTAX</span></span>

### <span data-ttu-id="072f9-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="072f9-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="072f9-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="072f9-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="072f9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="072f9-107">DESCRIPTION</span></span>
<span data-ttu-id="072f9-108">Erstellen oder Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="072f9-108">Create or update an application.</span></span>

## <span data-ttu-id="072f9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="072f9-109">EXAMPLES</span></span>

### <span data-ttu-id="072f9-110">Beispiel 1: Erstellen einer virtuellen Windows-Desktopanwendung</span><span class="sxs-lookup"><span data-stu-id="072f9-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="072f9-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer applicaton-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="072f9-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="072f9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="072f9-112">PARAMETERS</span></span>

### <span data-ttu-id="072f9-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="072f9-113">-AppAlias</span></span>
<span data-ttu-id="072f9-114">App-Alias vom Startmenüelement</span><span class="sxs-lookup"><span data-stu-id="072f9-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="072f9-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="072f9-115">-ApplicationType</span></span>
<span data-ttu-id="072f9-116">Ressourcentyp der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="072f9-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="072f9-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="072f9-117">-CommandLineArgument</span></span>
<span data-ttu-id="072f9-118">Befehlszeilenargumente für Anwendung.</span><span class="sxs-lookup"><span data-stu-id="072f9-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="072f9-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="072f9-119">-CommandLineSetting</span></span>
<span data-ttu-id="072f9-120">Gibt an, ob diese veröffentlichte Anwendung mit Befehlszeilenargumenten gestartet werden kann, die vom Client bereitgestellt werden, Befehlszeilenargumente, die zum Zeitpunkt der Veröffentlichung angegeben wurden, oder gar keine Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="072f9-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="072f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072f9-121">-DefaultProfile</span></span>
<span data-ttu-id="072f9-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="072f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="072f9-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="072f9-123">-Description</span></span>
<span data-ttu-id="072f9-124">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="072f9-124">Description of Application.</span></span>

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

### <span data-ttu-id="072f9-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="072f9-125">-FilePath</span></span>
<span data-ttu-id="072f9-126">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="072f9-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="072f9-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="072f9-127">-FriendlyName</span></span>
<span data-ttu-id="072f9-128">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="072f9-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="072f9-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="072f9-129">-GroupName</span></span>
<span data-ttu-id="072f9-130">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="072f9-130">The name of the application group</span></span>

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

### <span data-ttu-id="072f9-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="072f9-131">-IconIndex</span></span>
<span data-ttu-id="072f9-132">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="072f9-132">Index of the icon.</span></span>

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

### <span data-ttu-id="072f9-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="072f9-133">-IconPath</span></span>
<span data-ttu-id="072f9-134">Pfad zum Symbol.</span><span class="sxs-lookup"><span data-stu-id="072f9-134">Path to icon.</span></span>

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

### <span data-ttu-id="072f9-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="072f9-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="072f9-136">Gibt die Paketanwendungs-ID für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="072f9-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="072f9-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="072f9-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="072f9-138">Gibt den Paketfamiliennamen für MSIX-Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="072f9-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="072f9-139">-Name</span><span class="sxs-lookup"><span data-stu-id="072f9-139">-Name</span></span>
<span data-ttu-id="072f9-140">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="072f9-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="072f9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072f9-141">-ResourceGroupName</span></span>
<span data-ttu-id="072f9-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="072f9-142">The name of the resource group.</span></span>
<span data-ttu-id="072f9-143">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="072f9-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="072f9-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="072f9-144">-ShowInPortal</span></span>
<span data-ttu-id="072f9-145">Gibt an, ob das RemoteApp-Programm auf dem RD Web Access-Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="072f9-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="072f9-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="072f9-146">-SubscriptionId</span></span>
<span data-ttu-id="072f9-147">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="072f9-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="072f9-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="072f9-148">-Confirm</span></span>
<span data-ttu-id="072f9-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="072f9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072f9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072f9-150">-WhatIf</span></span>
<span data-ttu-id="072f9-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="072f9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="072f9-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="072f9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072f9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072f9-153">CommonParameters</span></span>
<span data-ttu-id="072f9-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="072f9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072f9-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="072f9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072f9-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="072f9-156">INPUTS</span></span>

## <span data-ttu-id="072f9-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="072f9-157">OUTPUTS</span></span>

### <span data-ttu-id="072f9-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="072f9-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="072f9-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="072f9-159">NOTES</span></span>

<span data-ttu-id="072f9-160">ALIASE</span><span class="sxs-lookup"><span data-stu-id="072f9-160">ALIASES</span></span>

## <span data-ttu-id="072f9-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="072f9-161">RELATED LINKS</span></span>

