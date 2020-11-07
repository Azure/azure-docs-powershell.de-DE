---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: ffa10dca752adaeebbdd6fbf92a6a16b094a3085
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841444"
---
# <span data-ttu-id="c556c-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="c556c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c556c-102">SYNOPSIS</span></span>
<span data-ttu-id="c556c-103">Verschiebt einen Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="c556c-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="c556c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c556c-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c556c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c556c-105">DESCRIPTION</span></span>
<span data-ttu-id="c556c-106">Mit dem Cmdlet **Move-AzExpressRouteCircuit** wird ein Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers verschoben.</span><span class="sxs-lookup"><span data-stu-id="c556c-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="c556c-107">Nach dem Verschieben verhält sich der Express Route-Schaltkreis wie jeder andere Express Route-Schaltkreis, der im Bereitstellungsmodell des Ressourcen-Managers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c556c-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="c556c-108">Schaltkreis Links, virtuelle Netzwerke und VPN-Gateways werden nicht durch diesen Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="c556c-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="c556c-109">Diese Ressourcen müssen nach dem Umzug neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c556c-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="c556c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c556c-110">EXAMPLES</span></span>

### <span data-ttu-id="c556c-111">Beispiel 1: Verschieben eines Express Route-Schaltkreises in das Bereitstellungsmodell des Ressourcen-Managers</span><span class="sxs-lookup"><span data-stu-id="c556c-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="c556c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c556c-112">PARAMETERS</span></span>

### <span data-ttu-id="c556c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c556c-113">-AsJob</span></span>
<span data-ttu-id="c556c-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c556c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c556c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c556c-115">-DefaultProfile</span></span>
<span data-ttu-id="c556c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c556c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c556c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c556c-117">-Force</span></span>
<span data-ttu-id="c556c-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c556c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c556c-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="c556c-119">-Location</span></span>
<span data-ttu-id="c556c-120">Der Name der Azure-Position, an der sich der Express Route-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="c556c-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="c556c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c556c-121">-Name</span></span>
<span data-ttu-id="c556c-122">Der Name des Express Route-Schaltkreises, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c556c-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="c556c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c556c-123">-ResourceGroupName</span></span>
<span data-ttu-id="c556c-124">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="c556c-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="c556c-125">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="c556c-125">-ServiceKey</span></span>
<span data-ttu-id="c556c-126">Der Dienstschlüssel, der vom Express Route-Schaltkreis im klassischen Bereitstellungsmodell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c556c-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="c556c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c556c-127">-Tag</span></span>
<span data-ttu-id="c556c-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c556c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c556c-129">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c556c-129">For example:</span></span>

<span data-ttu-id="c556c-130">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c556c-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c556c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c556c-131">-Confirm</span></span>
<span data-ttu-id="c556c-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c556c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c556c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c556c-133">-WhatIf</span></span>
<span data-ttu-id="c556c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c556c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c556c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c556c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c556c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c556c-136">CommonParameters</span></span>
<span data-ttu-id="c556c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c556c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c556c-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c556c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c556c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c556c-139">INPUTS</span></span>

## <span data-ttu-id="c556c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c556c-140">OUTPUTS</span></span>

### <span data-ttu-id="c556c-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c556c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c556c-142">NOTES</span></span>

## <span data-ttu-id="c556c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c556c-143">RELATED LINKS</span></span>

[<span data-ttu-id="c556c-144">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-144">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c556c-145">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-145">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="c556c-146">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-146">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="c556c-147">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c556c-147">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
