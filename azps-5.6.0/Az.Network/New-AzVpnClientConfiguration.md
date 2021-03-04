---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924675"
---
# <span data-ttu-id="f0bbe-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0bbe-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="f0bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bbe-103">Dieser Befehl ermöglicht benutzern das Erstellen des Vpn-Profilpakets basierend auf vorkonfigurierten Vpn-Einstellungen auf dem VPN-Gateway, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="f0bbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0bbe-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0bbe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="f0bbe-106">Auf diese Weise können die Benutzer das Vpn-Profilpaket basierend auf vorkonfigurierten Vpn-Einstellungen auf dem VPN-Gateway erstellen, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="f0bbe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="f0bbe-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0bbe-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="f0bbe-109">Dieses Cmdlet wird verwendet, um eine ZIP-Datei für ein VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der Ressourcengruppe "ContosoResourceGroup" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="f0bbe-110">Das Profil wird für einen vorkonfigurierten Radiusserver generiert, der für die Verwendung der Authentifizierungsmethode "EAPTLS" mit der VpnProfileRadiusCert-Zertifikatdatei konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="f0bbe-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0bbe-111">PARAMETERS</span></span>

### <span data-ttu-id="f0bbe-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="f0bbe-112">-AuthenticationMethod</span></span>
<span data-ttu-id="f0bbe-113">Die Authentifizierungsmethode kann werte EAPMSCHAPv2 oder EAPTLS übernehmen.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="f0bbe-114">Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Clientkonfigurationsinstallationsprogramm für die Benutzername-/Kennwortauthentifizierung, das EAP-MSCHAPv2 Authentifizierungsprotokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="f0bbe-115">Wenn EAPTLS angegeben ist, generiert das Cmdlet ein Clientkonfigurationsinstallationsprogramm für die Zertifikatauthentifizierung, das das EAP-TLS-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="f0bbe-116">Die Option "EapTls" kann sowohl für die RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungsauthentifizierung verwendet werden, die vom Virtual Network Gateway durch Hochladen des vertrauenswürdigen Stamms ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="f0bbe-117">Das Cmdlet erkennt automatisch, was konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="f0bbe-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="f0bbe-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="f0bbe-119">Eine Liste der Clientstammzertifikatpfade</span><span class="sxs-lookup"><span data-stu-id="f0bbe-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="f0bbe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bbe-120">-DefaultProfile</span></span>
<span data-ttu-id="f0bbe-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0bbe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0bbe-122">-Name</span></span>
<span data-ttu-id="f0bbe-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-123">The resource name.</span></span>

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

### <span data-ttu-id="f0bbe-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f0bbe-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="f0bbe-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f0bbe-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="f0bbe-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="f0bbe-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="f0bbe-127">Radiusserverstammzertifikatpfad.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-127">Radius server root certificate path.</span></span> <span data-ttu-id="f0bbe-128">Dies ist ein obligatorischer Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="f0bbe-129">Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das vom Client zum Überprüfen des RADIUS-Servers während der Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="f0bbe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bbe-130">-ResourceGroupName</span></span>
<span data-ttu-id="f0bbe-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-131">The resource group name.</span></span>

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

### <span data-ttu-id="f0bbe-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0bbe-132">-Confirm</span></span>
<span data-ttu-id="f0bbe-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0bbe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0bbe-134">-WhatIf</span></span>
<span data-ttu-id="f0bbe-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0bbe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0bbe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bbe-137">CommonParameters</span></span>
<span data-ttu-id="f0bbe-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bbe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bbe-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0bbe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bbe-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0bbe-140">INPUTS</span></span>

### <span data-ttu-id="f0bbe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f0bbe-141">System.String</span></span>

### <span data-ttu-id="f0bbe-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f0bbe-142">System.String[]</span></span>

## <span data-ttu-id="f0bbe-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0bbe-143">OUTPUTS</span></span>

### <span data-ttu-id="f0bbe-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="f0bbe-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="f0bbe-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0bbe-145">NOTES</span></span>

## <span data-ttu-id="f0bbe-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0bbe-146">RELATED LINKS</span></span>

[<span data-ttu-id="f0bbe-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0bbe-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
