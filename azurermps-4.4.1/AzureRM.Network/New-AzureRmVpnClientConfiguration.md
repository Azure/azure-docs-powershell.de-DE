---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: c6fad9aee39019063aa7872584d34ccec0f756f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662412"
---
# <span data-ttu-id="0e1d0-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e1d0-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="0e1d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1d0-103">Dieser Befehl ermöglicht es den Benutzern, das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen zu erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e1d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e1d0-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e1d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e1d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1d0-106">auf diese Weise können die Benutzer das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="0e1d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e1d0-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e1d0-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="0e1d0-109">Dieses Cmdlet wird verwendet, um eine ZIP-Datei für ein VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der "ContosoResourceGroup" von "ResourceGroup" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="0e1d0-110">Das Profil wird für einen vorkonfigurierten RADIUS-Server generiert, der für die Verwendung der Authentifizierungsmethode "eaptls" mit der VpnProfileRadiusCert-Zertifikatsdatei konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="0e1d0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e1d0-111">PARAMETERS</span></span>

### <span data-ttu-id="0e1d0-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="0e1d0-112">-AuthenticationMethod</span></span>
<span data-ttu-id="0e1d0-113">Die Authentifizierungsmethode kann Werte EAPMSCHAPv2 oder eaptls.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="0e1d0-114">Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Client Konfigurations Installationsprogramm für die Benutzernamen-und Kennwortauthentifizierung, die EAP-MSCHAPv2 Authentifizierungsprotokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="0e1d0-115">Wenn eaptls angegeben wird, generiert das Cmdlet ein Clientkonfigurations-Installationsprogramm für die Zertifikatauthentifizierung, die das EAP-TLS-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="0e1d0-116">Die Option "eaptls" kann sowohl für die RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungs Authentifizierung verwendet werden, die vom virtuellen Netzwerk Gateway durch Hochladen des vertrauenswürdigen Stamms durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="0e1d0-117">Das Cmdlet erkennt automatisch, was konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1d0-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="0e1d0-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="0e1d0-119">Eine Liste der Client-Stammzertifikat Pfade</span><span class="sxs-lookup"><span data-stu-id="0e1d0-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1d0-120">-DefaultProfile</span></span>
<span data-ttu-id="0e1d0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1d0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0e1d0-122">-Name</span></span>
<span data-ttu-id="0e1d0-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-123">The resource name.</span></span>

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

### <span data-ttu-id="0e1d0-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="0e1d0-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="0e1d0-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="0e1d0-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="0e1d0-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="0e1d0-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="0e1d0-127">RADIUS-Server-Stammzertifikatpfad.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-127">Radius server root certificate path.</span></span> <span data-ttu-id="0e1d0-128">Hierbei handelt es sich um einen obligatorischen Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="0e1d0-129">Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das der Client verwendet, um den RADIUS-Server während der Authentifizierung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="0e1d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="0e1d0-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-131">The resource group name.</span></span>

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

### <span data-ttu-id="0e1d0-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e1d0-132">-Confirm</span></span>
<span data-ttu-id="0e1d0-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e1d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1d0-134">-WhatIf</span></span>
<span data-ttu-id="0e1d0-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e1d0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e1d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1d0-137">CommonParameters</span></span>
<span data-ttu-id="0e1d0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1d0-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1d0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e1d0-140">INPUTS</span></span>

### <span data-ttu-id="0e1d0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0e1d0-141">System.String</span></span>
<span data-ttu-id="0e1d0-142">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0e1d0-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0e1d0-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e1d0-143">OUTPUTS</span></span>

### <span data-ttu-id="0e1d0-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="0e1d0-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="0e1d0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e1d0-145">NOTES</span></span>

## <span data-ttu-id="0e1d0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e1d0-146">RELATED LINKS</span></span>

