---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: 5b69ff6bb04f1e8b1ae5e13fbab2c6a5f7c67927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934408"
---
# <span data-ttu-id="a70b9-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="a70b9-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="a70b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a70b9-103">Aktualisieren eines Hostpools</span><span class="sxs-lookup"><span data-stu-id="a70b9-103">Update a host pool.</span></span>

## <span data-ttu-id="a70b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a70b9-104">SYNTAX</span></span>

### <span data-ttu-id="a70b9-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a70b9-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="a70b9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a70b9-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="a70b9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a70b9-107">DESCRIPTION</span></span>
<span data-ttu-id="a70b9-108">Aktualisieren eines Hostpools</span><span class="sxs-lookup"><span data-stu-id="a70b9-108">Update a host pool.</span></span>

## <span data-ttu-id="a70b9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a70b9-109">EXAMPLES</span></span>

### <span data-ttu-id="a70b9-110">Beispiel 1: Aktualisieren eines virtuellen Windows-DesktophostPools nach Name</span><span class="sxs-lookup"><span data-stu-id="a70b9-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="a70b9-111">Mit diesem Befehl wird eine Windows Virtual Desktop HostPool in einer Ressourcengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a70b9-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="a70b9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a70b9-112">PARAMETERS</span></span>

### <span data-ttu-id="a70b9-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="a70b9-113">-CustomRdpProperty</span></span>
<span data-ttu-id="a70b9-114">Benutzerdefinierte rdp-Eigenschaft von HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="a70b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70b9-115">-DefaultProfile</span></span>
<span data-ttu-id="a70b9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a70b9-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a70b9-117">-Description</span></span>
<span data-ttu-id="a70b9-118">Beschreibung von HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="a70b9-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a70b9-119">-FriendlyName</span></span>
<span data-ttu-id="a70b9-120">Anzeigename von HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="a70b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a70b9-121">-InputObject</span></span>
<span data-ttu-id="a70b9-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a70b9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a70b9-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="a70b9-123">-LoadBalancerType</span></span>
<span data-ttu-id="a70b9-124">Der Typ des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="a70b9-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="a70b9-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="a70b9-125">-MaxSessionLimit</span></span>
<span data-ttu-id="a70b9-126">Das maximale Sitzungslimit von HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="a70b9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a70b9-127">-Name</span></span>
<span data-ttu-id="a70b9-128">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a70b9-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a70b9-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="a70b9-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="a70b9-130">PersonalDesktopAssignment-Typ für HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="a70b9-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="a70b9-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="a70b9-132">Der Typ des bevorzugten Anwendungsgruppentyps, standardmäßig zur Gruppe "Desktopanwendung"</span><span class="sxs-lookup"><span data-stu-id="a70b9-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="a70b9-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="a70b9-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="a70b9-134">Ablaufzeit des Registrierungstokens.</span><span class="sxs-lookup"><span data-stu-id="a70b9-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="a70b9-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="a70b9-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="a70b9-136">Der Typ des Zurücksetzens des Tokens.</span><span class="sxs-lookup"><span data-stu-id="a70b9-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="a70b9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70b9-137">-ResourceGroupName</span></span>
<span data-ttu-id="a70b9-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a70b9-138">The name of the resource group.</span></span>
<span data-ttu-id="a70b9-139">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a70b9-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a70b9-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="a70b9-140">-Ring</span></span>
<span data-ttu-id="a70b9-141">Die Ringnummer von HostPool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="a70b9-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="a70b9-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="a70b9-143">URL zum Kunden-ADFS-Server zum Signieren von WVD-SSO-Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="a70b9-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="a70b9-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="a70b9-144">-SsoClientId</span></span>
<span data-ttu-id="a70b9-145">ClientId für die registrierte Vertrauenspartei, die zum Ausstellen von WVD-SSO-Zertifikaten verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a70b9-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="a70b9-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="a70b9-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="a70b9-147">Pfad zu Azure KeyVault zum Speichern des Geheimschlüssels, der für die Kommunikation mit ADFS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70b9-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="a70b9-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="a70b9-148">-SsoContext</span></span>
<span data-ttu-id="a70b9-149">Pfad zu keyvault, der ssoContext secret enthält.</span><span class="sxs-lookup"><span data-stu-id="a70b9-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="a70b9-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="a70b9-150">-SsoSecretType</span></span>
<span data-ttu-id="a70b9-151">Der Typ des einzelnen Zeichens unter Geheimer Typ.</span><span class="sxs-lookup"><span data-stu-id="a70b9-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="a70b9-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="a70b9-152">-StartVMOnConnect</span></span>
<span data-ttu-id="a70b9-153">Das Kennzeichen zum Aktivieren/Deaktivieren des Features StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="a70b9-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="a70b9-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a70b9-154">-SubscriptionId</span></span>
<span data-ttu-id="a70b9-155">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a70b9-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a70b9-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a70b9-156">-Tag</span></span>
<span data-ttu-id="a70b9-157">zu aktualisierende Tags</span><span class="sxs-lookup"><span data-stu-id="a70b9-157">tags to be updated</span></span>

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

### <span data-ttu-id="a70b9-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="a70b9-158">-ValidationEnvironment</span></span>
<span data-ttu-id="a70b9-159">Ist überprüfungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="a70b9-159">Is validation environment.</span></span>

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

### <span data-ttu-id="a70b9-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="a70b9-160">-VMTemplate</span></span>
<span data-ttu-id="a70b9-161">VM-Vorlage für die Sessionhosts-Konfiguration in hostpool.</span><span class="sxs-lookup"><span data-stu-id="a70b9-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="a70b9-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a70b9-162">-Confirm</span></span>
<span data-ttu-id="a70b9-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a70b9-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70b9-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70b9-164">-WhatIf</span></span>
<span data-ttu-id="a70b9-165">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a70b9-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70b9-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a70b9-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70b9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70b9-167">CommonParameters</span></span>
<span data-ttu-id="a70b9-168">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70b9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70b9-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a70b9-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70b9-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a70b9-170">INPUTS</span></span>

### <span data-ttu-id="a70b9-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a70b9-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a70b9-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a70b9-172">OUTPUTS</span></span>

### <span data-ttu-id="a70b9-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="a70b9-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="a70b9-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a70b9-174">NOTES</span></span>

<span data-ttu-id="a70b9-175">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a70b9-175">ALIASES</span></span>

<span data-ttu-id="a70b9-176">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a70b9-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a70b9-177">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a70b9-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a70b9-178">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a70b9-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a70b9-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a70b9-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a70b9-180">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a70b9-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a70b9-181">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a70b9-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a70b9-182">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="a70b9-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a70b9-183">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a70b9-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a70b9-184">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a70b9-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a70b9-185">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="a70b9-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a70b9-186">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a70b9-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a70b9-187">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a70b9-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="a70b9-188">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="a70b9-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a70b9-189">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a70b9-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a70b9-190">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="a70b9-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a70b9-191">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a70b9-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a70b9-192">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a70b9-192">RELATED LINKS</span></span>

