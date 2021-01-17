---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380203"
---
# <span data-ttu-id="b6dc9-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b6dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dc9-103">Ruft das vertrauenswürdige Stammzertifikat unter einem bestimmten Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="b6dc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6dc9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6dc9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6dc9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6dc9-106">Das **Cmdlet "Get-AzApplicationGatewayTrustedRootCertificate"** ruft das vertrauenswürdige Stammzertifikat mit einem bestimmten Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="b6dc9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6dc9-107">EXAMPLES</span></span>

### <span data-ttu-id="b6dc9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6dc9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="b6dc9-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b6dc9-110">Der zweite Befehl ruft das vertrauenswürdige Stammzertifikat mit einem angegebenen Namen vom Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="b6dc9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6dc9-111">PARAMETERS</span></span>

### <span data-ttu-id="b6dc9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6dc9-112">-ApplicationGateway</span></span>
<span data-ttu-id="b6dc9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6dc9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b6dc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dc9-114">-DefaultProfile</span></span>
<span data-ttu-id="b6dc9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6dc9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b6dc9-116">-Name</span></span>
<span data-ttu-id="b6dc9-117">Der Name des Zertifikats "TrustedRoot"</span><span class="sxs-lookup"><span data-stu-id="b6dc9-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="b6dc9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dc9-118">CommonParameters</span></span>
<span data-ttu-id="b6dc9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6dc9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dc9-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6dc9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dc9-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6dc9-121">INPUTS</span></span>

### <span data-ttu-id="b6dc9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6dc9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6dc9-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6dc9-123">OUTPUTS</span></span>

### <span data-ttu-id="b6dc9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b6dc9-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b6dc9-125">NOTES</span></span>

## <span data-ttu-id="b6dc9-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b6dc9-126">RELATED LINKS</span></span>

[<span data-ttu-id="b6dc9-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6dc9-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6dc9-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b6dc9-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dc9-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
