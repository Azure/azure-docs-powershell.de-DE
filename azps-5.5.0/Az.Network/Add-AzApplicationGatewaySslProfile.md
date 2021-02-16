---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170094"
---
# <span data-ttu-id="8ee98-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8ee98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee98-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee98-103">Fügt einem Anwendungsgateway das Profil "SSL" hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ee98-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="8ee98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ee98-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ee98-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee98-106">Das **Cmdlet "Add-AzApplicationGatewaySslProfile"** fügt einem Anwendungsgateway ein "SSL-Profil" hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ee98-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="8ee98-107">Das "SSL"-Profil wird auf "HTTPS-Listener" angewendet.</span><span class="sxs-lookup"><span data-stu-id="8ee98-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="8ee98-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ee98-108">EXAMPLES</span></span>

### <span data-ttu-id="8ee98-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ee98-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="8ee98-110">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="8ee98-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8ee98-111">Der zweite Befehl erstellt eine neue SSL-Richtlinie und speichert sie in der $sslPolicy Variable.</span><span class="sxs-lookup"><span data-stu-id="8ee98-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="8ee98-112">Der dritte und vierte Befehl erstellen zwei neue Zertifikatketten für vertrauenswürdige Client-Zertifizierungsstellen und speichern diese in den Variablen $ClientCert 01 und $ClientCert 02.</span><span class="sxs-lookup"><span data-stu-id="8ee98-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="8ee98-113">Der fünfte Befehl fügt das SSL-Profil mit der Ssl-Richtlinie und zertifikatketten vertrauenswürdigen Client-CA-Zertifikatketten zum Anwendungsgateway $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8ee98-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="8ee98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ee98-114">PARAMETERS</span></span>

### <span data-ttu-id="8ee98-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ee98-115">-ApplicationGateway</span></span>
<span data-ttu-id="8ee98-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ee98-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ee98-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ee98-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="8ee98-118">Konfigurationseinstellungen für die Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="8ee98-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="8ee98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-119">-DefaultProfile</span></span>
<span data-ttu-id="8ee98-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ee98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee98-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8ee98-121">-Name</span></span>
<span data-ttu-id="8ee98-122">Der Name des SSL-Profils</span><span class="sxs-lookup"><span data-stu-id="8ee98-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="8ee98-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="8ee98-123">-SslPolicy</span></span>
<span data-ttu-id="8ee98-124">"SSL-Richtlinie"</span><span class="sxs-lookup"><span data-stu-id="8ee98-124">SSL policy</span></span>

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

### <span data-ttu-id="8ee98-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="8ee98-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="8ee98-126">Zertifikatketten der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="8ee98-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="8ee98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee98-127">CommonParameters</span></span>
<span data-ttu-id="8ee98-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee98-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ee98-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee98-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ee98-130">INPUTS</span></span>

### <span data-ttu-id="8ee98-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ee98-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ee98-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ee98-132">OUTPUTS</span></span>

### <span data-ttu-id="8ee98-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ee98-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ee98-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8ee98-134">NOTES</span></span>

## <span data-ttu-id="8ee98-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8ee98-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ee98-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8ee98-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8ee98-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="8ee98-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8ee98-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)