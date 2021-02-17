---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154124"
---
# <span data-ttu-id="ddb21-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ddb21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb21-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb21-103">Aktualisiert das Ssl-Profil für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ddb21-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="ddb21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddb21-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb21-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddb21-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb21-106">Das **Cmdlet Set-AzApplicationGatewaySslProfile** aktualisiert das Ssl-Profil für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ddb21-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="ddb21-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddb21-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb21-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddb21-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="ddb21-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="ddb21-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="ddb21-110">Der zweite Befehl aktualisiert das ssl-Profil des Anwendungsgateways in der $AppGw-Variable, um die Konfiguration der Clientauthentisierung auf den neuen Wert zu aktualisieren, der in der Datei $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="ddb21-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="ddb21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb21-111">PARAMETERS</span></span>

### <span data-ttu-id="ddb21-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb21-112">-ApplicationGateway</span></span>
<span data-ttu-id="ddb21-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb21-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ddb21-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb21-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="ddb21-115">Konfigurationseinstellungen für die Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="ddb21-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="ddb21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-116">-DefaultProfile</span></span>
<span data-ttu-id="ddb21-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb21-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb21-118">-Name</span></span>
<span data-ttu-id="ddb21-119">Der Name des SSL-Profils</span><span class="sxs-lookup"><span data-stu-id="ddb21-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="ddb21-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="ddb21-120">-SslPolicy</span></span>
<span data-ttu-id="ddb21-121">"SSL-Richtlinie"</span><span class="sxs-lookup"><span data-stu-id="ddb21-121">SSL policy</span></span>

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

### <span data-ttu-id="ddb21-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="ddb21-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="ddb21-123">Zertifikatketten der vertrauenswürdigen Client-Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="ddb21-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="ddb21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb21-124">CommonParameters</span></span>
<span data-ttu-id="ddb21-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb21-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddb21-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb21-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddb21-127">INPUTS</span></span>

### <span data-ttu-id="ddb21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ddb21-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddb21-129">OUTPUTS</span></span>

### <span data-ttu-id="ddb21-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb21-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ddb21-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ddb21-131">NOTES</span></span>

## <span data-ttu-id="ddb21-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ddb21-132">RELATED LINKS</span></span>

[<span data-ttu-id="ddb21-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ddb21-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ddb21-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="ddb21-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)