---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660387"
---
# <span data-ttu-id="589ef-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="589ef-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="589ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="589ef-102">SYNOPSIS</span></span>
<span data-ttu-id="589ef-103">Entfernt eine Express Route-Schaltkreis-Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="589ef-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="589ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="589ef-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="589ef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="589ef-105">DESCRIPTION</span></span>
<span data-ttu-id="589ef-106">Mit dem Cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** wird eine Express Route-Schaltkreis Verbindungskonfiguration entfernt, die einem bestimmten Express-Routen Schaltkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="589ef-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="589ef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="589ef-107">EXAMPLES</span></span>

### <span data-ttu-id="589ef-108">Beispiel 1: Entfernen einer Leitungs Verbindungskonfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="589ef-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="589ef-109">Beispiel 2: Entfernen einer Leitungs Verbindungskonfiguration mithilfe von Rohrleitungen aus einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="589ef-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="589ef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="589ef-110">PARAMETERS</span></span>

### <span data-ttu-id="589ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589ef-111">-DefaultProfile</span></span>
<span data-ttu-id="589ef-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="589ef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="589ef-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="589ef-114">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="589ef-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="589ef-115">-Name</span><span class="sxs-lookup"><span data-stu-id="589ef-115">-Name</span></span>
<span data-ttu-id="589ef-116">Der Name der zu entfernende Leitungs Verbindungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="589ef-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="589ef-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="589ef-117">-Confirm</span></span>
<span data-ttu-id="589ef-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="589ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="589ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589ef-119">-WhatIf</span></span>
<span data-ttu-id="589ef-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="589ef-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="589ef-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="589ef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="589ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589ef-122">CommonParameters</span></span>
<span data-ttu-id="589ef-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589ef-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589ef-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="589ef-125">INPUTS</span></span>

### <span data-ttu-id="589ef-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="589ef-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="589ef-127">OUTPUTS</span></span>

### <span data-ttu-id="589ef-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="589ef-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="589ef-129">NOTES</span></span>

## <span data-ttu-id="589ef-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="589ef-130">RELATED LINKS</span></span>

[<span data-ttu-id="589ef-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="589ef-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="589ef-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="589ef-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="589ef-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="589ef-134">Satz-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="589ef-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="589ef-135">Neu – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="589ef-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="589ef-136">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="589ef-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="589ef-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)