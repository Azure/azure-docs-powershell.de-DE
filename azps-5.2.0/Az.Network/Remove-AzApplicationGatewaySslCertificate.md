---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b03d35b511bafefe0ba062eb15a9c1eee8961585
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360967"
---
# <span data-ttu-id="6ada5-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ada5-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6ada5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ada5-102">SYNOPSIS</span></span>
<span data-ttu-id="6ada5-103">Entfernt ein Zertifikat aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6ada5-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="6ada5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ada5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ada5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ada5-105">DESCRIPTION</span></span>
<span data-ttu-id="6ada5-106">Das **Cmdlet "Remove-AzApplicationGatewaySslCertificate"** entfernt ein Secure Sockets Layer (SSL)-Zertifikat aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6ada5-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="6ada5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ada5-107">EXAMPLES</span></span>

### <span data-ttu-id="6ada5-108">Beispiel 1: Entfernen eines SSL-Zertifikats von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="6ada5-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="6ada5-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ada5-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6ada5-110">Mit dem zweiten Befehl wird das #A0 namens Cert02 aus dem Anwendungsgateway entfernt, das in der #A1 $AppGW ist.</span><span class="sxs-lookup"><span data-stu-id="6ada5-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="6ada5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ada5-111">PARAMETERS</span></span>

### <span data-ttu-id="6ada5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ada5-112">-ApplicationGateway</span></span>
<span data-ttu-id="6ada5-113">Gibt das Anwendungsgateway an, aus dem dieses Cmdlet ein ZERTIFIKAT entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ada5-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="6ada5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ada5-114">-DefaultProfile</span></span>
<span data-ttu-id="6ada5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ada5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ada5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6ada5-116">-Name</span></span>
<span data-ttu-id="6ada5-117">Gibt den Namen eines SSL-Zertifikats an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6ada5-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6ada5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ada5-118">CommonParameters</span></span>
<span data-ttu-id="6ada5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ada5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ada5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ada5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ada5-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ada5-121">INPUTS</span></span>

### <span data-ttu-id="6ada5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ada5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ada5-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ada5-123">OUTPUTS</span></span>

### <span data-ttu-id="6ada5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ada5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ada5-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ada5-125">NOTES</span></span>

## <span data-ttu-id="6ada5-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ada5-126">RELATED LINKS</span></span>

[<span data-ttu-id="6ada5-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ada5-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ada5-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ada5-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ada5-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ada5-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6ada5-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ada5-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


