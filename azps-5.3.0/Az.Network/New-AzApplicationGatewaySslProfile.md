---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379278"
---
# <span data-ttu-id="5d2e7-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5d2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2e7-103">Erstellt ein "SSL"-Profil für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="5d2e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d2e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d2e7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="5d2e7-106">Das **Cmdlet "New-AzApplicationGatewaySslProfile"** erstellt ein "SSL-Profil" für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="5d2e7-107">Das Ssl-Profil wird für die HTTPS-Listener konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="5d2e7-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d2e7-108">EXAMPLES</span></span>

### <span data-ttu-id="5d2e7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d2e7-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="5d2e7-110">Der erste Befehl erstellt eine neue SSL-Richtlinie und speichert sie in der $sslPolicy Variable.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="5d2e7-111">Der zweite Befehl erstellt eine Zertifikatketten einer vertrauenswürdigen Client-Zertifizierungsstelle und speichert sie in $ClientCert 01-Variable.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="5d2e7-112">Der dritte Befehl erstellt ein neues SSL-Profil mit der Ssl-Richtlinie und der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="5d2e7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d2e7-113">PARAMETERS</span></span>

### <span data-ttu-id="5d2e7-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d2e7-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="5d2e7-115">Clientauthentifizierungskonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5d2e7-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-116">-DefaultProfile</span></span>
<span data-ttu-id="5d2e7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d2e7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5d2e7-118">-Name</span></span>
<span data-ttu-id="5d2e7-119">Der Name des SSL-Profils</span><span class="sxs-lookup"><span data-stu-id="5d2e7-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="5d2e7-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="5d2e7-120">-SslPolicy</span></span>
<span data-ttu-id="5d2e7-121">"SSL-Richtlinie"</span><span class="sxs-lookup"><span data-stu-id="5d2e7-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e7-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="5d2e7-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="5d2e7-123">Zertifikatketten der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="5d2e7-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2e7-124">CommonParameters</span></span>
<span data-ttu-id="5d2e7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2e7-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d2e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2e7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d2e7-127">INPUTS</span></span>

### <span data-ttu-id="5d2e7-128">Keine</span><span class="sxs-lookup"><span data-stu-id="5d2e7-128">None</span></span>

## <span data-ttu-id="5d2e7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d2e7-129">OUTPUTS</span></span>

### <span data-ttu-id="5d2e7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5d2e7-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d2e7-131">NOTES</span></span>

## <span data-ttu-id="5d2e7-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d2e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="5d2e7-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5d2e7-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5d2e7-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5d2e7-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e7-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)