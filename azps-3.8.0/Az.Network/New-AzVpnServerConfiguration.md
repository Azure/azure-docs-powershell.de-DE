---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846699"
---
# <span data-ttu-id="a52de-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52de-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a52de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a52de-102">SYNOPSIS</span></span>
<span data-ttu-id="a52de-103">Erstellen Sie ein neues VpnServerConfiguration für Point-to-Site-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="a52de-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="a52de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a52de-104">SYNTAX</span></span>

### <span data-ttu-id="a52de-105">ByVpnServerConfigurationNameByCertificateAuthentication (Standard)</span><span class="sxs-lookup"><span data-stu-id="a52de-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a52de-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a52de-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a52de-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a52de-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a52de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a52de-108">DESCRIPTION</span></span>
<span data-ttu-id="a52de-109">Mit dem Cmdlet **New-AzVpnServerConfiguration** können Sie ein neues VpnServerConfiguration mit unterschiedlichen VpnProtocols-, VpnAuthenticationTypes-, IpsecPolicies-und ausgewählten VPN-Authentifizierungstypen entsprechend den Anforderungen des Kunden für Point-to-Site-Konnektivität erstellen.</span><span class="sxs-lookup"><span data-stu-id="a52de-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a52de-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a52de-110">EXAMPLES</span></span>

### <span data-ttu-id="a52de-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a52de-111">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="a52de-112">Mit dem obigen Befehl wird eine neue VpnServerConfiguration mit VpnAuthenticationType als Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="a52de-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="a52de-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a52de-113">PARAMETERS</span></span>

### <span data-ttu-id="a52de-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a52de-114">-AadAudience</span></span>
<span data-ttu-id="a52de-115">Aad-Zielgruppe für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a52de-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a52de-116">-AadIssuer</span></span>
<span data-ttu-id="a52de-117">Aad-Aussteller für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a52de-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a52de-118">-AadTenant</span></span>
<span data-ttu-id="a52de-119">Aad-Mandant für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a52de-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a52de-120">-AsJob</span></span>
<span data-ttu-id="a52de-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a52de-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a52de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52de-122">-DefaultProfile</span></span>
<span data-ttu-id="a52de-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a52de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52de-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="a52de-124">-Location</span></span>
<span data-ttu-id="a52de-125">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a52de-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a52de-126">-Name</span></span>
<span data-ttu-id="a52de-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a52de-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a52de-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a52de-129">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="a52de-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a52de-130">-RadiusServerAddress</span></span>
<span data-ttu-id="a52de-131">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="a52de-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a52de-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a52de-133">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="a52de-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a52de-134">-RadiusServerSecret</span></span>
<span data-ttu-id="a52de-135">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a52de-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52de-136">-ResourceGroupName</span></span>
<span data-ttu-id="a52de-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a52de-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="a52de-138">-Tag</span></span>
<span data-ttu-id="a52de-139">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a52de-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a52de-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a52de-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="a52de-141">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="a52de-141">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a52de-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a52de-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a52de-143">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a52de-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a52de-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a52de-145">Eine Liste von VpnClientCertificates-Pfaden, die von Dateien gesperrt werden sollen</span><span class="sxs-lookup"><span data-stu-id="a52de-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a52de-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a52de-147">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="a52de-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52de-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a52de-148">-VpnProtocol</span></span>
<span data-ttu-id="a52de-149">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="a52de-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a52de-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a52de-150">-Confirm</span></span>
<span data-ttu-id="a52de-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a52de-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52de-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52de-152">-WhatIf</span></span>
<span data-ttu-id="a52de-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a52de-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52de-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a52de-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52de-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52de-155">CommonParameters</span></span>
<span data-ttu-id="a52de-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52de-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52de-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52de-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52de-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a52de-158">INPUTS</span></span>

### <span data-ttu-id="a52de-159">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a52de-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a52de-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a52de-160">OUTPUTS</span></span>

### <span data-ttu-id="a52de-161">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a52de-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a52de-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="a52de-162">NOTES</span></span>

## <span data-ttu-id="a52de-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a52de-163">RELATED LINKS</span></span>
