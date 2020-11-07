---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849164"
---
# <span data-ttu-id="8af7d-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="8af7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8af7d-102">SYNOPSIS</span></span>
<span data-ttu-id="8af7d-103">Verschiebt einen Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="8af7d-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8af7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af7d-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8af7d-105">DESCRIPTION</span></span>
<span data-ttu-id="8af7d-106">Mit dem Cmdlet **Move-AzureRmExpressRouteCircuit** wird ein Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers verschoben.</span><span class="sxs-lookup"><span data-stu-id="8af7d-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="8af7d-107">Nach dem Verschieben verhält sich der Express Route-Schaltkreis wie jeder andere Express Route-Schaltkreis, der im Bereitstellungsmodell des Ressourcen-Managers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8af7d-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="8af7d-108">Schaltkreis Links, virtuelle Netzwerke und VPN-Gateways werden nicht durch diesen Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="8af7d-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="8af7d-109">Diese Ressourcen müssen nach dem Umzug neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8af7d-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="8af7d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8af7d-110">EXAMPLES</span></span>

### <span data-ttu-id="8af7d-111">Beispiel 1: Verschieben eines Express Route-Schaltkreises in das Bereitstellungsmodell des Ressourcen-Managers</span><span class="sxs-lookup"><span data-stu-id="8af7d-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="8af7d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af7d-112">PARAMETERS</span></span>

### <span data-ttu-id="8af7d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8af7d-113">-AsJob</span></span>
<span data-ttu-id="8af7d-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8af7d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8af7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af7d-115">-DefaultProfile</span></span>
<span data-ttu-id="8af7d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8af7d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8af7d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8af7d-117">-Force</span></span>
<span data-ttu-id="8af7d-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8af7d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8af7d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="8af7d-119">-Location</span></span>
<span data-ttu-id="8af7d-120">Der Name der Azure-Position, an der sich der Express Route-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="8af7d-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="8af7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8af7d-121">-Name</span></span>
<span data-ttu-id="8af7d-122">Der Name des Express Route-Schaltkreises, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8af7d-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="8af7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8af7d-124">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="8af7d-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="8af7d-125">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="8af7d-125">-ServiceKey</span></span>
<span data-ttu-id="8af7d-126">Der Dienstschlüssel, der vom Express Route-Schaltkreis im klassischen Bereitstellungsmodell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8af7d-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="8af7d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="8af7d-127">-Tag</span></span>
<span data-ttu-id="8af7d-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8af7d-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8af7d-129">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8af7d-129">For example:</span></span>

<span data-ttu-id="8af7d-130">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8af7d-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8af7d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8af7d-131">-Confirm</span></span>
<span data-ttu-id="8af7d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8af7d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af7d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af7d-133">-WhatIf</span></span>
<span data-ttu-id="8af7d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8af7d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af7d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8af7d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af7d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af7d-136">CommonParameters</span></span>
<span data-ttu-id="8af7d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af7d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af7d-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af7d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af7d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8af7d-139">INPUTS</span></span>

## <span data-ttu-id="8af7d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8af7d-140">OUTPUTS</span></span>

### <span data-ttu-id="8af7d-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8af7d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8af7d-142">NOTES</span></span>

## <span data-ttu-id="8af7d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8af7d-143">RELATED LINKS</span></span>

[<span data-ttu-id="8af7d-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8af7d-145">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8af7d-146">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8af7d-147">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8af7d-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
