---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154484"
---
# <span data-ttu-id="6b11d-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6b11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b11d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b11d-103">Ruft ein -SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6b11d-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6b11d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b11d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b11d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b11d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b11d-106">Das **Cmdlet "Get-AzApplicationGatewaySslCertificate"** ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6b11d-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6b11d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b11d-107">EXAMPLES</span></span>

### <span data-ttu-id="6b11d-108">Beispiel 1: Erhalten eines bestimmten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6b11d-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6b11d-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b11d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6b11d-110">Der zweite Befehl ruft das #A0 namens Cert01 vom Anwendungsgateway ab, das in der Variablen namens "$AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b11d-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6b11d-111">Der Befehl speichert das Zertifikat in der Variablen namens $Cert.</span><span class="sxs-lookup"><span data-stu-id="6b11d-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="6b11d-112">Beispiel 2: Erhalten einer Liste von SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="6b11d-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="6b11d-113">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b11d-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6b11d-114">Dieser zweite Befehl ruft eine Liste der SSL-Zertifikate vom Anwendungsgateway ab, das in der Variablen namens "$AppGW" gespeichert $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b11d-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6b11d-115">Der Befehl speichert dann die Ergebnisse in der Variablen namens $Certs.</span><span class="sxs-lookup"><span data-stu-id="6b11d-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="6b11d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b11d-116">PARAMETERS</span></span>

### <span data-ttu-id="6b11d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b11d-117">-ApplicationGateway</span></span>
<span data-ttu-id="6b11d-118">Gibt das Anwendungsgatewayobjekt an, das das SSL-Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="6b11d-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="6b11d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b11d-119">-DefaultProfile</span></span>
<span data-ttu-id="6b11d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b11d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b11d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6b11d-121">-Name</span></span>
<span data-ttu-id="6b11d-122">Gibt den Namen des SSL-Zertifikatpools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6b11d-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6b11d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b11d-123">CommonParameters</span></span>
<span data-ttu-id="6b11d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b11d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b11d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b11d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b11d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b11d-126">INPUTS</span></span>

### <span data-ttu-id="6b11d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b11d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b11d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b11d-128">OUTPUTS</span></span>

### <span data-ttu-id="6b11d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6b11d-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b11d-130">NOTES</span></span>

## <span data-ttu-id="6b11d-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b11d-131">RELATED LINKS</span></span>

[<span data-ttu-id="6b11d-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b11d-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b11d-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6b11d-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6b11d-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


