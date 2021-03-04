---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: b9522cf7bc29f01215cbac7473c58643b8d63b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940275"
---
# <span data-ttu-id="be759-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="be759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be759-102">SYNOPSIS</span></span>
<span data-ttu-id="be759-103">Ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem bestimmten Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="be759-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="be759-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be759-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be759-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be759-105">DESCRIPTION</span></span>
<span data-ttu-id="be759-106">Das Get-AzApplicationGatewayTrustedClientCertificate-Cmdlet ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem bestimmten Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="be759-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="be759-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be759-107">EXAMPLES</span></span>

### <span data-ttu-id="be759-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be759-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="be759-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="be759-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="be759-110">Der zweite Befehl ruft die Zertifikatkette der vertrauenswürdigen Client-Zertifizierungsstelle mit einem angegebenen Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="be759-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="be759-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="be759-111">PARAMETERS</span></span>

### <span data-ttu-id="be759-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be759-112">-ApplicationGateway</span></span>
<span data-ttu-id="be759-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be759-113">The applicationGateway</span></span>

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

### <span data-ttu-id="be759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be759-114">-DefaultProfile</span></span>
<span data-ttu-id="be759-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be759-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be759-116">-Name</span><span class="sxs-lookup"><span data-stu-id="be759-116">-Name</span></span>
<span data-ttu-id="be759-117">Der Name der Zertifikatkette für vertrauenswürdige Client-Zertifizierungsstellen</span><span class="sxs-lookup"><span data-stu-id="be759-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="be759-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be759-118">CommonParameters</span></span>
<span data-ttu-id="be759-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be759-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be759-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be759-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be759-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be759-121">INPUTS</span></span>

### <span data-ttu-id="be759-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be759-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be759-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be759-123">OUTPUTS</span></span>

### <span data-ttu-id="be759-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="be759-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="be759-125">NOTES</span></span>

## <span data-ttu-id="be759-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="be759-126">RELATED LINKS</span></span>

[<span data-ttu-id="be759-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="be759-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="be759-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="be759-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="be759-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)