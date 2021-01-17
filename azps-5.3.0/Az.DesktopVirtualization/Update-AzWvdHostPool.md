---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469892"
---
# <span data-ttu-id="4aabb-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="4aabb-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="4aabb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aabb-102">SYNOPSIS</span></span>
<span data-ttu-id="4aabb-103">Aktualisieren Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-103">Update a host pool.</span></span>

## <span data-ttu-id="4aabb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aabb-104">SYNTAX</span></span>

### <span data-ttu-id="4aabb-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aabb-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4aabb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4aabb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4aabb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aabb-107">DESCRIPTION</span></span>
<span data-ttu-id="4aabb-108">Aktualisieren Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-108">Update a host pool.</span></span>

## <span data-ttu-id="4aabb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aabb-109">EXAMPLES</span></span>

### <span data-ttu-id="4aabb-110">Beispiel 1: Aktualisieren eines Windows Virtual Desktop HostPools nach Name</span><span class="sxs-lookup"><span data-stu-id="4aabb-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="4aabb-111">Mit diesem Befehl wird ein Windows Virtual Desktop HostPool in einer Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4aabb-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="4aabb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aabb-112">PARAMETERS</span></span>

### <span data-ttu-id="4aabb-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="4aabb-113">-CustomRdpProperty</span></span>
<span data-ttu-id="4aabb-114">Benutzerdefinierte rdp-Eigenschaft von HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="4aabb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aabb-115">-DefaultProfile</span></span>
<span data-ttu-id="4aabb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aabb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aabb-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aabb-117">-Description</span></span>
<span data-ttu-id="4aabb-118">Beschreibung von HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="4aabb-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4aabb-119">-FriendlyName</span></span>
<span data-ttu-id="4aabb-120">Anzeigename von HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="4aabb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aabb-121">-InputObject</span></span>
<span data-ttu-id="4aabb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4aabb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4aabb-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="4aabb-123">-LoadBalancerType</span></span>
<span data-ttu-id="4aabb-124">Der Typ des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="4aabb-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="4aabb-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="4aabb-125">-MaxSessionLimit</span></span>
<span data-ttu-id="4aabb-126">Die maximale Sitzungsgrenze von HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="4aabb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4aabb-127">-Name</span></span>
<span data-ttu-id="4aabb-128">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4aabb-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4aabb-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="4aabb-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="4aabb-130">PersonalDesktopAssignment-Typ für HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="4aabb-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="4aabb-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="4aabb-132">Der Typ der bevorzugten Anwendungsgruppe, Standardeinstellung "Desktopanwendungsgruppe"</span><span class="sxs-lookup"><span data-stu-id="4aabb-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="4aabb-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="4aabb-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="4aabb-134">Ablaufzeit des Registrierungstokens.</span><span class="sxs-lookup"><span data-stu-id="4aabb-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="4aabb-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="4aabb-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="4aabb-136">Der Typ des Zurücksetzens des Tokens.</span><span class="sxs-lookup"><span data-stu-id="4aabb-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="4aabb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aabb-137">-ResourceGroupName</span></span>
<span data-ttu-id="4aabb-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4aabb-138">The name of the resource group.</span></span>
<span data-ttu-id="4aabb-139">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="4aabb-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4aabb-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="4aabb-140">-Ring</span></span>
<span data-ttu-id="4aabb-141">Die Ringnummer von HostPool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="4aabb-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="4aabb-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="4aabb-143">URL des ADFS-Kundenservers zum Signieren von WVD-SSO-Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="4aabb-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="4aabb-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="4aabb-144">-SsoClientId</span></span>
<span data-ttu-id="4aabb-145">ClientId für die registrierte Vertrauende Partei, die zum Ausstellen von WVD-SSO-Zertifikaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aabb-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="4aabb-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="4aabb-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="4aabb-147">Pfad zu Azure KeyVault, der den geheimen Schlüssel speichert, der für die Kommunikation mit ADFS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aabb-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="4aabb-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="4aabb-148">-SsoContext</span></span>
<span data-ttu-id="4aabb-149">Pfad zu Keyvault, der den geheimen Schlüssel "ssoContext" enthält.</span><span class="sxs-lookup"><span data-stu-id="4aabb-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="4aabb-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="4aabb-150">-SsoSecretType</span></span>
<span data-ttu-id="4aabb-151">Der Typ des einzelnen Zeichens für den geheimen Typ.</span><span class="sxs-lookup"><span data-stu-id="4aabb-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aabb-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="4aabb-152">-StartVMOnConnect</span></span>
<span data-ttu-id="4aabb-153">Das Kennzeichen zum Aktivieren/Deaktivieren des Features "StartVMOnConnect".</span><span class="sxs-lookup"><span data-stu-id="4aabb-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="4aabb-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aabb-154">-SubscriptionId</span></span>
<span data-ttu-id="4aabb-155">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4aabb-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4aabb-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="4aabb-156">-Tag</span></span>
<span data-ttu-id="4aabb-157">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="4aabb-157">tags to be updated</span></span>

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

### <span data-ttu-id="4aabb-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="4aabb-158">-ValidationEnvironment</span></span>
<span data-ttu-id="4aabb-159">Ist überprüfungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="4aabb-159">Is validation environment.</span></span>

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

### <span data-ttu-id="4aabb-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="4aabb-160">-VMTemplate</span></span>
<span data-ttu-id="4aabb-161">VM template for sessionhosts configuration within hostpool.</span><span class="sxs-lookup"><span data-stu-id="4aabb-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="4aabb-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aabb-162">-Confirm</span></span>
<span data-ttu-id="4aabb-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aabb-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aabb-164">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4aabb-164">-WhatIf</span></span>
<span data-ttu-id="4aabb-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aabb-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aabb-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aabb-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aabb-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aabb-167">CommonParameters</span></span>
<span data-ttu-id="4aabb-168">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aabb-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aabb-169">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aabb-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aabb-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aabb-170">INPUTS</span></span>

### <span data-ttu-id="4aabb-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4aabb-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4aabb-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aabb-172">OUTPUTS</span></span>

### <span data-ttu-id="4aabb-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="4aabb-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="4aabb-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aabb-174">NOTES</span></span>

<span data-ttu-id="4aabb-175">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4aabb-175">ALIASES</span></span>

<span data-ttu-id="4aabb-176">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4aabb-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4aabb-177">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4aabb-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4aabb-178">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4aabb-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4aabb-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="4aabb-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4aabb-180">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="4aabb-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4aabb-181">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="4aabb-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4aabb-182">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="4aabb-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4aabb-183">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4aabb-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4aabb-184">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="4aabb-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4aabb-185">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="4aabb-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4aabb-186">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4aabb-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4aabb-187">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="4aabb-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="4aabb-188">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="4aabb-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4aabb-189">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4aabb-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4aabb-190">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="4aabb-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4aabb-191">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4aabb-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4aabb-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aabb-192">RELATED LINKS</span></span>

