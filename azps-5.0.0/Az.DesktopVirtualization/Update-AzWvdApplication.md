---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177694"
---
# <span data-ttu-id="f9749-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="f9749-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="f9749-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9749-102">SYNOPSIS</span></span>
<span data-ttu-id="f9749-103">Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="f9749-103">Update an application.</span></span>

## <span data-ttu-id="f9749-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9749-104">SYNTAX</span></span>

### <span data-ttu-id="f9749-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9749-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f9749-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f9749-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9749-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9749-107">DESCRIPTION</span></span>
<span data-ttu-id="f9749-108">Aktualisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="f9749-108">Update an application.</span></span>

## <span data-ttu-id="f9749-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9749-109">EXAMPLES</span></span>

### <span data-ttu-id="f9749-110">Beispiel 1: Aktualisieren einer virtuellen Windows-Desktop Anwendung</span><span class="sxs-lookup"><span data-stu-id="f9749-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="f9749-111">Mit diesem Befehl wird eine virtuelle Windows-Desktop Anwendung in einer Applicaton-Gruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f9749-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="f9749-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9749-112">PARAMETERS</span></span>

### <span data-ttu-id="f9749-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="f9749-113">-CommandLineArgument</span></span>
<span data-ttu-id="f9749-114">Befehlszeilenargumente für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f9749-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="f9749-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="f9749-115">-CommandLineSetting</span></span>
<span data-ttu-id="f9749-116">Gibt an, ob diese veröffentlichte Anwendung mit vom Client bereitgestellten Befehlszeilenargumenten, Befehlszeilenargumenten, die zur Veröffentlichungszeit angegeben werden, oder überhaupt keine Befehlszeilenargumente gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9749-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="f9749-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9749-117">-DefaultProfile</span></span>
<span data-ttu-id="f9749-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9749-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9749-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9749-119">-Description</span></span>
<span data-ttu-id="f9749-120">Beschreibung der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f9749-120">Description of Application.</span></span>

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

### <span data-ttu-id="f9749-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f9749-121">-FilePath</span></span>
<span data-ttu-id="f9749-122">Gibt einen Pfad für die ausführbare Datei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="f9749-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="f9749-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f9749-123">-FriendlyName</span></span>
<span data-ttu-id="f9749-124">Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f9749-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="f9749-125">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f9749-125">-GroupName</span></span>
<span data-ttu-id="f9749-126">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-126">The name of the application group</span></span>

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

### <span data-ttu-id="f9749-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="f9749-127">-IconIndex</span></span>
<span data-ttu-id="f9749-128">Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="f9749-128">Index of the icon.</span></span>

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

### <span data-ttu-id="f9749-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="f9749-129">-IconPath</span></span>
<span data-ttu-id="f9749-130">Pfad zu Symbol.</span><span class="sxs-lookup"><span data-stu-id="f9749-130">Path to icon.</span></span>

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

### <span data-ttu-id="f9749-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9749-131">-InputObject</span></span>
<span data-ttu-id="f9749-132">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f9749-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9749-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f9749-133">-Name</span></span>
<span data-ttu-id="f9749-134">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="f9749-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9749-135">-ResourceGroupName</span></span>
<span data-ttu-id="f9749-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9749-136">The name of the resource group.</span></span>
<span data-ttu-id="f9749-137">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f9749-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f9749-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="f9749-138">-ShowInPortal</span></span>
<span data-ttu-id="f9749-139">Gibt an, ob das RemoteApp-Programm auf dem Web Access für Remote Desktop-Server angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9749-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="f9749-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f9749-140">-SubscriptionId</span></span>
<span data-ttu-id="f9749-141">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f9749-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f9749-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9749-142">-Tag</span></span>
<span data-ttu-id="f9749-143">Tags, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="f9749-143">tags to be updated</span></span>

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

### <span data-ttu-id="f9749-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9749-144">-Confirm</span></span>
<span data-ttu-id="f9749-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9749-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9749-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9749-146">-WhatIf</span></span>
<span data-ttu-id="f9749-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9749-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9749-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9749-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9749-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9749-149">CommonParameters</span></span>
<span data-ttu-id="f9749-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9749-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9749-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9749-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9749-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9749-152">INPUTS</span></span>

### <span data-ttu-id="f9749-153">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f9749-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f9749-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9749-154">OUTPUTS</span></span>

### <span data-ttu-id="f9749-155">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="f9749-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="f9749-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9749-156">NOTES</span></span>

<span data-ttu-id="f9749-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="f9749-157">ALIASES</span></span>

<span data-ttu-id="f9749-158">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9749-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9749-159">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9749-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9749-160">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f9749-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9749-161">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f9749-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9749-162">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f9749-163">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f9749-164">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f9749-165">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f9749-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f9749-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f9749-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9749-167">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9749-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f9749-168">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f9749-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="f9749-169">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="f9749-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f9749-170">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f9749-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f9749-171">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="f9749-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f9749-172">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f9749-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f9749-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9749-173">RELATED LINKS</span></span>

