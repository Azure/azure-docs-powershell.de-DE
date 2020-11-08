---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003417"
---
# <span data-ttu-id="205c1-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="205c1-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="205c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="205c1-102">SYNOPSIS</span></span>
<span data-ttu-id="205c1-103">Aktualisiert eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="205c1-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="205c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="205c1-104">SYNTAX</span></span>

### <span data-ttu-id="205c1-105">ByVpnServerConfigurationNameByCertificateAuthentication (Standard)</span><span class="sxs-lookup"><span data-stu-id="205c1-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205c1-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205c1-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205c1-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205c1-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205c1-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205c1-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="205c1-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205c1-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="205c1-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205c1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="205c1-114">DESCRIPTION</span></span>
<span data-ttu-id="205c1-115">Mit dem Cmdlet **Update-AzVpnServerConfiguration** können Sie die vorhandenen VpnServerConfiguration mit unterschiedlichen VpnProtocols, VpnAuthenticationTypes und IpsecPolicies aktualisieren und ausgewählte VPN-Authentifizierungstypen entsprechend den Anforderungen des Kunden für Point-to-Site-Konnektivität einstellen.</span><span class="sxs-lookup"><span data-stu-id="205c1-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="205c1-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="205c1-116">EXAMPLES</span></span>

### <span data-ttu-id="205c1-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="205c1-117">Example 1</span></span>
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

<span data-ttu-id="205c1-118">Der obige Befehl aktualisiert eine vorhandene VpnServerConfiguration mit VpnProtocol als IkeV2.</span><span class="sxs-lookup"><span data-stu-id="205c1-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="205c1-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="205c1-119">PARAMETERS</span></span>

### <span data-ttu-id="205c1-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="205c1-120">-AadAudience</span></span>
<span data-ttu-id="205c1-121">Aad-Zielgruppe für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="205c1-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="205c1-122">-AadIssuer</span></span>
<span data-ttu-id="205c1-123">Aad-Aussteller für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="205c1-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="205c1-124">-AadTenant</span></span>
<span data-ttu-id="205c1-125">Aad-Mandant für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="205c1-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="205c1-126">-AsJob</span></span>
<span data-ttu-id="205c1-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="205c1-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="205c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205c1-128">-DefaultProfile</span></span>
<span data-ttu-id="205c1-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="205c1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205c1-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="205c1-130">-InputObject</span></span>
<span data-ttu-id="205c1-131">Das zu ändernde VPN-Server-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="205c1-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-132">-Name</span><span class="sxs-lookup"><span data-stu-id="205c1-132">-Name</span></span>
<span data-ttu-id="205c1-133">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="205c1-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="205c1-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="205c1-135">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="205c1-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="205c1-136">-RadiusServerAddress</span></span>
<span data-ttu-id="205c1-137">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="205c1-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="205c1-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="205c1-139">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="205c1-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="205c1-140">-RadiusServerSecret</span></span>
<span data-ttu-id="205c1-141">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="205c1-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205c1-142">-ResourceGroupName</span></span>
<span data-ttu-id="205c1-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="205c1-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-144">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="205c1-144">-ResourceId</span></span>
<span data-ttu-id="205c1-145">Die Azure-Ressourcen-ID für die VPN-Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="205c1-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="205c1-146">-Tag</span></span>
<span data-ttu-id="205c1-147">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="205c1-147">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="205c1-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="205c1-149">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="205c1-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="205c1-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="205c1-151">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="205c1-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="205c1-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="205c1-153">Eine Liste von VpnClientCertificates-Pfaden, die von Dateien gesperrt werden sollen</span><span class="sxs-lookup"><span data-stu-id="205c1-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="205c1-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="205c1-155">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="205c1-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="205c1-156">-VpnProtocol</span></span>
<span data-ttu-id="205c1-157">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="205c1-157">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205c1-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="205c1-158">-Confirm</span></span>
<span data-ttu-id="205c1-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="205c1-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205c1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205c1-160">-WhatIf</span></span>
<span data-ttu-id="205c1-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="205c1-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205c1-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="205c1-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205c1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205c1-163">CommonParameters</span></span>
<span data-ttu-id="205c1-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205c1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205c1-165">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205c1-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205c1-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="205c1-166">INPUTS</span></span>

### <span data-ttu-id="205c1-167">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="205c1-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="205c1-168">System. String Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="205c1-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="205c1-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="205c1-169">OUTPUTS</span></span>

### <span data-ttu-id="205c1-170">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="205c1-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="205c1-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="205c1-171">NOTES</span></span>

## <span data-ttu-id="205c1-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="205c1-172">RELATED LINKS</span></span>
