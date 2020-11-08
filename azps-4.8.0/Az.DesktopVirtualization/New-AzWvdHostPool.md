---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007997"
---
# <span data-ttu-id="f5ad0-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="f5ad0-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="f5ad0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ad0-103">Erstellen oder Aktualisieren eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="f5ad0-103">Create or update a host pool.</span></span>

## <span data-ttu-id="f5ad0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5ad0-104">SYNTAX</span></span>

### <span data-ttu-id="f5ad0-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5ad0-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5ad0-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="f5ad0-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5ad0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5ad0-107">DESCRIPTION</span></span>
<span data-ttu-id="f5ad0-108">Erstellen oder Aktualisieren eines Host Pools</span><span class="sxs-lookup"><span data-stu-id="f5ad0-108">Create or update a host pool.</span></span>

## <span data-ttu-id="f5ad0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5ad0-109">EXAMPLES</span></span>

### <span data-ttu-id="f5ad0-110">Beispiel 1: Erstellen einer virtuellen Windows-Desktop-HostPool nach Namen</span><span class="sxs-lookup"><span data-stu-id="f5ad0-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="f5ad0-111">Mit diesem Befehl wird eine Windows Virtual Desktop-HostPool in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="f5ad0-112">Beispiel 1: Erstellen einer virtuellen Windows-Desktop-HostPool nach Namen</span><span class="sxs-lookup"><span data-stu-id="f5ad0-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="f5ad0-113">Mit diesem Befehl wird eine Windows Virtual Desktop-HostPool in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="f5ad0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5ad0-114">PARAMETERS</span></span>

### <span data-ttu-id="f5ad0-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="f5ad0-115">-CustomRdpProperty</span></span>
<span data-ttu-id="f5ad0-116">Benutzerdefinierte RDP-Eigenschaft von HostPool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ad0-117">-DefaultProfile</span></span>
<span data-ttu-id="f5ad0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ad0-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5ad0-119">-Description</span></span>
<span data-ttu-id="f5ad0-120">Beschreibung von HostPool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ad0-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="f5ad0-122">Name der Desktop-App-Gruppe</span><span class="sxs-lookup"><span data-stu-id="f5ad0-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="f5ad0-123">-Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="f5ad0-123">-ExpirationTime</span></span>
<span data-ttu-id="f5ad0-124">Ablaufzeit des Registrierungs Tokens.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="f5ad0-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5ad0-125">-FriendlyName</span></span>
<span data-ttu-id="f5ad0-126">Anzeigename des HostPool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="f5ad0-127">-HostPoolType</span></span>
<span data-ttu-id="f5ad0-128">HostPool-Typ für Desktop.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="f5ad0-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="f5ad0-129">-LoadBalancerType</span></span>
<span data-ttu-id="f5ad0-130">Der Typ des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="f5ad0-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5ad0-131">-Location</span></span>
<span data-ttu-id="f5ad0-132">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="f5ad0-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="f5ad0-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="f5ad0-133">-MaxSessionLimit</span></span>
<span data-ttu-id="f5ad0-134">Die maximale Sitzungs Grenze von HostPool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f5ad0-135">-Name</span></span>
<span data-ttu-id="f5ad0-136">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f5ad0-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="f5ad0-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="f5ad0-138">PersonalDesktopAssignment-Typ für HostPool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="f5ad0-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="f5ad0-140">Der Typ des bevorzugten Anwendungsgruppen Typs, standardmäßig für die Desktop Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f5ad0-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="f5ad0-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="f5ad0-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="f5ad0-142">Die Base64-codierte Zeichenfolge des Registrierungs Tokens.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="f5ad0-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="f5ad0-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="f5ad0-144">Der Typ des Zurücksetzens des Tokens.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="f5ad0-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ad0-145">-ResourceGroupName</span></span>
<span data-ttu-id="f5ad0-146">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-146">The name of the resource group.</span></span>
<span data-ttu-id="f5ad0-147">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5ad0-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="f5ad0-148">-Ring</span></span>
<span data-ttu-id="f5ad0-149">Die Nummer des HostPool-Rings.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="f5ad0-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="f5ad0-150">-SsoContext</span></span>
<span data-ttu-id="f5ad0-151">Pfad zu keyvault mit ssoContext Secret</span><span class="sxs-lookup"><span data-stu-id="f5ad0-151">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="f5ad0-152">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f5ad0-152">-SubscriptionId</span></span>
<span data-ttu-id="f5ad0-153">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f5ad0-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5ad0-154">-Tag</span></span>
<span data-ttu-id="f5ad0-155">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-155">Resource tags.</span></span>

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

### <span data-ttu-id="f5ad0-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5ad0-156">-ValidationEnvironment</span></span>
<span data-ttu-id="f5ad0-157">Ist eine Validierungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-157">Is validation environment.</span></span>

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

### <span data-ttu-id="f5ad0-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="f5ad0-158">-VMTemplate</span></span>
<span data-ttu-id="f5ad0-159">VM-Vorlage für sessionhosts-Konfiguration in hostpool.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="f5ad0-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5ad0-160">-WorkspaceName</span></span>
<span data-ttu-id="f5ad0-161">Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f5ad0-161">Workspace Name</span></span>

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

### <span data-ttu-id="f5ad0-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5ad0-162">-Confirm</span></span>
<span data-ttu-id="f5ad0-163">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ad0-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ad0-164">-WhatIf</span></span>
<span data-ttu-id="f5ad0-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ad0-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ad0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ad0-167">CommonParameters</span></span>
<span data-ttu-id="f5ad0-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ad0-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5ad0-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ad0-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5ad0-170">INPUTS</span></span>

## <span data-ttu-id="f5ad0-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5ad0-171">OUTPUTS</span></span>

### <span data-ttu-id="f5ad0-172">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="f5ad0-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="f5ad0-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5ad0-173">NOTES</span></span>

<span data-ttu-id="f5ad0-174">Aliase</span><span class="sxs-lookup"><span data-stu-id="f5ad0-174">ALIASES</span></span>

## <span data-ttu-id="f5ad0-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5ad0-175">RELATED LINKS</span></span>

