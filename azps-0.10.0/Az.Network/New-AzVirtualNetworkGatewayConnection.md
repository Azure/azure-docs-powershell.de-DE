---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 7aede18c438faca196d696a69e7f7651edac132e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841255"
---
# <span data-ttu-id="9fe64-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9fe64-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9fe64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fe64-102">SYNOPSIS</span></span>

## <span data-ttu-id="9fe64-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe64-103">SYNTAX</span></span>

### <span data-ttu-id="9fe64-104">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fe64-104">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe64-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe64-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe64-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe64-106">DESCRIPTION</span></span>

## <span data-ttu-id="9fe64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fe64-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe64-108">1:</span><span class="sxs-lookup"><span data-stu-id="9fe64-108">1:</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="9fe64-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe64-109">PARAMETERS</span></span>

### <span data-ttu-id="9fe64-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fe64-110">-AsJob</span></span>
<span data-ttu-id="9fe64-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9fe64-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="9fe64-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="9fe64-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe64-114">-DefaultProfile</span></span>
<span data-ttu-id="9fe64-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fe64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe64-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="9fe64-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9fe64-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="9fe64-118">-IpsecPolicies</span></span>
<span data-ttu-id="9fe64-119">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="9fe64-119">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="9fe64-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="9fe64-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9fe64-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="9fe64-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-124">-Peer-Nr</span><span class="sxs-lookup"><span data-stu-id="9fe64-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe64-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="9fe64-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9fe64-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fe64-128">-Tag</span></span>
<span data-ttu-id="9fe64-129">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="9fe64-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9fe64-130">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9fe64-130">For example:</span></span>

<span data-ttu-id="9fe64-131">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9fe64-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="9fe64-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="9fe64-133">Verwenden richtlinienbasierter Datenverkehrs Auswahlen für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="9fe64-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="9fe64-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="9fe64-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe64-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fe64-136">-Confirm</span></span>
<span data-ttu-id="9fe64-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fe64-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe64-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe64-138">-WhatIf</span></span>
<span data-ttu-id="9fe64-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe64-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe64-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fe64-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe64-141">CommonParameters</span></span>
<span data-ttu-id="9fe64-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe64-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe64-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe64-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fe64-144">INPUTS</span></span>

## <span data-ttu-id="9fe64-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fe64-145">OUTPUTS</span></span>

### <span data-ttu-id="9fe64-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9fe64-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9fe64-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fe64-147">NOTES</span></span>

## <span data-ttu-id="9fe64-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fe64-148">RELATED LINKS</span></span>

[<span data-ttu-id="9fe64-149">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9fe64-149">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9fe64-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9fe64-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9fe64-151">Satz-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9fe64-151">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
