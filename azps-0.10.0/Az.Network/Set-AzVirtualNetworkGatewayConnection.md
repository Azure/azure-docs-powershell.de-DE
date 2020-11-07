---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843571"
---
# <span data-ttu-id="e77c7-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e77c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e77c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e77c7-103">Konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e77c7-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e77c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e77c7-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e77c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e77c7-105">DESCRIPTION</span></span>
<span data-ttu-id="e77c7-106">Das Cmdlet " **Satz-AzVirtualNetworkGatewayConnection** " konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e77c7-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="e77c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e77c7-107">EXAMPLES</span></span>

### <span data-ttu-id="e77c7-108">1:</span><span class="sxs-lookup"><span data-stu-id="e77c7-108">1:</span></span>
```

```

## <span data-ttu-id="e77c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e77c7-109">PARAMETERS</span></span>

### <span data-ttu-id="e77c7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e77c7-110">-AsJob</span></span>
<span data-ttu-id="e77c7-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e77c7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e77c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77c7-112">-DefaultProfile</span></span>
<span data-ttu-id="e77c7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e77c7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e77c7-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e77c7-114">-EnableBgp</span></span>
<span data-ttu-id="e77c7-115">Ob eine BGP-Sitzung über einen S2S-VPN-Tunnel verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="e77c7-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="e77c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e77c7-116">-Force</span></span>
<span data-ttu-id="e77c7-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e77c7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e77c7-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="e77c7-118">-IpsecPolicies</span></span>
<span data-ttu-id="e77c7-119">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="e77c7-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="e77c7-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="e77c7-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="e77c7-121">Ob richtlinienbasierte Datenverkehrs Auswahl für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="e77c7-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="e77c7-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e77c7-123">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das dieses Cmdlet zum Ändern der virtuellen Netzwerkgateway-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e77c7-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e77c7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e77c7-124">-Confirm</span></span>
<span data-ttu-id="e77c7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e77c7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77c7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77c7-126">-WhatIf</span></span>
<span data-ttu-id="e77c7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e77c7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77c7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e77c7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77c7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77c7-129">CommonParameters</span></span>
<span data-ttu-id="e77c7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77c7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77c7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e77c7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77c7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e77c7-132">INPUTS</span></span>

### <span data-ttu-id="e77c7-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="e77c7-134">Der Parameter "VirtualNetworkGatewayConnection" akzeptiert den Wert vom Typ "PSVirtualNetworkGatewayConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e77c7-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="e77c7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e77c7-135">OUTPUTS</span></span>

### <span data-ttu-id="e77c7-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="e77c7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e77c7-137">NOTES</span></span>

## <span data-ttu-id="e77c7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e77c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="e77c7-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e77c7-140">Neu – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="e77c7-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e77c7-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


