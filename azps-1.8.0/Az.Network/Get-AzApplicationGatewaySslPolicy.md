---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660834"
---
# <span data-ttu-id="db7fc-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="db7fc-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="db7fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="db7fc-103">Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="db7fc-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="db7fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db7fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db7fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db7fc-105">DESCRIPTION</span></span>
<span data-ttu-id="db7fc-106">Das Cmdlet " **Get-AzApplicationGatewaySslPolicy** " Ruft die SSL-Richtlinie eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="db7fc-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="db7fc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db7fc-107">EXAMPLES</span></span>

### <span data-ttu-id="db7fc-108">1:</span><span class="sxs-lookup"><span data-stu-id="db7fc-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="db7fc-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="db7fc-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="db7fc-110">Der zweite Befehl ruft die SSL-Richtlinie aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="db7fc-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="db7fc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="db7fc-111">PARAMETERS</span></span>

### <span data-ttu-id="db7fc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db7fc-112">-ApplicationGateway</span></span>
<span data-ttu-id="db7fc-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="db7fc-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="db7fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7fc-114">-DefaultProfile</span></span>
<span data-ttu-id="db7fc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db7fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db7fc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7fc-116">CommonParameters</span></span>
<span data-ttu-id="db7fc-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db7fc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7fc-118">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db7fc-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7fc-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db7fc-119">INPUTS</span></span>

### <span data-ttu-id="db7fc-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db7fc-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="db7fc-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db7fc-121">OUTPUTS</span></span>

### <span data-ttu-id="db7fc-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="db7fc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="db7fc-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="db7fc-123">NOTES</span></span>
* <span data-ttu-id="db7fc-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="db7fc-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="db7fc-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db7fc-125">RELATED LINKS</span></span>

[<span data-ttu-id="db7fc-126">Neu – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="db7fc-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="db7fc-127">Satz-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="db7fc-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


