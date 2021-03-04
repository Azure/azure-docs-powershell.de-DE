---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: cb5986d7e8d467c76b64baddb5fd389eda1b5b8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949435"
---
# <span data-ttu-id="187d5-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="187d5-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="187d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187d5-102">SYNOPSIS</span></span>
<span data-ttu-id="187d5-103">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne mithilfe eines von Front Door verwalteten Zertifikats oder mithilfe eines eigenen Zertifikats aus dem Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="187d5-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="187d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="187d5-104">SYNTAX</span></span>

### <span data-ttu-id="187d5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="187d5-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187d5-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d5-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="187d5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d5-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187d5-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d5-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187d5-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d5-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187d5-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="187d5-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187d5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="187d5-111">DESCRIPTION</span></span>
<span data-ttu-id="187d5-112">Die **Enable-AzFrontDoorCustomDomainHttps** aktiviert HTTPS für eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="187d5-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="187d5-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="187d5-113">EXAMPLES</span></span>

### <span data-ttu-id="187d5-114">Beispiel 1: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit FrontDoorName und ResourceGroupName mithilfe des verwalteten Front Door-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="187d5-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="187d5-115">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-custom-xyz", die teil von Front Door "frontdoor1" in der Ressourcengruppe "resourcegroup1" mit einem verwalteten Front Door-Zertifikat ist.</span><span class="sxs-lookup"><span data-stu-id="187d5-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="187d5-116">Beispiel 2: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit FrontDoorName und ResourceGroupName mithilfe eines eigenen Zertifikats im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="187d5-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="187d5-117">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-custom-xyz", die teil von Front Door "frontdoor1" in der Ressourcengruppe "resourcegroup1" mit einem verwalteten Front Door-Zertifikat ist.</span><span class="sxs-lookup"><span data-stu-id="187d5-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="187d5-118">Beispiel 3: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit PSFrontendEndpoint-Objekt mithilfe des verwalteten Front Door-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="187d5-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="187d5-119">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit PSFrontendEndpoint-Objekt mithilfe des verwalteten Front Door-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="187d5-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="187d5-120">Beispiel 4: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit Ressourcen-ID mithilfe des verwalteten Zertifikats von Front Door.</span><span class="sxs-lookup"><span data-stu-id="187d5-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="187d5-121">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-custom-xyz" mit Ressourcen-ID$resourceId das verwaltete Zertifikat von Front Door verwendet.</span><span class="sxs-lookup"><span data-stu-id="187d5-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="187d5-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="187d5-122">PARAMETERS</span></span>

### <span data-ttu-id="187d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187d5-123">-DefaultProfile</span></span>
<span data-ttu-id="187d5-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="187d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="187d5-125">-FrontDoorName</span></span>
<span data-ttu-id="187d5-126">Der Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="187d5-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="187d5-127">-FrontendEndpointName</span></span>
<span data-ttu-id="187d5-128">Name des Frontend-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="187d5-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="187d5-129">-InputObject</span></span>
<span data-ttu-id="187d5-130">Das zu aktualisierende Frontend-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="187d5-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="187d5-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="187d5-132">Die mindeste TLS-Version, die von den Clients benötigt wird, um einen SSL-Handshake mit Front Door zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="187d5-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="187d5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187d5-133">-ResourceGroupName</span></span>
<span data-ttu-id="187d5-134">Die Ressourcengruppe, zu der die Eingangstür gehört.</span><span class="sxs-lookup"><span data-stu-id="187d5-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="187d5-135">-ResourceId</span></span>
<span data-ttu-id="187d5-136">Ressourcen-ID des Endpunkts "Eingangstür", um https zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="187d5-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="187d5-137">-SecretName</span></span>
<span data-ttu-id="187d5-138">Der Name des Schlüsseltresorschlüssels, der das vollständige ZERTIFIKAT PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="187d5-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="187d5-139">-SecretVersion</span></span>
<span data-ttu-id="187d5-140">Die Version des Schlüsseltresorschlüssels, der das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="187d5-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="187d5-141">-VaultId</span></span>
<span data-ttu-id="187d5-142">Die Schlüsseltresor-ID, die das SSL-Zertifikat enthält</span><span class="sxs-lookup"><span data-stu-id="187d5-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187d5-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="187d5-143">-Confirm</span></span>
<span data-ttu-id="187d5-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="187d5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187d5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187d5-145">-WhatIf</span></span>
<span data-ttu-id="187d5-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="187d5-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="187d5-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="187d5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187d5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187d5-148">CommonParameters</span></span>
<span data-ttu-id="187d5-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187d5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187d5-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="187d5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187d5-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="187d5-151">INPUTS</span></span>

### <span data-ttu-id="187d5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="187d5-152">System.String</span></span>
## <span data-ttu-id="187d5-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="187d5-153">OUTPUTS</span></span>

### <span data-ttu-id="187d5-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="187d5-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="187d5-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="187d5-155">NOTES</span></span>

## <span data-ttu-id="187d5-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="187d5-156">RELATED LINKS</span></span>
