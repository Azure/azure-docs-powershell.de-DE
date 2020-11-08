---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003425"
---
# <span data-ttu-id="d4a20-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4a20-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="d4a20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a20-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a20-103">Dieser Befehl ermöglicht es den Benutzern, das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen zu erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="d4a20-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="d4a20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a20-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a20-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a20-106">auf diese Weise können die Benutzer das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="d4a20-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="d4a20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a20-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4a20-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="d4a20-109">Dieses Cmdlet wird verwendet, um eine ZIP-Datei für ein VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der "ContosoResourceGroup" von "ResourceGroup" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4a20-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="d4a20-110">Das Profil wird für einen vorkonfigurierten RADIUS-Server generiert, der für die Verwendung der Authentifizierungsmethode "eaptls" mit der VpnProfileRadiusCert-Zertifikatsdatei konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d4a20-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="d4a20-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a20-111">PARAMETERS</span></span>

### <span data-ttu-id="d4a20-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d4a20-112">-AuthenticationMethod</span></span>
<span data-ttu-id="d4a20-113">Die Authentifizierungsmethode kann Werte EAPMSCHAPv2 oder eaptls.</span><span class="sxs-lookup"><span data-stu-id="d4a20-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="d4a20-114">Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Client Konfigurations Installationsprogramm für die Benutzernamen-und Kennwortauthentifizierung, die EAP-MSCHAPv2 Authentifizierungsprotokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4a20-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="d4a20-115">Wenn eaptls angegeben wird, generiert das Cmdlet ein Clientkonfigurations-Installationsprogramm für die Zertifikatauthentifizierung, die das EAP-TLS-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4a20-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="d4a20-116">Die Option "eaptls" kann sowohl für die RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungs Authentifizierung verwendet werden, die vom virtuellen Netzwerk Gateway durch Hochladen des vertrauenswürdigen Stamms durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a20-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="d4a20-117">Das Cmdlet erkennt automatisch, was konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d4a20-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="d4a20-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="d4a20-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="d4a20-119">Eine Liste der Client-Stammzertifikat Pfade</span><span class="sxs-lookup"><span data-stu-id="d4a20-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="d4a20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a20-120">-DefaultProfile</span></span>
<span data-ttu-id="d4a20-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4a20-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a20-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d4a20-122">-Name</span></span>
<span data-ttu-id="d4a20-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d4a20-123">The resource name.</span></span>

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

### <span data-ttu-id="d4a20-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="d4a20-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="d4a20-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="d4a20-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="d4a20-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="d4a20-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="d4a20-127">RADIUS-Server-Stammzertifikatpfad.</span><span class="sxs-lookup"><span data-stu-id="d4a20-127">Radius server root certificate path.</span></span> <span data-ttu-id="d4a20-128">Hierbei handelt es sich um einen obligatorischen Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a20-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="d4a20-129">Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das der Client verwendet, um den RADIUS-Server während der Authentifizierung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d4a20-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="d4a20-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a20-130">-ResourceGroupName</span></span>
<span data-ttu-id="d4a20-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4a20-131">The resource group name.</span></span>

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

### <span data-ttu-id="d4a20-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4a20-132">-Confirm</span></span>
<span data-ttu-id="d4a20-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4a20-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a20-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a20-134">-WhatIf</span></span>
<span data-ttu-id="d4a20-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a20-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4a20-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a20-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a20-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a20-137">CommonParameters</span></span>
<span data-ttu-id="d4a20-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a20-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a20-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a20-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a20-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a20-140">INPUTS</span></span>

### <span data-ttu-id="d4a20-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a20-141">System.String</span></span>

### <span data-ttu-id="d4a20-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="d4a20-142">System.String[]</span></span>

## <span data-ttu-id="d4a20-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a20-143">OUTPUTS</span></span>

### <span data-ttu-id="d4a20-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="d4a20-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="d4a20-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a20-145">NOTES</span></span>

## <span data-ttu-id="d4a20-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a20-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4a20-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4a20-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
