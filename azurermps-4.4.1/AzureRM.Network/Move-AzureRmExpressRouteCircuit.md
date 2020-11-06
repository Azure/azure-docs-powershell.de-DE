---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499961"
---
# <span data-ttu-id="7b09d-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="7b09d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b09d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b09d-103">Verschiebt einen Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="7b09d-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b09d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b09d-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b09d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b09d-105">DESCRIPTION</span></span>
<span data-ttu-id="7b09d-106">Mit dem Cmdlet **Move-AzureRmExpressRouteCircuit** wird ein Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers verschoben.</span><span class="sxs-lookup"><span data-stu-id="7b09d-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="7b09d-107">Nach dem Verschieben verhält sich der Express Route-Schaltkreis wie jeder andere Express Route-Schaltkreis, der im Bereitstellungsmodell des Ressourcen-Managers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7b09d-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="7b09d-108">Schaltkreis Links, virtuelle Netzwerke und VPN-Gateways werden nicht durch diesen Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="7b09d-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="7b09d-109">Diese Ressourcen müssen nach dem Umzug neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7b09d-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="7b09d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b09d-110">EXAMPLES</span></span>

### <span data-ttu-id="7b09d-111">Beispiel 1: Verschieben eines Express Route-Schaltkreises in das Bereitstellungsmodell des Ressourcen-Managers</span><span class="sxs-lookup"><span data-stu-id="7b09d-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="7b09d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b09d-112">PARAMETERS</span></span>

### <span data-ttu-id="7b09d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7b09d-113">-Force</span></span>
<span data-ttu-id="7b09d-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7b09d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b09d-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="7b09d-115">-Location</span></span>
<span data-ttu-id="7b09d-116">Der Name der Azure-Position, an der sich der Express Route-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="7b09d-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b09d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b09d-117">-Name</span></span>
<span data-ttu-id="7b09d-118">Der Name des Express Route-Schaltkreises, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b09d-118">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b09d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b09d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7b09d-120">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="7b09d-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b09d-121">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="7b09d-121">-ServiceKey</span></span>
<span data-ttu-id="7b09d-122">Der Dienstschlüssel, der vom Express Route-Schaltkreis im klassischen Bereitstellungsmodell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b09d-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b09d-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b09d-123">-Tag</span></span>
<span data-ttu-id="7b09d-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="7b09d-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b09d-125">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7b09d-125">For example:</span></span>

<span data-ttu-id="7b09d-126">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7b09d-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b09d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b09d-127">-Confirm</span></span>
<span data-ttu-id="7b09d-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b09d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b09d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b09d-129">-WhatIf</span></span>
<span data-ttu-id="7b09d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b09d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b09d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b09d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b09d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b09d-132">-DefaultProfile</span></span>
<span data-ttu-id="7b09d-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b09d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b09d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b09d-134">CommonParameters</span></span>
<span data-ttu-id="7b09d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b09d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b09d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b09d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b09d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b09d-137">INPUTS</span></span>

## <span data-ttu-id="7b09d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b09d-138">OUTPUTS</span></span>

### <span data-ttu-id="7b09d-139">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b09d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b09d-140">NOTES</span></span>

## <span data-ttu-id="7b09d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b09d-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b09d-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7b09d-143">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7b09d-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7b09d-145">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b09d-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
