---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850784"
---
# <span data-ttu-id="980a4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="980a4-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="980a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="980a4-102">SYNOPSIS</span></span>
<span data-ttu-id="980a4-103">Fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="980a4-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="980a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="980a4-104">SYNTAX</span></span>

### <span data-ttu-id="980a4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="980a4-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="980a4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="980a4-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="980a4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="980a4-107">DESCRIPTION</span></span>
<span data-ttu-id="980a4-108">Das Cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="980a4-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="980a4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="980a4-109">EXAMPLES</span></span>

### <span data-ttu-id="980a4-110">1:</span><span class="sxs-lookup"><span data-stu-id="980a4-110">1:</span></span>
```

```

## <span data-ttu-id="980a4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="980a4-111">PARAMETERS</span></span>

### <span data-ttu-id="980a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980a4-112">-DefaultProfile</span></span>
<span data-ttu-id="980a4-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="980a4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="980a4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="980a4-114">-Name</span></span>
<span data-ttu-id="980a4-115">Gibt den Namen der IP-Gateway-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="980a4-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="980a4-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="980a4-116">-PrivateIpAddress</span></span>
<span data-ttu-id="980a4-117">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="980a4-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="980a4-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="980a4-118">-PublicIpAddress</span></span>
<span data-ttu-id="980a4-119">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="980a4-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980a4-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="980a4-120">-PublicIpAddressId</span></span>
<span data-ttu-id="980a4-121">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="980a4-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="980a4-122">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="980a4-122">-Subnet</span></span>
<span data-ttu-id="980a4-123">Gibt ein **PSSubnet** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="980a4-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="980a4-124">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="980a4-124">-SubnetId</span></span>
<span data-ttu-id="980a4-125">Gibt die ID des Subnets an.</span><span class="sxs-lookup"><span data-stu-id="980a4-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="980a4-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a4-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="980a4-127">Gibt ein **PSVirtualNetworkGateway** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="980a4-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="980a4-128">Dieses Cmdlet ändert das von Ihnen angegebene **PSVirtualNetworkGateway** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="980a4-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="980a4-129">Sie können das Get-AzureRmVirtualNetworkGateway-Cmdlet verwenden, um ein **PSVirtualNetworkGateway** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="980a4-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="980a4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="980a4-130">-Confirm</span></span>
<span data-ttu-id="980a4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="980a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="980a4-132">-WhatIf</span></span>
<span data-ttu-id="980a4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="980a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="980a4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="980a4-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980a4-135">CommonParameters</span></span>
<span data-ttu-id="980a4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980a4-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="980a4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980a4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="980a4-138">INPUTS</span></span>

### <span data-ttu-id="980a4-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a4-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="980a4-140">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="980a4-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="980a4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="980a4-141">OUTPUTS</span></span>

### <span data-ttu-id="980a4-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a4-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="980a4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="980a4-143">NOTES</span></span>

## <span data-ttu-id="980a4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="980a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="980a4-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="980a4-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="980a4-146">Neu – AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="980a4-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="980a4-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="980a4-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


