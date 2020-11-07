---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848740"
---
# <span data-ttu-id="13ff1-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="13ff1-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="13ff1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="13ff1-103">Entfernt ein SSL-Zertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13ff1-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ff1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ff1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ff1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="13ff1-106">Das Cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** entfernt ein SSL-Zertifikat (Secure Sockets Layer) von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13ff1-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="13ff1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13ff1-107">EXAMPLES</span></span>

### <span data-ttu-id="13ff1-108">Beispiel 1: Entfernen eines SSL-Zertifikats von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="13ff1-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="13ff1-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="13ff1-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="13ff1-110">Der zweite Befehl entfernt das SSL-Zertifikat mit dem Namen Cert02 aus dem Anwendungsgateway, das in der $AppGW-Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="13ff1-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="13ff1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="13ff1-111">PARAMETERS</span></span>

### <span data-ttu-id="13ff1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ff1-112">-ApplicationGateway</span></span>
<span data-ttu-id="13ff1-113">Gibt das Anwendungsgateway an, von dem dieses Cmdlet ein SSL-Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="13ff1-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="13ff1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ff1-114">-DefaultProfile</span></span>
<span data-ttu-id="13ff1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13ff1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ff1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="13ff1-116">-Name</span></span>
<span data-ttu-id="13ff1-117">Gibt den Namen eines SSL-Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="13ff1-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13ff1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ff1-118">CommonParameters</span></span>
<span data-ttu-id="13ff1-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ff1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ff1-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ff1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ff1-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13ff1-121">INPUTS</span></span>

### <span data-ttu-id="13ff1-122">System. String</span><span class="sxs-lookup"><span data-stu-id="13ff1-122">System.String</span></span>

## <span data-ttu-id="13ff1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13ff1-123">OUTPUTS</span></span>

### <span data-ttu-id="13ff1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13ff1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13ff1-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="13ff1-125">NOTES</span></span>

## <span data-ttu-id="13ff1-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13ff1-126">RELATED LINKS</span></span>

[<span data-ttu-id="13ff1-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="13ff1-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="13ff1-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="13ff1-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="13ff1-129">Neu – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="13ff1-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="13ff1-130">Satz-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="13ff1-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


