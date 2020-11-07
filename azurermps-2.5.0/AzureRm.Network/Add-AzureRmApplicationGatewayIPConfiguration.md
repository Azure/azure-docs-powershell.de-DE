---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 17938a8fe4ee5a279554758cc36cc7a234a359ce
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849983"
---
# <span data-ttu-id="f3c0a-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c0a-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f3c0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c0a-103">Fügt eine IP-Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3c0a-104">SYNTAX</span></span>

### <span data-ttu-id="f3c0a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c0a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c0a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f3c0a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c0a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c0a-108">Das Cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** fügt eine IP-Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="f3c0a-109">IP-Konfigurationen enthalten das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="f3c0a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3c0a-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c0a-111">Beispiel 1: Hinzufügen einer virtuellen Netzwerkkonfiguration zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f3c0a-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="f3c0a-112">Mit dem ersten Befehl wird ein virtuelles Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="f3c0a-113">Mit dem zweiten Befehl wird ein Subnetz mit dem zuvor erstellten virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="f3c0a-114">Der dritte Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f3c0a-115">Der vierten-Befehl fügt die IP-Konfiguration dem Anwendungsgateway hinzu, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f3c0a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3c0a-116">PARAMETERS</span></span>

### <span data-ttu-id="f3c0a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c0a-117">-ApplicationGateway</span></span>
<span data-ttu-id="f3c0a-118">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="f3c0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c0a-119">-DefaultProfile</span></span>
<span data-ttu-id="f3c0a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3c0a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c0a-121">-Name</span></span>
<span data-ttu-id="f3c0a-122">Gibt den Namen der IP-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="f3c0a-123">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="f3c0a-123">-Subnet</span></span>
<span data-ttu-id="f3c0a-124">Gibt ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-124">Specifies a subnet.</span></span>
<span data-ttu-id="f3c0a-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c0a-126">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="f3c0a-126">-SubnetId</span></span>
<span data-ttu-id="f3c0a-127">Gibt eine Subnetz-ID an.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="f3c0a-128">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c0a-129">CommonParameters</span></span>
<span data-ttu-id="f3c0a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c0a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c0a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c0a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3c0a-132">INPUTS</span></span>

### <span data-ttu-id="f3c0a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f3c0a-133">System.String</span></span>

## <span data-ttu-id="f3c0a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3c0a-134">OUTPUTS</span></span>

### <span data-ttu-id="f3c0a-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c0a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3c0a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3c0a-136">NOTES</span></span>

## <span data-ttu-id="f3c0a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3c0a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3c0a-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c0a-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3c0a-139">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c0a-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3c0a-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c0a-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3c0a-141">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c0a-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


