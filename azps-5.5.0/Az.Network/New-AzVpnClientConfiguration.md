---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156865"
---
# <span data-ttu-id="6fe1e-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fe1e-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="6fe1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe1e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe1e-103">Dieser Befehl ermöglicht es den Benutzern, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. einige Stammzertifikate, das Vpn-Profilpaket basierend auf vorkonfigurierten Vpneinstellungen auf dem VPN-Gateway zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="6fe1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fe1e-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fe1e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fe1e-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe1e-106">dadurch können die Benutzer zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. einige Stammzertifikate, das Vpn-Profilpaket basierend auf vorkonfigurierten Vpneinstellungen auf dem VPN-Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="6fe1e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fe1e-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe1e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fe1e-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="6fe1e-109">Dieses Cmdlet wird verwendet, um eine ZIP-Datei für das VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der Ressourcengruppe "ContosoResourceGroup" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="6fe1e-110">Das Profil wird für einen vorkonfigurierten Radiusserver generiert, der für die Verwendung der "EAPTLS"-Authentifizierungsmethode mit der Zertifikatdatei "VpnProfileRadiusCert" konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="6fe1e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe1e-111">PARAMETERS</span></span>

### <span data-ttu-id="6fe1e-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="6fe1e-112">-AuthenticationMethod</span></span>
<span data-ttu-id="6fe1e-113">Bei der Authentifizierungsmethode können Werte wie EAPMSCHAPv2 oder EAPTLS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="6fe1e-114">Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Clientkonfigurationsprogramm für die Authentifizierung mit Benutzername/Kennwort, das EAP-MSCHAPv2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="6fe1e-115">Wenn EAPTLS angegeben wird, generiert das Cmdlet ein Clientkonfigurationsprogramm für die Zertifikatauthentifizierung, das das EAP-TLS-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="6fe1e-116">Die Option "EapTls" kann sowohl für DIE RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungsauthentifizierung verwendet werden, die vom virtuellen Netzwerkgateway durch Hochladen des vertrauenswürdigen Stamms ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="6fe1e-117">Das Cmdlet erkennt automatisch, was konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="6fe1e-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="6fe1e-119">Eine Liste der Pfade für Clientstammzertifikate</span><span class="sxs-lookup"><span data-stu-id="6fe1e-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe1e-120">-DefaultProfile</span></span>
<span data-ttu-id="6fe1e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fe1e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe1e-122">-Name</span></span>
<span data-ttu-id="6fe1e-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6fe1e-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="6fe1e-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6fe1e-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="6fe1e-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="6fe1e-127">Radius des Serverstammzertifikatpfads.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-127">Radius server root certificate path.</span></span> <span data-ttu-id="6fe1e-128">Dies ist ein obligatorischer Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="6fe1e-129">Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das der Client zum Überprüfen des RADIUS-Servers während der Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe1e-130">-ResourceGroupName</span></span>
<span data-ttu-id="6fe1e-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe1e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fe1e-132">-Confirm</span></span>
<span data-ttu-id="6fe1e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe1e-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6fe1e-134">-WhatIf</span></span>
<span data-ttu-id="6fe1e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fe1e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe1e-137">CommonParameters</span></span>
<span data-ttu-id="6fe1e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe1e-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe1e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe1e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fe1e-140">INPUTS</span></span>

### <span data-ttu-id="6fe1e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6fe1e-141">System.String</span></span>

### <span data-ttu-id="6fe1e-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6fe1e-142">System.String[]</span></span>

## <span data-ttu-id="6fe1e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fe1e-143">OUTPUTS</span></span>

### <span data-ttu-id="6fe1e-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="6fe1e-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="6fe1e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fe1e-145">NOTES</span></span>

## <span data-ttu-id="6fe1e-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fe1e-146">RELATED LINKS</span></span>

[<span data-ttu-id="6fe1e-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fe1e-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
