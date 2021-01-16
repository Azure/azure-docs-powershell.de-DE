---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467891"
---
# <span data-ttu-id="1fc8b-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="1fc8b-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="1fc8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc8b-103">Erstellen oder aktualisieren Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-103">Create or update a host pool.</span></span>

## <span data-ttu-id="1fc8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fc8b-104">SYNTAX</span></span>

### <span data-ttu-id="1fc8b-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fc8b-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fc8b-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="1fc8b-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fc8b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fc8b-107">DESCRIPTION</span></span>
<span data-ttu-id="1fc8b-108">Erstellen oder aktualisieren Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-108">Create or update a host pool.</span></span>

## <span data-ttu-id="1fc8b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fc8b-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc8b-110">Beispiel 1: Erstellen eines virtuellen Desktophostpools für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="1fc8b-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="1fc8b-111">Mit diesem Befehl wird ein Windows Virtual Desktop HostPool in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="1fc8b-112">Beispiel 1: Erstellen eines virtuellen Desktophostpools für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="1fc8b-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="1fc8b-113">Mit diesem Befehl wird ein Windows Virtual Desktop HostPool in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="1fc8b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fc8b-114">PARAMETERS</span></span>

### <span data-ttu-id="1fc8b-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="1fc8b-115">-CustomRdpProperty</span></span>
<span data-ttu-id="1fc8b-116">Benutzerdefinierte rdp-Eigenschaft von HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="1fc8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc8b-117">-DefaultProfile</span></span>
<span data-ttu-id="1fc8b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc8b-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fc8b-119">-Description</span></span>
<span data-ttu-id="1fc8b-120">Beschreibung von HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="1fc8b-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc8b-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="1fc8b-122">Gruppenname der Desktop-App</span><span class="sxs-lookup"><span data-stu-id="1fc8b-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="1fc8b-123">-ExpirationTime</span></span>
<span data-ttu-id="1fc8b-124">Ablaufzeit des Registrierungstokens.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="1fc8b-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1fc8b-125">-FriendlyName</span></span>
<span data-ttu-id="1fc8b-126">Anzeigename von HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="1fc8b-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="1fc8b-127">-HostPoolType</span></span>
<span data-ttu-id="1fc8b-128">HostPool-Typ für Desktop.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="1fc8b-129">-LoadBalancerType</span></span>
<span data-ttu-id="1fc8b-130">Der Typ des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-131">-Location</span><span class="sxs-lookup"><span data-stu-id="1fc8b-131">-Location</span></span>
<span data-ttu-id="1fc8b-132">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="1fc8b-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="1fc8b-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="1fc8b-133">-MaxSessionLimit</span></span>
<span data-ttu-id="1fc8b-134">Die maximale Sitzungsgrenze von HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="1fc8b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="1fc8b-135">-Name</span></span>
<span data-ttu-id="1fc8b-136">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1fc8b-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="1fc8b-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="1fc8b-138">PersonalDesktopAssignment-Typ für HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="1fc8b-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="1fc8b-140">Der Typ des bevorzugten Anwendungsgruppentyps, Standardmäßig "Desktopanwendungsgruppe"</span><span class="sxs-lookup"><span data-stu-id="1fc8b-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="1fc8b-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="1fc8b-142">Die codierte Zeichenfolge des Registrierungstokens base64.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="1fc8b-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="1fc8b-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="1fc8b-144">Der Typ des Zurücksetzens des Tokens.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc8b-145">-ResourceGroupName</span></span>
<span data-ttu-id="1fc8b-146">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-146">The name of the resource group.</span></span>
<span data-ttu-id="1fc8b-147">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1fc8b-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="1fc8b-148">-Ring</span></span>
<span data-ttu-id="1fc8b-149">Die Ringnummer von HostPool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="1fc8b-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="1fc8b-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="1fc8b-151">URL des ADFS-Kundenservers zum Signieren von WVD-SSO-Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="1fc8b-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="1fc8b-152">-SsoClientId</span></span>
<span data-ttu-id="1fc8b-153">ClientId für die registrierte Vertrauende Partei, die zum Ausstellen von WVD-SSO-Zertifikaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="1fc8b-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="1fc8b-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="1fc8b-155">Pfad zu Azure KeyVault, der den geheimen Schlüssel für die Kommunikation mit ADFS speichert.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="1fc8b-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="1fc8b-156">-SsoContext</span></span>
<span data-ttu-id="1fc8b-157">Pfad zu Keyvault, der den geheimen Schlüssel "ssoContext" enthält.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="1fc8b-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="1fc8b-158">-SsoSecretType</span></span>
<span data-ttu-id="1fc8b-159">Der Typ des einzelnen Zeichens für den geheimen Typ.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="1fc8b-160">-StartVMOnConnect</span></span>
<span data-ttu-id="1fc8b-161">Das Kennzeichen zum Aktivieren/Deaktivieren des Features "StartVMOnConnect".</span><span class="sxs-lookup"><span data-stu-id="1fc8b-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fc8b-162">-SubscriptionId</span></span>
<span data-ttu-id="1fc8b-163">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1fc8b-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fc8b-164">-Tag</span></span>
<span data-ttu-id="1fc8b-165">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-165">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="1fc8b-166">-ValidationEnvironment</span></span>
<span data-ttu-id="1fc8b-167">Ist die Gültigkeitsprüfungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-167">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="1fc8b-168">-VMTemplate</span></span>
<span data-ttu-id="1fc8b-169">VM template for sessionhosts configuration within hostpool.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="1fc8b-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1fc8b-170">-WorkspaceName</span></span>
<span data-ttu-id="1fc8b-171">Arbeitsbereichsname</span><span class="sxs-lookup"><span data-stu-id="1fc8b-171">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc8b-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fc8b-172">-Confirm</span></span>
<span data-ttu-id="1fc8b-173">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc8b-174">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1fc8b-174">-WhatIf</span></span>
<span data-ttu-id="1fc8b-175">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc8b-176">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc8b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc8b-177">CommonParameters</span></span>
<span data-ttu-id="1fc8b-178">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc8b-179">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fc8b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc8b-180">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fc8b-180">INPUTS</span></span>

## <span data-ttu-id="1fc8b-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fc8b-181">OUTPUTS</span></span>

### <span data-ttu-id="1fc8b-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="1fc8b-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="1fc8b-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1fc8b-183">NOTES</span></span>

<span data-ttu-id="1fc8b-184">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1fc8b-184">ALIASES</span></span>

## <span data-ttu-id="1fc8b-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1fc8b-185">RELATED LINKS</span></span>

