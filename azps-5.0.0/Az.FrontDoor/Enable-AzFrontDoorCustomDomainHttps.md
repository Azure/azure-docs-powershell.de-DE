---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179269"
---
# <span data-ttu-id="3a39a-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="3a39a-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="3a39a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a39a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a39a-103">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit verwaltetem Haustür Zertifikat oder mithilfe eines eigenen Zertifikats aus dem Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3a39a-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="3a39a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a39a-104">SYNTAX</span></span>

### <span data-ttu-id="3a39a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a39a-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a39a-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a39a-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a39a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a39a-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a39a-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a39a-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a39a-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a39a-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a39a-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a39a-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a39a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a39a-111">DESCRIPTION</span></span>
<span data-ttu-id="3a39a-112">Die **enable-AzFrontDoorCustomDomainHttps-** Funktion ermöglicht HTTPS für eine benutzerdefinierte Domäne.</span><span class="sxs-lookup"><span data-stu-id="3a39a-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="3a39a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a39a-113">EXAMPLES</span></span>

### <span data-ttu-id="3a39a-114">Beispiel 1: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit FrontDoorName und ResourceGroupName unter Verwendung eines von der Haustür verwalteten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3a39a-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="3a39a-115">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-Benutzerdefiniert-XYZ", die Teil der Haustür "frontdoor1" in der Ressourcengruppe "resourcegroup1" ist, die das von der Haustür verwaltete Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a39a-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="3a39a-116">Beispiel 2: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit FrontDoorName und ResourceGroupName mithilfe des eigenen Zertifikats in Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3a39a-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="3a39a-117">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-Benutzerdefiniert-XYZ", die Teil der Haustür "frontdoor1" in der Ressourcengruppe "resourcegroup1" ist, die das von der Haustür verwaltete Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a39a-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="3a39a-118">Beispiel 3: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit einem PSFrontendEndpoint-Objekt mit verwaltetem Haustür Zertifikat</span><span class="sxs-lookup"><span data-stu-id="3a39a-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="3a39a-119">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne mit einem PSFrontendEndpoint-Objekt, das ein von der Haustür verwaltetes Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a39a-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="3a39a-120">Beispiel 4: Aktivieren von HTTPS für eine benutzerdefinierte Domäne mit Ressourcen-ID mit verwaltetem Haustür Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="3a39a-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="3a39a-121">Aktivieren Sie HTTPS für eine benutzerdefinierte Domäne "frontendpointname1-Benutzerdefiniert-XYZ" mit der Ressourcen-ID $ResourceId mit verwaltetem Haustür Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="3a39a-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="3a39a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a39a-122">PARAMETERS</span></span>

### <span data-ttu-id="3a39a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a39a-123">-DefaultProfile</span></span>
<span data-ttu-id="3a39a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a39a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a39a-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3a39a-125">-FrontDoorName</span></span>
<span data-ttu-id="3a39a-126">Der Name der Haustür.</span><span class="sxs-lookup"><span data-stu-id="3a39a-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="3a39a-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="3a39a-127">-FrontendEndpointName</span></span>
<span data-ttu-id="3a39a-128">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="3a39a-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="3a39a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a39a-129">-InputObject</span></span>
<span data-ttu-id="3a39a-130">Das zu aktualisierbare Frontend-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a39a-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="3a39a-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3a39a-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="3a39a-132">Die für die Clients erforderliche minimale TLS-Version, um einen SSL-Handshake mit Haustür einzurichten.</span><span class="sxs-lookup"><span data-stu-id="3a39a-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="3a39a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a39a-133">-ResourceGroupName</span></span>
<span data-ttu-id="3a39a-134">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="3a39a-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="3a39a-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a39a-135">-ResourceId</span></span>
<span data-ttu-id="3a39a-136">Ressourcen-ID des Front-Door-Endpunkts zum Aktivieren von HTTPS</span><span class="sxs-lookup"><span data-stu-id="3a39a-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="3a39a-137">-Secretname</span><span class="sxs-lookup"><span data-stu-id="3a39a-137">-SecretName</span></span>
<span data-ttu-id="3a39a-138">Der Name des Schlüssel Tresors, der die vollständige Zertifikat-PFX-Datei darstellt</span><span class="sxs-lookup"><span data-stu-id="3a39a-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="3a39a-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="3a39a-139">-SecretVersion</span></span>
<span data-ttu-id="3a39a-140">Die Version des Schlüssels Vault Secret, die das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="3a39a-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="3a39a-141">-Tresor</span><span class="sxs-lookup"><span data-stu-id="3a39a-141">-VaultId</span></span>
<span data-ttu-id="3a39a-142">Die schlüsseltresor-ID mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="3a39a-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="3a39a-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a39a-143">-Confirm</span></span>
<span data-ttu-id="3a39a-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a39a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a39a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a39a-145">-WhatIf</span></span>
<span data-ttu-id="3a39a-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a39a-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a39a-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a39a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a39a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a39a-148">CommonParameters</span></span>
<span data-ttu-id="3a39a-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a39a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a39a-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a39a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a39a-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a39a-151">INPUTS</span></span>

### <span data-ttu-id="3a39a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3a39a-152">System.String</span></span>
## <span data-ttu-id="3a39a-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a39a-153">OUTPUTS</span></span>

### <span data-ttu-id="3a39a-154">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a39a-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="3a39a-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a39a-155">NOTES</span></span>

## <span data-ttu-id="3a39a-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a39a-156">RELATED LINKS</span></span>
