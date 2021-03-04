---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940336"
---
# <span data-ttu-id="6c5df-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6c5df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5df-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5df-103">Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6c5df-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6c5df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c5df-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c5df-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5df-106">Das **Get-AzApplicationGatewaySslCertificate-Cmdlet** erhält ein SSL-Zertifikat für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6c5df-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6c5df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c5df-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5df-108">Beispiel 1: Erhalten eines bestimmten SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6c5df-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6c5df-109">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6c5df-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6c5df-110">Der zweite Befehl ruft das #A0 mit dem Namen Cert01 aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6c5df-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6c5df-111">Der Befehl speichert das Zertifikat in der Variablen namens $Cert.</span><span class="sxs-lookup"><span data-stu-id="6c5df-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="6c5df-112">Beispiel 2: Erhalten einer Liste von SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="6c5df-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="6c5df-113">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6c5df-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6c5df-114">Dieser zweite Befehl ruft eine Liste der SSL-Zertifikate aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6c5df-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="6c5df-115">Der Befehl speichert dann die Ergebnisse in der Variablen namens $Certs.</span><span class="sxs-lookup"><span data-stu-id="6c5df-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="6c5df-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6c5df-116">PARAMETERS</span></span>

### <span data-ttu-id="6c5df-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c5df-117">-ApplicationGateway</span></span>
<span data-ttu-id="6c5df-118">Gibt das Anwendungsgatewayobjekt an, das das SSL-Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="6c5df-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="6c5df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5df-119">-DefaultProfile</span></span>
<span data-ttu-id="6c5df-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c5df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c5df-121">-Name</span></span>
<span data-ttu-id="6c5df-122">Gibt den Namen des SSL-Zertifikatpools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6c5df-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6c5df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5df-123">CommonParameters</span></span>
<span data-ttu-id="6c5df-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5df-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c5df-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5df-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c5df-126">INPUTS</span></span>

### <span data-ttu-id="6c5df-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c5df-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c5df-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c5df-128">OUTPUTS</span></span>

### <span data-ttu-id="6c5df-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6c5df-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6c5df-130">NOTES</span></span>

## <span data-ttu-id="6c5df-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6c5df-131">RELATED LINKS</span></span>

[<span data-ttu-id="6c5df-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6c5df-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6c5df-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6c5df-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6c5df-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


