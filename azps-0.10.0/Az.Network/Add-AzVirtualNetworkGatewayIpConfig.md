---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841796"
---
# <span data-ttu-id="490c5-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="490c5-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="490c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="490c5-102">SYNOPSIS</span></span>
<span data-ttu-id="490c5-103">Fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="490c5-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="490c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="490c5-104">SYNTAX</span></span>

### <span data-ttu-id="490c5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="490c5-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="490c5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="490c5-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="490c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="490c5-107">DESCRIPTION</span></span>
<span data-ttu-id="490c5-108">Das Cmdlet **Add-AzVirtualNetworkGatewayIpConfig** fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="490c5-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="490c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="490c5-109">EXAMPLES</span></span>

### <span data-ttu-id="490c5-110">1:</span><span class="sxs-lookup"><span data-stu-id="490c5-110">1:</span></span>
```

```

## <span data-ttu-id="490c5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="490c5-111">PARAMETERS</span></span>

### <span data-ttu-id="490c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490c5-112">-DefaultProfile</span></span>
<span data-ttu-id="490c5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="490c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="490c5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="490c5-114">-Name</span></span>
<span data-ttu-id="490c5-115">Gibt den Namen der IP-Gateway-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="490c5-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="490c5-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="490c5-116">-PrivateIpAddress</span></span>
<span data-ttu-id="490c5-117">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="490c5-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="490c5-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="490c5-118">-PublicIpAddress</span></span>
<span data-ttu-id="490c5-119">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="490c5-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="490c5-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="490c5-120">-PublicIpAddressId</span></span>
<span data-ttu-id="490c5-121">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="490c5-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="490c5-122">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="490c5-122">-Subnet</span></span>
<span data-ttu-id="490c5-123">Gibt ein **PSSubnet** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="490c5-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="490c5-124">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="490c5-124">-SubnetId</span></span>
<span data-ttu-id="490c5-125">Gibt die ID des Subnets an.</span><span class="sxs-lookup"><span data-stu-id="490c5-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="490c5-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="490c5-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="490c5-127">Gibt ein **PSVirtualNetworkGateway** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="490c5-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="490c5-128">Dieses Cmdlet ändert das von Ihnen angegebene **PSVirtualNetworkGateway** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="490c5-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="490c5-129">Sie können das Get-AzVirtualNetworkGateway-Cmdlet verwenden, um ein **PSVirtualNetworkGateway** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="490c5-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="490c5-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="490c5-130">-Confirm</span></span>
<span data-ttu-id="490c5-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="490c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="490c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="490c5-132">-WhatIf</span></span>
<span data-ttu-id="490c5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="490c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="490c5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="490c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="490c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490c5-135">CommonParameters</span></span>
<span data-ttu-id="490c5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490c5-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="490c5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490c5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="490c5-138">INPUTS</span></span>

### <span data-ttu-id="490c5-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="490c5-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="490c5-140">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="490c5-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="490c5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="490c5-141">OUTPUTS</span></span>

### <span data-ttu-id="490c5-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="490c5-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="490c5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="490c5-143">NOTES</span></span>

## <span data-ttu-id="490c5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="490c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="490c5-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="490c5-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="490c5-146">Neu – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="490c5-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="490c5-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="490c5-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


