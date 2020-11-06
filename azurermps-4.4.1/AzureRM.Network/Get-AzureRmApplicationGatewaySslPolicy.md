---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 29f9d1b13704f190a94bffaa70b900bc5a3b29e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501745"
---
# <span data-ttu-id="5f765-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5f765-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5f765-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f765-102">SYNOPSIS</span></span>
<span data-ttu-id="5f765-103">Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5f765-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f765-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f765-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f765-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f765-105">DESCRIPTION</span></span>
<span data-ttu-id="5f765-106">Das Cmdlet " **Get-AzureRmApplicationGatewaySslPolicy** " Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5f765-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5f765-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f765-107">EXAMPLES</span></span>

### <span data-ttu-id="5f765-108">1:</span><span class="sxs-lookup"><span data-stu-id="5f765-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="5f765-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5f765-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5f765-110">Der zweite Befehl ruft die SSL-Richtlinie aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5f765-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="5f765-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f765-111">PARAMETERS</span></span>

### <span data-ttu-id="5f765-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f765-112">-ApplicationGateway</span></span>
<span data-ttu-id="5f765-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5f765-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f765-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f765-114">-DefaultProfile</span></span>
<span data-ttu-id="5f765-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f765-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f765-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f765-116">CommonParameters</span></span>
<span data-ttu-id="5f765-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f765-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f765-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f765-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f765-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f765-119">INPUTS</span></span>

### <span data-ttu-id="5f765-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5f765-120">System.String</span></span>

## <span data-ttu-id="5f765-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f765-121">OUTPUTS</span></span>

### <span data-ttu-id="5f765-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5f765-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5f765-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f765-123">NOTES</span></span>
* <span data-ttu-id="5f765-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="5f765-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5f765-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f765-125">RELATED LINKS</span></span>

[<span data-ttu-id="5f765-126">Neu – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5f765-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5f765-127">Satz-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5f765-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


