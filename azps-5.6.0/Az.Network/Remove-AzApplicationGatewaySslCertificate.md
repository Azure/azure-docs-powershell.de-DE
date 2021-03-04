---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936147"
---
# <span data-ttu-id="b5c3d-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c3d-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b5c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c3d-103">Entfernt ein SSL-Zertifikat aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b5c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5c3d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c3d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c3d-106">Das **Cmdlet Remove-AzApplicationGatewaySslCertificate** entfernt ein SSL-Zertifikat (Secure Sockets Layer) aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b5c3d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c3d-108">Beispiel 1: Entfernen eines SSL-Zertifikats aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b5c3d-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="b5c3d-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b5c3d-110">Mit dem zweiten Befehl wird das #A0 mit dem Namen Cert02 aus dem Anwendungsgateway entfernt, das in der $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="b5c3d-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5c3d-111">PARAMETERS</span></span>

### <span data-ttu-id="b5c3d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c3d-112">-ApplicationGateway</span></span>
<span data-ttu-id="b5c3d-113">Gibt das Anwendungsgateway an, aus dem dieses Cmdlet ein SSL-Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="b5c3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c3d-114">-DefaultProfile</span></span>
<span data-ttu-id="b5c3d-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c3d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b5c3d-116">-Name</span></span>
<span data-ttu-id="b5c3d-117">Gibt den Namen eines SSL-Zertifikats an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c3d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c3d-118">CommonParameters</span></span>
<span data-ttu-id="b5c3d-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c3d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c3d-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c3d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c3d-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5c3d-121">INPUTS</span></span>

### <span data-ttu-id="b5c3d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c3d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5c3d-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5c3d-123">OUTPUTS</span></span>

### <span data-ttu-id="b5c3d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c3d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5c3d-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5c3d-125">NOTES</span></span>

## <span data-ttu-id="b5c3d-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5c3d-126">RELATED LINKS</span></span>

[<span data-ttu-id="b5c3d-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c3d-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5c3d-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c3d-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5c3d-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c3d-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5c3d-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c3d-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


