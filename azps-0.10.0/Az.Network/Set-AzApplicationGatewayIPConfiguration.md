---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2c14c8c903f892ac5fe822e96fc463528d32f39d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843687"
---
# <span data-ttu-id="24249-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="24249-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24249-102">SYNOPSIS</span></span>
<span data-ttu-id="24249-103">Ändert eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="24249-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="24249-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24249-104">SYNTAX</span></span>

### <span data-ttu-id="24249-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24249-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24249-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24249-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24249-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24249-107">DESCRIPTION</span></span>
<span data-ttu-id="24249-108">Das Cmdlet " **Satz-AzApplicationGatewayIPConfiguration** " ändert eine IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="24249-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="24249-109">Eine IP-Konfiguration enthält das Subnetz, in dem ein Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24249-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="24249-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24249-110">EXAMPLES</span></span>

### <span data-ttu-id="24249-111">Beispiel 1: Festlegung des Zielzustands einer IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="24249-112">Der erste Befehl ruft das virtuelle Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $VNet Variablen.</span><span class="sxs-lookup"><span data-stu-id="24249-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="24249-113">Der zweite Befehl ruft die Subnetz-Konfiguration mit dem Namen Subnet01 mit $VNet ab und speichert Sie in der $Subnet-Variablen.</span><span class="sxs-lookup"><span data-stu-id="24249-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="24249-114">Der dritte Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="24249-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="24249-115">Der Befehl Forth legt die IP-Konfiguration des in $AppGw gespeicherten Anwendungs Gateways auf die in $Subnet gespeicherte Subnetz-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="24249-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="24249-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="24249-116">PARAMETERS</span></span>

### <span data-ttu-id="24249-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24249-117">-ApplicationGateway</span></span>
<span data-ttu-id="24249-118">Gibt ein Application Gateway-Objekt an, mit dem dieses Cmdlet eine IP-Konfiguration verknüpft.</span><span class="sxs-lookup"><span data-stu-id="24249-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="24249-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24249-119">-DefaultProfile</span></span>
<span data-ttu-id="24249-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24249-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24249-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24249-121">-Name</span></span>
<span data-ttu-id="24249-122">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="24249-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="24249-123">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="24249-123">-Subnet</span></span>
<span data-ttu-id="24249-124">Gibt das Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="24249-124">Specifies the subnet.</span></span>
<span data-ttu-id="24249-125">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24249-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="24249-126">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="24249-126">-SubnetId</span></span>
<span data-ttu-id="24249-127">Gibt die Subnet-ID an.</span><span class="sxs-lookup"><span data-stu-id="24249-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="24249-128">Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24249-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="24249-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24249-129">CommonParameters</span></span>
<span data-ttu-id="24249-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24249-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24249-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24249-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24249-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24249-132">INPUTS</span></span>

### <span data-ttu-id="24249-133">System. String</span><span class="sxs-lookup"><span data-stu-id="24249-133">System.String</span></span>

## <span data-ttu-id="24249-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24249-134">OUTPUTS</span></span>

### <span data-ttu-id="24249-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24249-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24249-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="24249-136">NOTES</span></span>

## <span data-ttu-id="24249-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24249-137">RELATED LINKS</span></span>

[<span data-ttu-id="24249-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="24249-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="24249-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="24249-141">Neu – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="24249-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24249-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


