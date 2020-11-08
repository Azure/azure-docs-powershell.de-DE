---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179851"
---
# <span data-ttu-id="03c98-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c98-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="03c98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03c98-102">SYNOPSIS</span></span>
<span data-ttu-id="03c98-103">Erstellen Sie ein neues VpnServerConfiguration für Point-to-Site-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="03c98-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="03c98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03c98-104">SYNTAX</span></span>

### <span data-ttu-id="03c98-105">ByVpnServerConfigurationNameByCertificateAuthentication (Standard)</span><span class="sxs-lookup"><span data-stu-id="03c98-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c98-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="03c98-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c98-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="03c98-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c98-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03c98-108">DESCRIPTION</span></span>
<span data-ttu-id="03c98-109">Mit dem Cmdlet **New-AzVpnServerConfiguration** können Sie ein neues VpnServerConfiguration mit unterschiedlichen VpnProtocols-, VpnAuthenticationTypes-, IpsecPolicies-und ausgewählten VPN-Authentifizierungstypen entsprechend den Anforderungen des Kunden für Point-to-Site-Konnektivität erstellen.</span><span class="sxs-lookup"><span data-stu-id="03c98-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="03c98-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03c98-110">EXAMPLES</span></span>

### <span data-ttu-id="03c98-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03c98-111">Example 1</span></span>
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

<span data-ttu-id="03c98-112">Mit dem obigen Befehl wird eine neue VpnServerConfiguration mit VpnAuthenticationType als Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="03c98-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="03c98-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="03c98-113">Example 2</span></span>

<span data-ttu-id="03c98-114">Erstellen Sie ein neues VpnServerConfiguration für Point-to-Site-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="03c98-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="03c98-115">automatisch</span><span class="sxs-lookup"><span data-stu-id="03c98-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="03c98-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="03c98-116">PARAMETERS</span></span>

### <span data-ttu-id="03c98-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="03c98-117">-AadAudience</span></span>
<span data-ttu-id="03c98-118">Aad-Zielgruppe für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="03c98-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="03c98-119">-AadIssuer</span></span>
<span data-ttu-id="03c98-120">Aad-Aussteller für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="03c98-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="03c98-121">-AadTenant</span></span>
<span data-ttu-id="03c98-122">Aad-Mandant für P2S Aad-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="03c98-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c98-123">-AsJob</span></span>
<span data-ttu-id="03c98-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="03c98-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03c98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c98-125">-DefaultProfile</span></span>
<span data-ttu-id="03c98-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03c98-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c98-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="03c98-127">-Location</span></span>
<span data-ttu-id="03c98-128">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="03c98-128">The resource location.</span></span>

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

### <span data-ttu-id="03c98-129">-Name</span><span class="sxs-lookup"><span data-stu-id="03c98-129">-Name</span></span>
<span data-ttu-id="03c98-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="03c98-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03c98-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="03c98-132">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="03c98-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="03c98-133">-RadiusServerAddress</span></span>
<span data-ttu-id="03c98-134">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="03c98-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="03c98-135">-RadiusServerList</span></span>
<span data-ttu-id="03c98-136">P2S externer mehrerer RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="03c98-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03c98-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="03c98-138">Eine Liste der Pfade von RadiusClientRootCertificate-Dateien</span><span class="sxs-lookup"><span data-stu-id="03c98-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="03c98-139">-RadiusServerSecret</span></span>
<span data-ttu-id="03c98-140">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="03c98-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c98-141">-ResourceGroupName</span></span>
<span data-ttu-id="03c98-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03c98-142">The resource group name.</span></span>

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

### <span data-ttu-id="03c98-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="03c98-143">-Tag</span></span>
<span data-ttu-id="03c98-144">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="03c98-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="03c98-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="03c98-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="03c98-146">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="03c98-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="03c98-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="03c98-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="03c98-148">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="03c98-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03c98-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="03c98-150">Eine Liste von VpnClientCertificates-Pfaden, die von Dateien gesperrt werden sollen</span><span class="sxs-lookup"><span data-stu-id="03c98-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03c98-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="03c98-152">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="03c98-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c98-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="03c98-153">-VpnProtocol</span></span>
<span data-ttu-id="03c98-154">Die Liste der P2S-VPN-Client Tunneling-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="03c98-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="03c98-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03c98-155">-Confirm</span></span>
<span data-ttu-id="03c98-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03c98-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c98-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c98-157">-WhatIf</span></span>
<span data-ttu-id="03c98-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03c98-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c98-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03c98-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c98-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c98-160">CommonParameters</span></span>
<span data-ttu-id="03c98-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c98-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c98-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03c98-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c98-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03c98-163">INPUTS</span></span>

### <span data-ttu-id="03c98-164">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="03c98-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="03c98-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03c98-165">OUTPUTS</span></span>

### <span data-ttu-id="03c98-166">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c98-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="03c98-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="03c98-167">NOTES</span></span>

## <span data-ttu-id="03c98-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03c98-168">RELATED LINKS</span></span>
