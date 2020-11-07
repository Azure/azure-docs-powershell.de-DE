---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849931"
---
# <span data-ttu-id="0a925-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0a925-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a925-102">SYNOPSIS</span></span>
<span data-ttu-id="0a925-103">Konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0a925-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a925-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a925-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a925-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a925-105">DESCRIPTION</span></span>
<span data-ttu-id="0a925-106">Das Cmdlet " **Satz-AzureRmVirtualNetworkGatewayConnection** " konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0a925-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="0a925-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a925-107">EXAMPLES</span></span>

### <span data-ttu-id="0a925-108">1:</span><span class="sxs-lookup"><span data-stu-id="0a925-108">1:</span></span>
```

```

## <span data-ttu-id="0a925-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a925-109">PARAMETERS</span></span>

### <span data-ttu-id="0a925-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a925-110">-AsJob</span></span>
<span data-ttu-id="0a925-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a925-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a925-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a925-112">-DefaultProfile</span></span>
<span data-ttu-id="0a925-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a925-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a925-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0a925-114">-EnableBgp</span></span>
<span data-ttu-id="0a925-115">Ob eine BGP-Sitzung über einen S2S-VPN-Tunnel verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="0a925-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="0a925-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0a925-116">-Force</span></span>
<span data-ttu-id="0a925-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0a925-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a925-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="0a925-118">-IpsecPolicies</span></span>
<span data-ttu-id="0a925-119">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="0a925-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="0a925-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="0a925-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="0a925-121">Ob richtlinienbasierte Datenverkehrs Auswahl für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="0a925-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="0a925-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="0a925-123">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das dieses Cmdlet zum Ändern der virtuellen Netzwerkgateway-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a925-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a925-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a925-124">-Confirm</span></span>
<span data-ttu-id="0a925-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a925-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a925-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a925-126">-WhatIf</span></span>
<span data-ttu-id="0a925-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a925-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a925-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a925-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a925-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a925-129">CommonParameters</span></span>
<span data-ttu-id="0a925-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a925-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a925-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a925-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a925-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a925-132">INPUTS</span></span>

### <span data-ttu-id="0a925-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="0a925-134">Der Parameter "VirtualNetworkGatewayConnection" akzeptiert den Wert vom Typ "PSVirtualNetworkGatewayConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a925-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="0a925-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a925-135">OUTPUTS</span></span>

### <span data-ttu-id="0a925-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="0a925-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a925-137">NOTES</span></span>

## <span data-ttu-id="0a925-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a925-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a925-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0a925-140">Neu – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="0a925-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a925-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


