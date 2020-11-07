---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 09986be8ccc8dce8eaec522c501fe3f98ff03c56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850751"
---
# <span data-ttu-id="c66ad-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c66ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c66ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c66ad-103">Ruft die IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="c66ad-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c66ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c66ad-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c66ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c66ad-105">DESCRIPTION</span></span>
<span data-ttu-id="c66ad-106">Das Cmdlet " **Get-AzureRmApplicationGatewayIPConfiguration** " Ruft die IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="c66ad-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="c66ad-107">Die IP-Konfiguration enthält das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c66ad-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="c66ad-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c66ad-108">EXAMPLES</span></span>

### <span data-ttu-id="c66ad-109">Beispiel 1: Abrufen einer bestimmten IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c66ad-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Der zweite Befehl ruft eine IP-Konfiguration mit dem Namen GateSubnet01 aus dem Gateway ab, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c66ad-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="c66ad-111">Beispiel 2: Abrufen einer Liste mit IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c66ad-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="c66ad-112">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Der zweite Befehl ruft eine Liste aller IP-Konfigurationen ab.</span><span class="sxs-lookup"><span data-stu-id="c66ad-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="c66ad-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c66ad-113">PARAMETERS</span></span>

### <span data-ttu-id="c66ad-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c66ad-114">-ApplicationGateway</span></span>
<span data-ttu-id="c66ad-115">Gibt das Application Gateway-Objekt an, das die IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="c66ad-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="c66ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66ad-116">-DefaultProfile</span></span>
<span data-ttu-id="c66ad-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c66ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c66ad-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c66ad-118">-Name</span></span>
<span data-ttu-id="c66ad-119">Gibt den Namen der IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c66ad-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66ad-120">CommonParameters</span></span>
<span data-ttu-id="c66ad-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c66ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66ad-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c66ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66ad-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c66ad-123">INPUTS</span></span>

### <span data-ttu-id="c66ad-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c66ad-124">System.String</span></span>

## <span data-ttu-id="c66ad-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c66ad-125">OUTPUTS</span></span>

### <span data-ttu-id="c66ad-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c66ad-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c66ad-127">NOTES</span></span>

## <span data-ttu-id="c66ad-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c66ad-128">RELATED LINKS</span></span>

[<span data-ttu-id="c66ad-129">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c66ad-130">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c66ad-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c66ad-132">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c66ad-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


