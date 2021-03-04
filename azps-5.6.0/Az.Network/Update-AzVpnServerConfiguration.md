---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918336"
---
# <span data-ttu-id="0da81-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da81-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0da81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da81-102">SYNOPSIS</span></span>
<span data-ttu-id="0da81-103">Aktualisiert eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0da81-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0da81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0da81-104">SYNTAX</span></span>

### <span data-ttu-id="0da81-105">ByVpnServerConfigurationName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0da81-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0da81-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0da81-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0da81-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="0da81-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0da81-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0da81-108">DESCRIPTION</span></span>
<span data-ttu-id="0da81-109">Mit dem **Update-AzVpnServerConfiguration-Cmdlet** können Sie die vorhandene VpnServerConfiguration mit unterschiedlichen VpnProtocols, VpnAuthenticationTypes, IpsecPolicies aktualisieren und ausgewählte Parameter für den Vpn-Authentifizierungstyp nach den Anforderungen des Kunden an die Konnektivität von Punkt auf Website festlegen.</span><span class="sxs-lookup"><span data-stu-id="0da81-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="0da81-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0da81-110">EXAMPLES</span></span>

### <span data-ttu-id="0da81-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0da81-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="0da81-112">Der obige Befehl aktualisiert eine vorhandene VpnServerConfiguration mit VpnProtocol als IkeV2.</span><span class="sxs-lookup"><span data-stu-id="0da81-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="0da81-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0da81-113">PARAMETERS</span></span>

### <span data-ttu-id="0da81-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="0da81-114">-AadAudience</span></span>
<span data-ttu-id="0da81-115">AAD-Benutzer für die P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0da81-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="0da81-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="0da81-116">-AadIssuer</span></span>
<span data-ttu-id="0da81-117">AAD-Aussteller für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0da81-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="0da81-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="0da81-118">-AadTenant</span></span>
<span data-ttu-id="0da81-119">AAD-Mandant für P2S AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0da81-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="0da81-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0da81-120">-AsJob</span></span>
<span data-ttu-id="0da81-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0da81-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0da81-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da81-122">-DefaultProfile</span></span>
<span data-ttu-id="0da81-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0da81-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da81-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0da81-124">-InputObject</span></span>
<span data-ttu-id="0da81-125">Das zu ändernde Vpnserverkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="0da81-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0da81-126">-Name</span></span>
<span data-ttu-id="0da81-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0da81-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0da81-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="0da81-129">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="0da81-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="0da81-130">-RadiusServerAddress</span></span>
<span data-ttu-id="0da81-131">P2S-Serveradresse für externen Radius.</span><span class="sxs-lookup"><span data-stu-id="0da81-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="0da81-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="0da81-132">-RadiusServerList</span></span>
<span data-ttu-id="0da81-133">P2S Externe Server mit mehreren Radius.</span><span class="sxs-lookup"><span data-stu-id="0da81-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0da81-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="0da81-135">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="0da81-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="0da81-136">-RadiusServerSecret</span></span>
<span data-ttu-id="0da81-137">P2S External Radius server secret.</span><span class="sxs-lookup"><span data-stu-id="0da81-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da81-138">-ResourceGroupName</span></span>
<span data-ttu-id="0da81-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0da81-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0da81-140">-ResourceId</span></span>
<span data-ttu-id="0da81-141">Die Azure-Ressourcen-ID für die Vpnserverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0da81-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0da81-142">-Tag</span></span>
<span data-ttu-id="0da81-143">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0da81-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0da81-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0da81-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="0da81-145">Die Liste der P2S-VPN-Client-Tunnelprotokolle.</span><span class="sxs-lookup"><span data-stu-id="0da81-145">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0da81-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="0da81-147">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0da81-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0da81-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="0da81-149">Eine Liste der VpnClientCertificates zum Widerrufen der Pfade von Dateien</span><span class="sxs-lookup"><span data-stu-id="0da81-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0da81-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="0da81-151">Eine Liste von VpnClientRootCertificates zum Hinzufügen von Dateipfaden</span><span class="sxs-lookup"><span data-stu-id="0da81-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="0da81-152">-VpnProtocol</span></span>
<span data-ttu-id="0da81-153">Die Liste der P2S-VPN-Client-Tunnelprotokolle.</span><span class="sxs-lookup"><span data-stu-id="0da81-153">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0da81-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0da81-154">-Confirm</span></span>
<span data-ttu-id="0da81-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0da81-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da81-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da81-156">-WhatIf</span></span>
<span data-ttu-id="0da81-157">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0da81-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da81-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0da81-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da81-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da81-159">CommonParameters</span></span>
<span data-ttu-id="0da81-160">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da81-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da81-161">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da81-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da81-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0da81-162">INPUTS</span></span>

### <span data-ttu-id="0da81-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da81-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="0da81-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="0da81-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="0da81-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0da81-165">OUTPUTS</span></span>

### <span data-ttu-id="0da81-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da81-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="0da81-167">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0da81-167">NOTES</span></span>

## <span data-ttu-id="0da81-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0da81-168">RELATED LINKS</span></span>
