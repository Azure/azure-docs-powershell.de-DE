---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479750"
---
# <span data-ttu-id="67856-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67856-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="67856-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67856-102">SYNOPSIS</span></span>
<span data-ttu-id="67856-103">Fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="67856-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67856-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67856-104">SYNTAX</span></span>

### <span data-ttu-id="67856-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="67856-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67856-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="67856-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67856-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67856-107">DESCRIPTION</span></span>
<span data-ttu-id="67856-108">Das Cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** fügt eine IP-Konfiguration zu einem virtuellen Netzwerkgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="67856-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="67856-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67856-109">EXAMPLES</span></span>

## <span data-ttu-id="67856-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67856-110">PARAMETERS</span></span>

### <span data-ttu-id="67856-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67856-111">-DefaultProfile</span></span>
<span data-ttu-id="67856-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67856-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67856-113">-Name</span><span class="sxs-lookup"><span data-stu-id="67856-113">-Name</span></span>
<span data-ttu-id="67856-114">Gibt den Namen der IP-Gateway-Konfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="67856-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="67856-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="67856-115">-PrivateIpAddress</span></span>
<span data-ttu-id="67856-116">Gibt die private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="67856-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="67856-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67856-117">-PublicIpAddress</span></span>
<span data-ttu-id="67856-118">Gibt die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="67856-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="67856-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="67856-119">-PublicIpAddressId</span></span>
<span data-ttu-id="67856-120">Gibt die ID der öffentlichen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="67856-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="67856-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="67856-121">-Subnet</span></span>
<span data-ttu-id="67856-122">Gibt ein **PSSubnet** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="67856-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="67856-123">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="67856-123">-SubnetId</span></span>
<span data-ttu-id="67856-124">Gibt die ID des Subnets an.</span><span class="sxs-lookup"><span data-stu-id="67856-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="67856-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67856-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="67856-126">Gibt ein **PSVirtualNetworkGateway** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="67856-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="67856-127">Dieses Cmdlet ändert das von Ihnen angegebene **PSVirtualNetworkGateway** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="67856-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="67856-128">Sie können das Get-AzureRmVirtualNetworkGateway-Cmdlet verwenden, um ein **PSVirtualNetworkGateway** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="67856-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="67856-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67856-129">-Confirm</span></span>
<span data-ttu-id="67856-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67856-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67856-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67856-131">-WhatIf</span></span>
<span data-ttu-id="67856-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67856-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67856-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67856-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67856-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67856-134">CommonParameters</span></span>
<span data-ttu-id="67856-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67856-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67856-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67856-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67856-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67856-137">INPUTS</span></span>

### <span data-ttu-id="67856-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67856-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="67856-139">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="67856-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="67856-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67856-140">OUTPUTS</span></span>

### <span data-ttu-id="67856-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67856-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="67856-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="67856-142">NOTES</span></span>

## <span data-ttu-id="67856-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67856-143">RELATED LINKS</span></span>

[<span data-ttu-id="67856-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67856-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="67856-145">Neu – AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67856-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="67856-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67856-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


