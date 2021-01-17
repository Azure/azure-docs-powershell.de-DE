---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473350"
---
# <span data-ttu-id="1b359-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b359-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="1b359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b359-102">SYNOPSIS</span></span>
<span data-ttu-id="1b359-103">Aktualisiert eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b359-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="1b359-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b359-104">SYNTAX</span></span>

### <span data-ttu-id="1b359-105">ByVpnServerConfigurationNameByCertificateAuthentication (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b359-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b359-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b359-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b359-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1b359-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b359-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b359-114">DESCRIPTION</span></span>
<span data-ttu-id="1b359-115">Mit dem Cmdlet **"Update-AzVpnServerConfiguration"** können Sie die vorhandene VpnServerConfiguration mit unterschiedlichen VpnProtocols, VpnAuthenticationTypes und IpsecPolicies aktualisieren und die parameter im Zusammenhang mit dem Vpn-Authentifizierungstyp festlegen, wie es für den Kunden für die Verbindung mit Point to Site erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1b359-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="1b359-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b359-116">EXAMPLES</span></span>

### <span data-ttu-id="1b359-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b359-117">Example 1</span></span>
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

<span data-ttu-id="1b359-118">Mit dem oben angegebenen Befehl wird eine vorhandene VpnServerConfiguration mit VpnProtocol als IkeV2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1b359-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="1b359-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b359-119">PARAMETERS</span></span>

### <span data-ttu-id="1b359-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="1b359-120">-AadAudience</span></span>
<span data-ttu-id="1b359-121">AAD-Zielgruppe für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1b359-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="1b359-122">-AadIssuer</span></span>
<span data-ttu-id="1b359-123">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="1b359-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="1b359-124">-AadTenant</span></span>
<span data-ttu-id="1b359-125">AAD-Mandant für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1b359-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b359-126">-AsJob</span></span>
<span data-ttu-id="1b359-127">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1b359-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b359-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b359-128">-DefaultProfile</span></span>
<span data-ttu-id="1b359-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b359-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b359-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b359-130">-InputObject</span></span>
<span data-ttu-id="1b359-131">Das vpn-Server-Konfigurationsobjekt, das geändert werden soll</span><span class="sxs-lookup"><span data-stu-id="1b359-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1b359-132">-Name</span></span>
<span data-ttu-id="1b359-133">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1b359-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1b359-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="1b359-135">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="1b359-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1b359-136">-RadiusServerAddress</span></span>
<span data-ttu-id="1b359-137">Serveradresse des externen Radius von P2S.</span><span class="sxs-lookup"><span data-stu-id="1b359-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="1b359-138">-RadiusServerList</span></span>
<span data-ttu-id="1b359-139">P2S Externe Server mit mehreren Radiusservern.</span><span class="sxs-lookup"><span data-stu-id="1b359-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1b359-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="1b359-141">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="1b359-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1b359-142">-RadiusServerSecret</span></span>
<span data-ttu-id="1b359-143">Geheimer Servergeheimnis des externen Radius von P2S.</span><span class="sxs-lookup"><span data-stu-id="1b359-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b359-144">-ResourceGroupName</span></span>
<span data-ttu-id="1b359-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b359-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b359-146">-ResourceId</span></span>
<span data-ttu-id="1b359-147">Die Azure-Ressourcen-ID für die Vpn-Server-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b359-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b359-148">-Tag</span></span>
<span data-ttu-id="1b359-149">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b359-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1b359-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1b359-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="1b359-151">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="1b359-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1b359-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1b359-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1b359-153">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b359-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="1b359-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1b359-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="1b359-155">Eine Liste der VpnClientCertificates, die zu widerrufenden Dateipfaden verwendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="1b359-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1b359-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="1b359-157">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="1b359-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b359-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="1b359-158">-VpnProtocol</span></span>
<span data-ttu-id="1b359-159">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="1b359-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1b359-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b359-160">-Confirm</span></span>
<span data-ttu-id="1b359-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b359-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b359-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b359-162">-WhatIf</span></span>
<span data-ttu-id="1b359-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b359-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b359-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b359-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b359-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b359-165">CommonParameters</span></span>
<span data-ttu-id="1b359-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b359-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b359-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b359-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b359-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b359-168">INPUTS</span></span>

### <span data-ttu-id="1b359-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b359-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="1b359-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="1b359-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="1b359-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b359-171">OUTPUTS</span></span>

### <span data-ttu-id="1b359-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b359-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1b359-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b359-173">NOTES</span></span>

## <span data-ttu-id="1b359-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b359-174">RELATED LINKS</span></span>
