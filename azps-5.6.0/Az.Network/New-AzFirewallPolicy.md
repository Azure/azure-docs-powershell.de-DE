---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 3e60546992957a027dd5bbb94281e19e74e42274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930960"
---
# <span data-ttu-id="f0ba8-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f0ba8-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="f0ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ba8-103">Erstellt eine neue Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f0ba8-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="f0ba8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0ba8-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0ba8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ba8-106">Das **Cmdlet New-AzFirewallPolicy** erstellt eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f0ba8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ba8-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-108">Example 1: 1.</span></span> <span data-ttu-id="f0ba8-109">Erstellen einer leeren Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f0ba8-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="f0ba8-110">In diesem Beispiel wird eine Azure-Firewallrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="f0ba8-111">Beispiel 2: 2.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-111">Example 2: 2.</span></span> <span data-ttu-id="f0ba8-112">Erstellen einer leeren Richtlinie mit dem ThreatIntel-Modus</span><span class="sxs-lookup"><span data-stu-id="f0ba8-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="f0ba8-113">In diesem Beispiel wird eine Azure-Firewallrichtlinie mit einem Intel-Bedrohungsmodus erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="f0ba8-114">Beispiel 3: 3.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-114">Example 3: 3.</span></span> <span data-ttu-id="f0ba8-115">Erstellen einer leeren Richtlinie mit ThreatIntel Whitelist</span><span class="sxs-lookup"><span data-stu-id="f0ba8-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="f0ba8-116">In diesem Beispiel wird eine Azure-Firewallrichtlinie mit einer Intel Whitelist für Bedrohungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="f0ba8-117">Beispiel 4: 4.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-117">Example 4: 4.</span></span> <span data-ttu-id="f0ba8-118">Erstellen einer Richtlinie mit Erkennung von Eindringversuchen, Identitäts- und Transportsicherheit</span><span class="sxs-lookup"><span data-stu-id="f0ba8-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="f0ba8-119">In diesem Beispiel wird eine Azure-Firewallrichtlinie mit einer Warnung zur Erkennung von Eindringversuchen im Modus, vom Benutzer zugewiesener Identität und Transportsicherheit erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="f0ba8-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0ba8-120">PARAMETERS</span></span>

### <span data-ttu-id="f0ba8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0ba8-121">-AsJob</span></span>
<span data-ttu-id="f0ba8-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0ba8-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="f0ba8-123">-BasePolicy</span></span>
<span data-ttu-id="f0ba8-124">Die Basisrichtlinie, von der geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="f0ba8-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ba8-125">-DefaultProfile</span></span>
<span data-ttu-id="f0ba8-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f0ba8-127">-DnsSetting</span></span>
<span data-ttu-id="f0ba8-128">Die DNS-Einstellung</span><span class="sxs-lookup"><span data-stu-id="f0ba8-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-129">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f0ba8-129">-Force</span></span>
<span data-ttu-id="f0ba8-130">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="f0ba8-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-131">-Identity</span><span class="sxs-lookup"><span data-stu-id="f0ba8-131">-Identity</span></span>
<span data-ttu-id="f0ba8-132">Firewallrichtlinienidentität, die der Firewallrichtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="f0ba8-133">-IntrusionDetection</span></span>
<span data-ttu-id="f0ba8-134">Einstellung zur Erkennung von Eindringversuchen</span><span class="sxs-lookup"><span data-stu-id="f0ba8-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-135">-Location</span><span class="sxs-lookup"><span data-stu-id="f0ba8-135">-Location</span></span>
<span data-ttu-id="f0ba8-136">speicherort.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f0ba8-137">-Name</span></span>
<span data-ttu-id="f0ba8-138">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ba8-139">-ResourceGroupName</span></span>
<span data-ttu-id="f0ba8-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f0ba8-141">-SkuTier</span></span>
<span data-ttu-id="f0ba8-142">Sku-Ebene der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="f0ba8-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0ba8-143">-Tag</span></span>
<span data-ttu-id="f0ba8-144">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f0ba8-145">-ThreatIntelMode</span></span>
<span data-ttu-id="f0ba8-146">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f0ba8-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f0ba8-148">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="f0ba8-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="f0ba8-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="f0ba8-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span><span class="sxs-lookup"><span data-stu-id="f0ba8-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="f0ba8-151">-TransportSecurityName</span></span>
<span data-ttu-id="f0ba8-152">Name der Transportsicherheit</span><span class="sxs-lookup"><span data-stu-id="f0ba8-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f0ba8-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f0ba8-154">ResourceId des Benutzers, dem die Identität zugewiesen wurde, die der Firewallrichtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0ba8-155">-Confirm</span></span>
<span data-ttu-id="f0ba8-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ba8-157">-WhatIf</span></span>
<span data-ttu-id="f0ba8-158">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ba8-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ba8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ba8-160">CommonParameters</span></span>
<span data-ttu-id="f0ba8-161">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ba8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ba8-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0ba8-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ba8-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0ba8-163">INPUTS</span></span>

### <span data-ttu-id="f0ba8-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f0ba8-164">System.String</span></span>

### <span data-ttu-id="f0ba8-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0ba8-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0ba8-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0ba8-166">OUTPUTS</span></span>

### <span data-ttu-id="f0ba8-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f0ba8-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f0ba8-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0ba8-168">NOTES</span></span>

## <span data-ttu-id="f0ba8-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0ba8-169">RELATED LINKS</span></span>
