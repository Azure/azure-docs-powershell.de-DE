---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 013831c6b7b05a1da520744df9823076d95ccf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505294"
---
# <span data-ttu-id="11fe9-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="11fe9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="11fe9-103">Ändert eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="11fe9-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11fe9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11fe9-104">SYNTAX</span></span>

### <span data-ttu-id="11fe9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11fe9-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11fe9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11fe9-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11fe9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11fe9-107">DESCRIPTION</span></span>
<span data-ttu-id="11fe9-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayIPConfiguration** " ändert eine IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="11fe9-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="11fe9-109">Eine IP-Konfiguration enthält das Subnetz, in dem ein Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11fe9-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="11fe9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11fe9-110">EXAMPLES</span></span>

### <span data-ttu-id="11fe9-111">Beispiel 1: Festlegung des Zielzustands einer IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="11fe9-112">Der erste Befehl ruft das virtuelle Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet Variablen.</span><span class="sxs-lookup"><span data-stu-id="11fe9-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="11fe9-113">Der zweite Befehl ruft die Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="11fe9-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="11fe9-114">Der dritte Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="11fe9-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="11fe9-115">Der Befehl Forth legt die IP-Konfiguration des in $AppGw gespeicherten Anwendungs Gateways auf die in $Subnet gespeicherte Subnetz-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="11fe9-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="11fe9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="11fe9-116">PARAMETERS</span></span>

### <span data-ttu-id="11fe9-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fe9-117">-ApplicationGateway</span></span>
<span data-ttu-id="11fe9-118">Gibt ein Application Gateway-Objekt an, mit dem dieses Cmdlet eine IP-Konfiguration verknüpft.</span><span class="sxs-lookup"><span data-stu-id="11fe9-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="11fe9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fe9-119">-DefaultProfile</span></span>
<span data-ttu-id="11fe9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11fe9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11fe9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="11fe9-121">-Name</span></span>
<span data-ttu-id="11fe9-122">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="11fe9-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="11fe9-123">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="11fe9-123">-Subnet</span></span>
<span data-ttu-id="11fe9-124">Gibt das Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="11fe9-124">Specifies the subnet.</span></span>
<span data-ttu-id="11fe9-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11fe9-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe9-126">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="11fe9-126">-SubnetId</span></span>
<span data-ttu-id="11fe9-127">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="11fe9-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="11fe9-128">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="11fe9-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11fe9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fe9-129">CommonParameters</span></span>
<span data-ttu-id="11fe9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11fe9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fe9-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11fe9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fe9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11fe9-132">INPUTS</span></span>

### <span data-ttu-id="11fe9-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fe9-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="11fe9-134">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11fe9-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="11fe9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11fe9-135">OUTPUTS</span></span>

### <span data-ttu-id="11fe9-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11fe9-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11fe9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="11fe9-137">NOTES</span></span>

## <span data-ttu-id="11fe9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11fe9-138">RELATED LINKS</span></span>

[<span data-ttu-id="11fe9-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="11fe9-140">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-140">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="11fe9-141">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-141">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="11fe9-142">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-142">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="11fe9-143">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11fe9-143">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


