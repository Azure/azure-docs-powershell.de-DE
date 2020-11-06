---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481801"
---
# <span data-ttu-id="77985-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77985-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77985-102">SYNOPSIS</span></span>
<span data-ttu-id="77985-103">Konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="77985-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77985-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77985-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77985-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77985-105">DESCRIPTION</span></span>
<span data-ttu-id="77985-106">Das Cmdlet " **Satz-AzureRmVirtualNetworkGatewayConnection** " konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="77985-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="77985-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77985-107">EXAMPLES</span></span>

## <span data-ttu-id="77985-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="77985-108">PARAMETERS</span></span>

### <span data-ttu-id="77985-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="77985-109">-EnableBgp</span></span>
<span data-ttu-id="77985-110">Ob eine BGP-Sitzung über einen S2S-VPN-Tunnel verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="77985-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77985-111">-Force</span><span class="sxs-lookup"><span data-stu-id="77985-111">-Force</span></span>
<span data-ttu-id="77985-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="77985-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77985-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="77985-113">-IpsecPolicies</span></span>
<span data-ttu-id="77985-114">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="77985-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="77985-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="77985-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="77985-116">Ob richtlinienbasierte Datenverkehrs Auswahl für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="77985-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77985-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="77985-118">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das dieses Cmdlet zum Ändern der virtuellen Netzwerkgateway-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="77985-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77985-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77985-119">-Confirm</span></span>
<span data-ttu-id="77985-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77985-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77985-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77985-121">-WhatIf</span></span>
<span data-ttu-id="77985-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77985-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77985-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77985-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77985-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77985-124">-DefaultProfile</span></span>
<span data-ttu-id="77985-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77985-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77985-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77985-126">CommonParameters</span></span>
<span data-ttu-id="77985-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77985-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77985-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77985-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77985-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77985-129">INPUTS</span></span>

### <span data-ttu-id="77985-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="77985-131">Der Parameter "VirtualNetworkGatewayConnection" akzeptiert den Wert vom Typ "PSVirtualNetworkGatewayConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="77985-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="77985-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77985-132">OUTPUTS</span></span>

### <span data-ttu-id="77985-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77985-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="77985-134">NOTES</span></span>

## <span data-ttu-id="77985-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77985-135">RELATED LINKS</span></span>

[<span data-ttu-id="77985-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77985-137">Neu – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77985-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77985-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


