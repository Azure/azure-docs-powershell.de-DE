---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161148"
---
# <span data-ttu-id="02ecb-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="02ecb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="02ecb-103">Ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem bestimmten Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="02ecb-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="02ecb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02ecb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ecb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="02ecb-106">Das Get-AzApplicationGatewayTrustedClientCertificate ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem bestimmten Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="02ecb-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="02ecb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="02ecb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02ecb-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="02ecb-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="02ecb-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="02ecb-110">Der zweite Befehl ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem angegebenen Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="02ecb-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="02ecb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02ecb-111">PARAMETERS</span></span>

### <span data-ttu-id="02ecb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02ecb-112">-ApplicationGateway</span></span>
<span data-ttu-id="02ecb-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02ecb-113">The applicationGateway</span></span>

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

### <span data-ttu-id="02ecb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ecb-114">-DefaultProfile</span></span>
<span data-ttu-id="02ecb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02ecb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ecb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="02ecb-116">-Name</span></span>
<span data-ttu-id="02ecb-117">Der Name der Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="02ecb-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ecb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ecb-118">CommonParameters</span></span>
<span data-ttu-id="02ecb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ecb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ecb-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02ecb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ecb-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02ecb-121">INPUTS</span></span>

### <span data-ttu-id="02ecb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02ecb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02ecb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02ecb-123">OUTPUTS</span></span>

### <span data-ttu-id="02ecb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="02ecb-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02ecb-125">NOTES</span></span>

## <span data-ttu-id="02ecb-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02ecb-126">RELATED LINKS</span></span>

[<span data-ttu-id="02ecb-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="02ecb-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="02ecb-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="02ecb-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ecb-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)