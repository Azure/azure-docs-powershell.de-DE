---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940272"
---
# <span data-ttu-id="3d152-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3d152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d152-102">SYNOPSIS</span></span>
<span data-ttu-id="3d152-103">Ruft das vertrauenswürdige Stammzertifikat mit einem bestimmten Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3d152-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="3d152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d152-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d152-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d152-105">DESCRIPTION</span></span>
<span data-ttu-id="3d152-106">Das **Get-AzApplicationGatewayTrustedRootCertificate-Cmdlet** ruft vertrauenswürdiges Stammzertifikat mit einem bestimmten Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3d152-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="3d152-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d152-107">EXAMPLES</span></span>

### <span data-ttu-id="3d152-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d152-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="3d152-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d152-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="3d152-110">Der zweite Befehl ruft das vertrauenswürdige Stammzertifikat mit einem angegebenen Namen aus dem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3d152-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="3d152-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3d152-111">PARAMETERS</span></span>

### <span data-ttu-id="3d152-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d152-112">-ApplicationGateway</span></span>
<span data-ttu-id="3d152-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d152-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d152-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d152-114">-DefaultProfile</span></span>
<span data-ttu-id="3d152-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d152-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d152-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3d152-116">-Name</span></span>
<span data-ttu-id="3d152-117">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="3d152-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="3d152-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d152-118">CommonParameters</span></span>
<span data-ttu-id="3d152-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d152-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d152-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d152-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d152-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d152-121">INPUTS</span></span>

### <span data-ttu-id="3d152-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d152-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d152-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d152-123">OUTPUTS</span></span>

### <span data-ttu-id="3d152-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="3d152-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3d152-125">NOTES</span></span>

## <span data-ttu-id="3d152-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3d152-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d152-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3d152-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3d152-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="3d152-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d152-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
