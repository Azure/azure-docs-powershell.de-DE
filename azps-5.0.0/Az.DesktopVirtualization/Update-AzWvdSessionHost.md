---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175778"
---
# <span data-ttu-id="c4a6e-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="c4a6e-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="c4a6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a6e-103">Aktualisieren eines Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="c4a6e-103">Update a session host.</span></span>

## <span data-ttu-id="c4a6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4a6e-104">SYNTAX</span></span>

### <span data-ttu-id="c4a6e-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4a6e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4a6e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4a6e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4a6e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a6e-108">Aktualisieren eines Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="c4a6e-108">Update a session host.</span></span>

## <span data-ttu-id="c4a6e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a6e-110">Beispiel 1: Aktualisieren eines Windows Virtual Desktop-SessionHost nach Name</span><span class="sxs-lookup"><span data-stu-id="c4a6e-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="c4a6e-111">Mit diesem Befehl wird ein Windows Virtual Desktop-SessionHost in einem Host Pool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="c4a6e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4a6e-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a6e-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="c4a6e-113">-AllowNewSession</span></span>
<span data-ttu-id="c4a6e-114">Eine neue Sitzung zulassen.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-114">Allow a new session.</span></span>

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

### <span data-ttu-id="c4a6e-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="c4a6e-115">-AssignedUser</span></span>
<span data-ttu-id="c4a6e-116">Benutzer, der SessionHost zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="c4a6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a6e-117">-DefaultProfile</span></span>
<span data-ttu-id="c4a6e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a6e-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c4a6e-119">-HostPoolName</span></span>
<span data-ttu-id="c4a6e-120">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="c4a6e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4a6e-121">-InputObject</span></span>
<span data-ttu-id="c4a6e-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4a6e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a6e-123">-Name</span></span>
<span data-ttu-id="c4a6e-124">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="c4a6e-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4a6e-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-126">The name of the resource group.</span></span>
<span data-ttu-id="c4a6e-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c4a6e-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c4a6e-128">-SubscriptionId</span></span>
<span data-ttu-id="c4a6e-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c4a6e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4a6e-130">-Confirm</span></span>
<span data-ttu-id="c4a6e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a6e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a6e-132">-WhatIf</span></span>
<span data-ttu-id="c4a6e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a6e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a6e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a6e-135">CommonParameters</span></span>
<span data-ttu-id="c4a6e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a6e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a6e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a6e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4a6e-138">INPUTS</span></span>

### <span data-ttu-id="c4a6e-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c4a6e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c4a6e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4a6e-140">OUTPUTS</span></span>

### <span data-ttu-id="c4a6e-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="c4a6e-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="c4a6e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4a6e-142">NOTES</span></span>

<span data-ttu-id="c4a6e-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="c4a6e-143">ALIASES</span></span>

<span data-ttu-id="c4a6e-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4a6e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4a6e-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4a6e-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4a6e-147">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c4a6e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4a6e-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c4a6e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c4a6e-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c4a6e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c4a6e-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="c4a6e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c4a6e-151">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c4a6e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c4a6e-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c4a6e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4a6e-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4a6e-154">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4a6e-155">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="c4a6e-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c4a6e-156">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c4a6e-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4a6e-157">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="c4a6e-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c4a6e-158">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c4a6e-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c4a6e-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4a6e-159">RELATED LINKS</span></span>

