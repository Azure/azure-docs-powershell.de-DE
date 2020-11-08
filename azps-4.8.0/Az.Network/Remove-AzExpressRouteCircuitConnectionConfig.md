---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174307"
---
# <span data-ttu-id="dc649-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc649-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="dc649-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc649-102">SYNOPSIS</span></span>
<span data-ttu-id="dc649-103">Entfernt eine Express Route-Schaltkreis-Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc649-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="dc649-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc649-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc649-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc649-105">DESCRIPTION</span></span>
<span data-ttu-id="dc649-106">Mit dem Cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** wird eine Express Route-Schaltkreis Verbindungskonfiguration entfernt, die einem bestimmten Express-Routen Schaltkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dc649-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="dc649-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc649-107">EXAMPLES</span></span>

### <span data-ttu-id="dc649-108">Beispiel 1: Entfernen einer Leitungs Verbindungskonfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="dc649-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="dc649-109">Beispiel 2: Entfernen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen aus einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="dc649-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="dc649-110">Beispiel 3: Entfernen einer Leitungs Verbindungskonfiguration von einem Express Route-Schaltkreis für eine bestimmte Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="dc649-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="dc649-111">Beispiel 4: Entfernen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen aus einem Express Route-Schaltkreis für eine bestimmte Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="dc649-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="dc649-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc649-112">PARAMETERS</span></span>

### <span data-ttu-id="dc649-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc649-113">-DefaultProfile</span></span>
<span data-ttu-id="dc649-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc649-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc649-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="dc649-116">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc649-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="dc649-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dc649-117">-Name</span></span>
<span data-ttu-id="dc649-118">Der Name der zu entfernende Leitungs Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc649-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="dc649-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="dc649-119">-AddressPrefixType</span></span>
<span data-ttu-id="dc649-120">Gibt die Adressfamilie an, die aus der config entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="dc649-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc649-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc649-121">-Confirm</span></span>
<span data-ttu-id="dc649-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc649-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc649-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc649-123">-WhatIf</span></span>
<span data-ttu-id="dc649-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc649-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc649-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc649-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc649-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc649-126">CommonParameters</span></span>
<span data-ttu-id="dc649-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc649-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc649-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc649-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc649-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc649-129">INPUTS</span></span>

### <span data-ttu-id="dc649-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="dc649-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc649-131">OUTPUTS</span></span>

### <span data-ttu-id="dc649-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="dc649-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc649-133">NOTES</span></span>

## <span data-ttu-id="dc649-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc649-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc649-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="dc649-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc649-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dc649-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc649-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dc649-138">Satz-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc649-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dc649-139">Neu – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dc649-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="dc649-140">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="dc649-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dc649-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)