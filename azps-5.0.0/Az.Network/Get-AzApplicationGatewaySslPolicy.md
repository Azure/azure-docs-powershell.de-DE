---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180184"
---
# <span data-ttu-id="f3460-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f3460-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f3460-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3460-102">SYNOPSIS</span></span>
<span data-ttu-id="f3460-103">Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="f3460-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="f3460-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3460-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3460-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3460-105">DESCRIPTION</span></span>
<span data-ttu-id="f3460-106">Das Cmdlet " **Get-AzApplicationGatewaySslPolicy** " Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="f3460-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="f3460-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3460-107">EXAMPLES</span></span>

### <span data-ttu-id="f3460-108">1:</span><span class="sxs-lookup"><span data-stu-id="f3460-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="f3460-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f3460-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f3460-110">Der zweite Befehl ruft die SSL-Richtlinie aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f3460-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f3460-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3460-111">PARAMETERS</span></span>

### <span data-ttu-id="f3460-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3460-112">-ApplicationGateway</span></span>
<span data-ttu-id="f3460-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f3460-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3460-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3460-114">-DefaultProfile</span></span>
<span data-ttu-id="f3460-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3460-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3460-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3460-116">CommonParameters</span></span>
<span data-ttu-id="f3460-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3460-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3460-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3460-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3460-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3460-119">INPUTS</span></span>

### <span data-ttu-id="f3460-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3460-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3460-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3460-121">OUTPUTS</span></span>

### <span data-ttu-id="f3460-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f3460-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f3460-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3460-123">NOTES</span></span>
* <span data-ttu-id="f3460-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f3460-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f3460-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3460-125">RELATED LINKS</span></span>

[<span data-ttu-id="f3460-126">Neu – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f3460-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="f3460-127">Satz-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f3460-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


