---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 16df8726fc0018bbc89dfbee025223b9e35792c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822431"
---
# <span data-ttu-id="2c1c4-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2c1c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1c4-103">Ruft die IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="2c1c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c1c4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c1c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c1c4-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1c4-106">Das Cmdlet " **Get-AzApplicationGatewayIPConfiguration** " Ruft die IP-Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="2c1c4-107">Die IP-Konfiguration enthält das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="2c1c4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c1c4-108">EXAMPLES</span></span>

### <span data-ttu-id="2c1c4-109">Beispiel 1: Abrufen einer bestimmten IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="2c1c4-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Der zweite Befehl ruft eine IP-Konfiguration mit dem Namen GateSubnet01 aus dem Gateway ab, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="2c1c4-111">Beispiel 2: Abrufen einer Liste mit IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="2c1c4-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="2c1c4-112">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Der zweite Befehl ruft eine Liste aller IP-Konfigurationen ab.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="2c1c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c1c4-113">PARAMETERS</span></span>

### <span data-ttu-id="2c1c4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c1c4-114">-ApplicationGateway</span></span>
<span data-ttu-id="2c1c4-115">Gibt das Application Gateway-Objekt an, das die IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="2c1c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1c4-116">-DefaultProfile</span></span>
<span data-ttu-id="2c1c4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c1c4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2c1c4-118">-Name</span></span>
<span data-ttu-id="2c1c4-119">Gibt den Namen der IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="2c1c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1c4-120">CommonParameters</span></span>
<span data-ttu-id="2c1c4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1c4-122">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c1c4-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1c4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c1c4-123">INPUTS</span></span>

### <span data-ttu-id="2c1c4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c1c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c1c4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c1c4-125">OUTPUTS</span></span>

### <span data-ttu-id="2c1c4-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2c1c4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c1c4-127">NOTES</span></span>

## <span data-ttu-id="2c1c4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c1c4-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c1c4-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c1c4-130">Neu – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c1c4-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2c1c4-132">Satz-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c1c4-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


