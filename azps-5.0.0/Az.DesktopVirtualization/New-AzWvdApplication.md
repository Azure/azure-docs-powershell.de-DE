---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297046"
---
# <span data-ttu-id="1d5d8-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="1d5d8-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="1d5d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5d8-103">Erstellen oder aktualisieren Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-103">Create or update an application.</span></span>

## <span data-ttu-id="1d5d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5d8-104">SYNTAX</span></span>

### <span data-ttu-id="1d5d8-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d5d8-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1d5d8-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="1d5d8-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1d5d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d5d8-107">DESCRIPTION</span></span>
<span data-ttu-id="1d5d8-108">Erstellen oder aktualisieren Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-108">Create or update an application.</span></span>

## <span data-ttu-id="1d5d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d5d8-109">EXAMPLES</span></span>

### <span data-ttu-id="1d5d8-110">Beispiel 1: Erstellen einer virtuellen Windows-Desktop Anwendung</span><span class="sxs-lookup"><span data-stu-id="1d5d8-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="1d5d8-111">Mit diesem Befehl wird eine Windows-virtuelle Desktop Anwendung in einer Applicaton-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="1d5d8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d5d8-112">PARAMETERS</span></span>

### <span data-ttu-id="1d5d8-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="1d5d8-113">-AppAlias</span></span>
<span data-ttu-id="1d5d8-114">App-Alias aus dem Menüelement "Start"</span><span class="sxs-lookup"><span data-stu-id="1d5d8-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="1d5d8-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="1d5d8-115">-CommandLineArgument</span></span>
<span data-ttu-id="1d5d8-116">Befehlszeilenargumente für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="1d5d8-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="1d5d8-117">-CommandLineSetting</span></span>
<span data-ttu-id="1d5d8-118">Gibt an, ob diese veröffentlichte Anwendung mit vom Client bereitgestellten Befehlszeilenargumenten, Befehlszeilenargumenten, die zur Veröffentlichungszeit angegeben werden, oder überhaupt keine Befehlszeilenargumente gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="1d5d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5d8-119">-DefaultProfile</span></span>
<span data-ttu-id="1d5d8-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d5d8-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d5d8-121">-Description</span></span>
<span data-ttu-id="1d5d8-122">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-122">Description of Application.</span></span>

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

### <span data-ttu-id="1d5d8-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1d5d8-123">-FilePath</span></span>
<span data-ttu-id="1d5d8-124">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="1d5d8-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1d5d8-125">-FriendlyName</span></span>
<span data-ttu-id="1d5d8-126">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="1d5d8-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="1d5d8-127">-GroupName</span></span>
<span data-ttu-id="1d5d8-128">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1d5d8-128">The name of the application group</span></span>

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

### <span data-ttu-id="1d5d8-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="1d5d8-129">-IconIndex</span></span>
<span data-ttu-id="1d5d8-130">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-130">Index of the icon.</span></span>

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

### <span data-ttu-id="1d5d8-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="1d5d8-131">-IconPath</span></span>
<span data-ttu-id="1d5d8-132">Pfad zu Symbol.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-132">Path to icon.</span></span>

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

### <span data-ttu-id="1d5d8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1d5d8-133">-Name</span></span>
<span data-ttu-id="1d5d8-134">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1d5d8-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="1d5d8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5d8-135">-ResourceGroupName</span></span>
<span data-ttu-id="1d5d8-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-136">The name of the resource group.</span></span>
<span data-ttu-id="1d5d8-137">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1d5d8-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="1d5d8-138">-ShowInPortal</span></span>
<span data-ttu-id="1d5d8-139">Gibt an, ob das RemoteApp-Programm auf dem Web Access für Remote Desktop-Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="1d5d8-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1d5d8-140">-SubscriptionId</span></span>
<span data-ttu-id="1d5d8-141">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1d5d8-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d5d8-142">-Confirm</span></span>
<span data-ttu-id="1d5d8-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d5d8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d5d8-144">-WhatIf</span></span>
<span data-ttu-id="1d5d8-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d5d8-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d5d8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5d8-147">CommonParameters</span></span>
<span data-ttu-id="1d5d8-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d5d8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5d8-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d5d8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5d8-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d5d8-150">INPUTS</span></span>

## <span data-ttu-id="1d5d8-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d5d8-151">OUTPUTS</span></span>

### <span data-ttu-id="1d5d8-152">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="1d5d8-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="1d5d8-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d5d8-153">NOTES</span></span>

<span data-ttu-id="1d5d8-154">Aliase</span><span class="sxs-lookup"><span data-stu-id="1d5d8-154">ALIASES</span></span>

## <span data-ttu-id="1d5d8-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d5d8-155">RELATED LINKS</span></span>

