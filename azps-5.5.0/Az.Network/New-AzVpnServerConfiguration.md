---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169758"
---
# <span data-ttu-id="13ef6-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="13ef6-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="13ef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="13ef6-103">Erstellen Sie eine neue VpnServerConfiguration für die Punkt-zu-Website-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="13ef6-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="13ef6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13ef6-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13ef6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="13ef6-106">Mit dem Cmdlet **"New-AzVpnServerConfiguration"** können Sie eine neue VpnServerConfiguration mit unterschiedlichen VpnProtocols, VpnAuthenticationTypes und IpsecPolicies erstellen und ausgewählte Parameter für den Vpn-Authentifizierungstyp festlegen, wie es für die Konnektivität mit Point to Site durch den Kunden erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="13ef6-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="13ef6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="13ef6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13ef6-108">Example 1</span></span>
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

<span data-ttu-id="13ef6-109">Mit dem oben angegebenen Befehl wird eine neue VpnServerConfiguration mit VpnAuthenticationType als Zertifikat erstellt.</span><span class="sxs-lookup"><span data-stu-id="13ef6-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="13ef6-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="13ef6-110">Example 2</span></span>

<span data-ttu-id="13ef6-111">Erstellen Sie eine neue VpnServerConfiguration für die Punkt-zu-Website-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="13ef6-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="13ef6-112">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="13ef6-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="13ef6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13ef6-113">PARAMETERS</span></span>

### <span data-ttu-id="13ef6-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="13ef6-114">-AadAudience</span></span>
<span data-ttu-id="13ef6-115">AAD-Zielgruppe für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="13ef6-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="13ef6-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="13ef6-116">-AadIssuer</span></span>
<span data-ttu-id="13ef6-117">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="13ef6-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="13ef6-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="13ef6-118">-AadTenant</span></span>
<span data-ttu-id="13ef6-119">AAD-Mandant für P2S-AAD-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="13ef6-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="13ef6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13ef6-120">-AsJob</span></span>
<span data-ttu-id="13ef6-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="13ef6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13ef6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ef6-122">-DefaultProfile</span></span>
<span data-ttu-id="13ef6-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13ef6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ef6-124">-Location</span><span class="sxs-lookup"><span data-stu-id="13ef6-124">-Location</span></span>
<span data-ttu-id="13ef6-125">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="13ef6-125">The resource location.</span></span>

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

### <span data-ttu-id="13ef6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="13ef6-126">-Name</span></span>
<span data-ttu-id="13ef6-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="13ef6-127">The resource name.</span></span>

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

### <span data-ttu-id="13ef6-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="13ef6-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="13ef6-129">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="13ef6-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="13ef6-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="13ef6-130">-RadiusServerAddress</span></span>
<span data-ttu-id="13ef6-131">Serveradresse des externen Radius von P2S.</span><span class="sxs-lookup"><span data-stu-id="13ef6-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="13ef6-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="13ef6-132">-RadiusServerList</span></span>
<span data-ttu-id="13ef6-133">P2S External multiple radius servers.</span><span class="sxs-lookup"><span data-stu-id="13ef6-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="13ef6-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="13ef6-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="13ef6-135">Eine Liste der Pfade von "RadiusClientRootCertificate"-Dateien</span><span class="sxs-lookup"><span data-stu-id="13ef6-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="13ef6-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="13ef6-136">-RadiusServerSecret</span></span>
<span data-ttu-id="13ef6-137">Geheimer Servergeheimnis des externen P2S-Radius.</span><span class="sxs-lookup"><span data-stu-id="13ef6-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="13ef6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ef6-138">-ResourceGroupName</span></span>
<span data-ttu-id="13ef6-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13ef6-139">The resource group name.</span></span>

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

### <span data-ttu-id="13ef6-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="13ef6-140">-Tag</span></span>
<span data-ttu-id="13ef6-141">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="13ef6-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="13ef6-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="13ef6-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="13ef6-143">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="13ef6-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="13ef6-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="13ef6-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="13ef6-145">Eine Liste der IPSec-Richtlinien für VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="13ef6-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="13ef6-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="13ef6-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="13ef6-147">Eine Liste der VpnClientCertificates, die zu widerrufenden Dateipfaden verwendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="13ef6-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="13ef6-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="13ef6-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="13ef6-149">Eine Liste der VpnClientRootCertificates, die den Pfaden von Dateien hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="13ef6-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="13ef6-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="13ef6-150">-VpnProtocol</span></span>
<span data-ttu-id="13ef6-151">Die Liste der Protokolle zum Tunneln von P2S-VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="13ef6-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="13ef6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13ef6-152">-Confirm</span></span>
<span data-ttu-id="13ef6-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13ef6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ef6-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="13ef6-154">-WhatIf</span></span>
<span data-ttu-id="13ef6-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13ef6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ef6-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13ef6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ef6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ef6-157">CommonParameters</span></span>
<span data-ttu-id="13ef6-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ef6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ef6-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13ef6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ef6-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13ef6-160">INPUTS</span></span>

### <span data-ttu-id="13ef6-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="13ef6-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="13ef6-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13ef6-162">OUTPUTS</span></span>

### <span data-ttu-id="13ef6-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="13ef6-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="13ef6-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13ef6-164">NOTES</span></span>

## <span data-ttu-id="13ef6-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13ef6-165">RELATED LINKS</span></span>
