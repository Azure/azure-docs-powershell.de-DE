---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177827"
---
# <span data-ttu-id="5f4d3-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="5f4d3-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="5f4d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4d3-103">Aktualisieren eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="5f4d3-103">Update a host pool.</span></span>

## <span data-ttu-id="5f4d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f4d3-104">SYNTAX</span></span>

### <span data-ttu-id="5f4d3-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f4d3-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f4d3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5f4d3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f4d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f4d3-107">DESCRIPTION</span></span>
<span data-ttu-id="5f4d3-108">Aktualisieren eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="5f4d3-108">Update a host pool.</span></span>

## <span data-ttu-id="5f4d3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f4d3-109">EXAMPLES</span></span>

### <span data-ttu-id="5f4d3-110">Beispiel 1: Aktualisieren eines Windows Virtual Desktop-HostPool nach Name</span><span class="sxs-lookup"><span data-stu-id="5f4d3-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="5f4d3-111">Mit diesem Befehl wird eine Windows Virtual Desktop-HostPool in einer Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="5f4d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f4d3-112">PARAMETERS</span></span>

### <span data-ttu-id="5f4d3-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="5f4d3-113">-CustomRdpProperty</span></span>
<span data-ttu-id="5f4d3-114">Benutzerdefinierte RDP-Eigenschaft von HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="5f4d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4d3-115">-DefaultProfile</span></span>
<span data-ttu-id="5f4d3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f4d3-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f4d3-117">-Description</span></span>
<span data-ttu-id="5f4d3-118">Beschreibung von HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="5f4d3-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f4d3-119">-FriendlyName</span></span>
<span data-ttu-id="5f4d3-120">Anzeigename des HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="5f4d3-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f4d3-121">-InputObject</span></span>
<span data-ttu-id="5f4d3-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f4d3-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="5f4d3-123">-LoadBalancerType</span></span>
<span data-ttu-id="5f4d3-124">Der Typ des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="5f4d3-125">-MaxSessionLimit</span></span>
<span data-ttu-id="5f4d3-126">Die maximale Sitzungs Grenze von HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="5f4d3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5f4d3-127">-Name</span></span>
<span data-ttu-id="5f4d3-128">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="5f4d3-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="5f4d3-130">PersonalDesktopAssignment-Typ für HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="5f4d3-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="5f4d3-132">Der Typ des bevorzugten Anwendungsgruppen Typs, standardmäßig für die Desktop Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5f4d3-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="5f4d3-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="5f4d3-134">Ablaufzeit des Registrierungs Tokens.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="5f4d3-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="5f4d3-136">Der Typ des Zurücksetzens des Tokens.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4d3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f4d3-137">-ResourceGroupName</span></span>
<span data-ttu-id="5f4d3-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-138">The name of the resource group.</span></span>
<span data-ttu-id="5f4d3-139">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f4d3-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="5f4d3-140">-Ring</span></span>
<span data-ttu-id="5f4d3-141">Die Nummer des HostPool-Rings.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="5f4d3-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="5f4d3-142">-SsoContext</span></span>
<span data-ttu-id="5f4d3-143">Pfad zu keyvault mit ssoContext Secret</span><span class="sxs-lookup"><span data-stu-id="5f4d3-143">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="5f4d3-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5f4d3-144">-SubscriptionId</span></span>
<span data-ttu-id="5f4d3-145">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f4d3-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f4d3-146">-Tag</span></span>
<span data-ttu-id="5f4d3-147">Tags, die aktualisiert werden sollen</span><span class="sxs-lookup"><span data-stu-id="5f4d3-147">tags to be updated</span></span>

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

### <span data-ttu-id="5f4d3-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="5f4d3-148">-ValidationEnvironment</span></span>
<span data-ttu-id="5f4d3-149">Ist eine Validierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-149">Is validation environment.</span></span>

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

### <span data-ttu-id="5f4d3-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f4d3-150">-Confirm</span></span>
<span data-ttu-id="5f4d3-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f4d3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f4d3-152">-WhatIf</span></span>
<span data-ttu-id="5f4d3-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f4d3-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f4d3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4d3-155">CommonParameters</span></span>
<span data-ttu-id="5f4d3-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4d3-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f4d3-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4d3-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f4d3-158">INPUTS</span></span>

### <span data-ttu-id="5f4d3-159">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5f4d3-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f4d3-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f4d3-160">OUTPUTS</span></span>

### <span data-ttu-id="5f4d3-161">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="5f4d3-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="5f4d3-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f4d3-162">NOTES</span></span>

<span data-ttu-id="5f4d3-163">Aliase</span><span class="sxs-lookup"><span data-stu-id="5f4d3-163">ALIASES</span></span>

<span data-ttu-id="5f4d3-164">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f4d3-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f4d3-165">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f4d3-166">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f4d3-167">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5f4d3-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f4d3-168">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5f4d3-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f4d3-169">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5f4d3-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f4d3-170">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="5f4d3-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f4d3-171">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5f4d3-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f4d3-172">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5f4d3-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f4d3-173">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f4d3-174">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f4d3-175">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="5f4d3-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f4d3-176">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5f4d3-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f4d3-177">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="5f4d3-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f4d3-178">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5f4d3-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f4d3-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f4d3-179">RELATED LINKS</span></span>

