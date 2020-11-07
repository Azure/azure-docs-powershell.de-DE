---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 9b90dc354a62c6f6d69e1e6dbd8bf18ecc0fa4f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841191"
---
# <span data-ttu-id="7e3b6-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e3b6-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7e3b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e3b6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3b6-103">Entfernt ein SSL-Zertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="7e3b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e3b6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e3b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e3b6-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3b6-106">Das Cmdlet **Remove-AzApplicationGatewaySslCertificate** entfernt ein SSL-Zertifikat (Secure Sockets Layer) von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="7e3b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e3b6-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3b6-108">Beispiel 1: Entfernen eines SSL-Zertifikats von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="7e3b6-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="7e3b6-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="7e3b6-110">Der zweite Befehl entfernt das SSL-Zertifikat mit dem Namen Cert02 aus dem Anwendungsgateway, das in der $AppGW-Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="7e3b6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e3b6-111">PARAMETERS</span></span>

### <span data-ttu-id="7e3b6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e3b6-112">-ApplicationGateway</span></span>
<span data-ttu-id="7e3b6-113">Gibt das Anwendungsgateway an, von dem dieses Cmdlet ein SSL-Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="7e3b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3b6-114">-DefaultProfile</span></span>
<span data-ttu-id="7e3b6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3b6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7e3b6-116">-Name</span></span>
<span data-ttu-id="7e3b6-117">Gibt den Namen eines SSL-Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e3b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3b6-118">CommonParameters</span></span>
<span data-ttu-id="7e3b6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3b6-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3b6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3b6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e3b6-121">INPUTS</span></span>

### <span data-ttu-id="7e3b6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3b6-122">System.String</span></span>

## <span data-ttu-id="7e3b6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e3b6-123">OUTPUTS</span></span>

### <span data-ttu-id="7e3b6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e3b6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e3b6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e3b6-125">NOTES</span></span>

## <span data-ttu-id="7e3b6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e3b6-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e3b6-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e3b6-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7e3b6-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e3b6-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7e3b6-129">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e3b6-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7e3b6-130">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7e3b6-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


