---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177691"
---
# <span data-ttu-id="a9012-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a9012-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="a9012-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9012-102">SYNOPSIS</span></span>
<span data-ttu-id="a9012-103">Aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9012-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="a9012-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9012-104">SYNTAX</span></span>

### <span data-ttu-id="a9012-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9012-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9012-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a9012-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a9012-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9012-107">DESCRIPTION</span></span>
<span data-ttu-id="a9012-108">Aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9012-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="a9012-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9012-109">EXAMPLES</span></span>

### <span data-ttu-id="a9012-110">Beispiel 1: Erstellen einer virtuellen Windows-Desktop Anwendung mit Namen</span><span class="sxs-lookup"><span data-stu-id="a9012-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="a9012-111">Mit diesem Befehl wird eine Windows Virtual Desktop-Anwendungsgruppe in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9012-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="a9012-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9012-112">PARAMETERS</span></span>

### <span data-ttu-id="a9012-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9012-113">-DefaultProfile</span></span>
<span data-ttu-id="a9012-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9012-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9012-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9012-115">-Description</span></span>
<span data-ttu-id="a9012-116">Beschreibung von ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9012-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="a9012-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9012-117">-FriendlyName</span></span>
<span data-ttu-id="a9012-118">Anzeigename der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="a9012-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="a9012-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9012-119">-InputObject</span></span>
<span data-ttu-id="a9012-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a9012-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a9012-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a9012-121">-Name</span></span>
<span data-ttu-id="a9012-122">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9012-122">The name of the application group</span></span>

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

### <span data-ttu-id="a9012-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9012-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9012-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a9012-124">The name of the resource group.</span></span>
<span data-ttu-id="a9012-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a9012-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9012-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a9012-126">-SubscriptionId</span></span>
<span data-ttu-id="a9012-127">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a9012-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9012-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9012-128">-Tag</span></span>
<span data-ttu-id="a9012-129">Tags, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="a9012-129">tags to be updated</span></span>

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

### <span data-ttu-id="a9012-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9012-130">-Confirm</span></span>
<span data-ttu-id="a9012-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9012-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9012-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9012-132">-WhatIf</span></span>
<span data-ttu-id="a9012-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9012-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9012-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9012-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9012-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9012-135">CommonParameters</span></span>
<span data-ttu-id="a9012-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9012-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9012-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9012-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9012-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9012-138">INPUTS</span></span>

### <span data-ttu-id="a9012-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a9012-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a9012-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9012-140">OUTPUTS</span></span>

### <span data-ttu-id="a9012-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a9012-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="a9012-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9012-142">NOTES</span></span>

<span data-ttu-id="a9012-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="a9012-143">ALIASES</span></span>

<span data-ttu-id="a9012-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9012-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9012-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9012-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9012-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a9012-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9012-147">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9012-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9012-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9012-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a9012-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a9012-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a9012-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="a9012-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a9012-151">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a9012-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a9012-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a9012-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9012-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a9012-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a9012-154">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a9012-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9012-155">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="a9012-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a9012-156">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a9012-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a9012-157">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="a9012-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a9012-158">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a9012-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a9012-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9012-159">RELATED LINKS</span></span>

