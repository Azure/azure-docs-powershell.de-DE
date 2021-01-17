---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378929"
---
# <span data-ttu-id="a8a11-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8a11-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a8a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a11-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a11-103">Erstellen Sie eine neue VpnServerConfiguration für die Punkt-zu-Website-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="a8a11-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="a8a11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8a11-104">SYNTAX</span></span>

### <span data-ttu-id="a8a11-105">ByVpnServerConfigurationNameByCertificateAuthentication (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8a11-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8a11-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8a11-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8a11-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8a11-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8a11-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8a11-108">DESCRIPTION</span></span>
<span data-ttu-id="a8a11-109">Mit dem Cmdlet **"New-AzVpnServerConfiguration"** können Sie eine neue VpnServerConfiguration mit unterschiedlichen VpnProtocols, VpnAuthenticationTypes und IpsecPolicies erstellen und ausgewählte Parameter für den Vpn-Authentifizierungstyp so festlegen, dass die Konnektivität mit "Verweisen auf" des Kunden erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a8a11-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a8a11-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8a11-110">EXAMPLES</span></span>

### <span data-ttu-id="a8a11-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8a11-111">Example 1</span></span>
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

<span data-ttu-id="a8a11-112">Mit dem oben angegebenen Befehl wird eine neue VpnServerConfiguration mit VpnAuthenticationType als Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="a8a11-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="a8a11-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8a11-113">Example 2</span></span>

<span data-ttu-id="a8a11-114">Erstellen Sie eine neue VpnServerConfiguration für die Punkt-zu-Website-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="a8a11-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="a8a11-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="a8a11-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="a8a11-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8a11-116">PARAMETERS</span></span>

### <span data-ttu-id="a8a11-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a8a11-117">-AadAudience</span></span>
<span data-ttu-id="a8a11-118">AAD-Zielgruppe für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a8a11-118">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a8a11-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a8a11-119">-AadIssuer</span></span>
<span data-ttu-id="a8a11-120">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="a8a11-120">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a8a11-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a8a11-121">-AadTenant</span></span>
<span data-ttu-id="a8a11-122">AAD-Mandant für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="a8a11-122">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="a8a11-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8a11-123">-AsJob</span></span>
<span data-ttu-id="a8a11-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a8a11-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8a11-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a11-125">-DefaultProfile</span></span>
<span data-ttu-id="a8a11-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8a11-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8a11-127">-Location</span><span class="sxs-lookup"><span data-stu-id="a8a11-127">-Location</span></span>
<span data-ttu-id="a8a11-128">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="a8a11-128">The resource location.</span></span>

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

### <span data-ttu-id="a8a11-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a8a11-129">-Name</span></span>
<span data-ttu-id="a8a11-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a8a11-130">The resource name.</span></span>

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

### <span data-ttu-id="a8a11-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8a11-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a8a11-132">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8a11-132">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="a8a11-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a8a11-133">-RadiusServerAddress</span></span>
<span data-ttu-id="a8a11-134">Serveradresse des externen Radius von P2S.</span><span class="sxs-lookup"><span data-stu-id="a8a11-134">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="a8a11-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="a8a11-135">-RadiusServerList</span></span>
<span data-ttu-id="a8a11-136">P2S External multiple radius servers.</span><span class="sxs-lookup"><span data-stu-id="a8a11-136">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="a8a11-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8a11-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a8a11-138">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="a8a11-138">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="a8a11-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a8a11-139">-RadiusServerSecret</span></span>
<span data-ttu-id="a8a11-140">Geheimer Servergeheimnis des externen P2S-Radius.</span><span class="sxs-lookup"><span data-stu-id="a8a11-140">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="a8a11-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a11-141">-ResourceGroupName</span></span>
<span data-ttu-id="a8a11-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8a11-142">The resource group name.</span></span>

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

### <span data-ttu-id="a8a11-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8a11-143">-Tag</span></span>
<span data-ttu-id="a8a11-144">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8a11-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a8a11-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a8a11-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="a8a11-146">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="a8a11-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a8a11-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a8a11-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a8a11-148">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a8a11-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="a8a11-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8a11-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a8a11-150">Eine Liste der VpnClientCertificates, die zu widerrufenden Dateipfaden verwendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a8a11-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="a8a11-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8a11-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a8a11-152">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="a8a11-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="a8a11-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a8a11-153">-VpnProtocol</span></span>
<span data-ttu-id="a8a11-154">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="a8a11-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a8a11-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8a11-155">-Confirm</span></span>
<span data-ttu-id="a8a11-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8a11-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a11-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a8a11-157">-WhatIf</span></span>
<span data-ttu-id="a8a11-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8a11-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8a11-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8a11-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a11-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a11-160">CommonParameters</span></span>
<span data-ttu-id="a8a11-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a11-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a11-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8a11-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a11-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8a11-163">INPUTS</span></span>

### <span data-ttu-id="a8a11-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="a8a11-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a8a11-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8a11-165">OUTPUTS</span></span>

### <span data-ttu-id="a8a11-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8a11-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a8a11-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a8a11-167">NOTES</span></span>

## <span data-ttu-id="a8a11-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a8a11-168">RELATED LINKS</span></span>
