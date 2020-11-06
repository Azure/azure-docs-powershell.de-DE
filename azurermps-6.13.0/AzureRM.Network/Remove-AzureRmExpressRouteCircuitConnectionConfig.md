---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482258"
---
# <span data-ttu-id="893cb-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="893cb-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="893cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="893cb-102">SYNOPSIS</span></span>
<span data-ttu-id="893cb-103">Entfernt eine Express Route-Schaltkreis-Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="893cb-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="893cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="893cb-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="893cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="893cb-105">DESCRIPTION</span></span>
<span data-ttu-id="893cb-106">Mit dem Cmdlet **Remove-AzureRmExpressRouteCircuitConnectionConfig** wird eine Express Route-Schaltkreis Verbindungskonfiguration entfernt, die einem bestimmten Express-Routen Schaltkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="893cb-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="893cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="893cb-107">EXAMPLES</span></span>

### <span data-ttu-id="893cb-108">Beispiel 1: Entfernen einer Leitungs Verbindungskonfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="893cb-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="893cb-109">Beispiel 2: Entfernen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen aus einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="893cb-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="893cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="893cb-110">PARAMETERS</span></span>

### <span data-ttu-id="893cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893cb-111">-DefaultProfile</span></span>
<span data-ttu-id="893cb-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="893cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893cb-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="893cb-114">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="893cb-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="893cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="893cb-115">-Name</span></span>
<span data-ttu-id="893cb-116">Der Name der zu entfernende Leitungs Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="893cb-116">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893cb-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="893cb-117">-Confirm</span></span>
<span data-ttu-id="893cb-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="893cb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893cb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893cb-119">-WhatIf</span></span>
<span data-ttu-id="893cb-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893cb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="893cb-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="893cb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893cb-122">CommonParameters</span></span>
<span data-ttu-id="893cb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893cb-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893cb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893cb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="893cb-125">INPUTS</span></span>

### <span data-ttu-id="893cb-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="893cb-127">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="893cb-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="893cb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="893cb-128">OUTPUTS</span></span>

### <span data-ttu-id="893cb-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="893cb-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="893cb-130">NOTES</span></span>

## <span data-ttu-id="893cb-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="893cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="893cb-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="893cb-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="893cb-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="893cb-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="893cb-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="893cb-135">Satz-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="893cb-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="893cb-136">Neu – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="893cb-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="893cb-137">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="893cb-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893cb-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
