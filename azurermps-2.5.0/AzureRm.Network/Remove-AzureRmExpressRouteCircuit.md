---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848128"
---
# <span data-ttu-id="a9d43-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d43-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="a9d43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9d43-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d43-103">Entfernt einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="a9d43-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d43-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9d43-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d43-106">Mit dem Cmdlet **Remove-AzureRmExpressRouteCircuit** wird ein Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9d43-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a9d43-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9d43-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d43-108">Beispiel 1: Löschen eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="a9d43-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a9d43-109">Beispiel 2: Löschen eines Express Route-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9d43-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="a9d43-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d43-110">PARAMETERS</span></span>

### <span data-ttu-id="a9d43-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9d43-111">-AsJob</span></span>
<span data-ttu-id="a9d43-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a9d43-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9d43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d43-113">-DefaultProfile</span></span>
<span data-ttu-id="a9d43-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9d43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9d43-115">-Force</span></span>
<span data-ttu-id="a9d43-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a9d43-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9d43-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9d43-117">-Name</span></span>
<span data-ttu-id="a9d43-118">Der Name des Express Route-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9d43-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="a9d43-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9d43-119">-PassThru</span></span>
<span data-ttu-id="a9d43-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a9d43-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a9d43-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a9d43-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9d43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d43-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9d43-123">Gibt den Namen der Ressourcengruppe an, zu der dieser Express Route-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="a9d43-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="a9d43-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9d43-124">-Confirm</span></span>
<span data-ttu-id="a9d43-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9d43-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d43-126">-WhatIf</span></span>
<span data-ttu-id="a9d43-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9d43-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d43-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9d43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d43-129">CommonParameters</span></span>
<span data-ttu-id="a9d43-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d43-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d43-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d43-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9d43-132">INPUTS</span></span>

## <span data-ttu-id="a9d43-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9d43-133">OUTPUTS</span></span>

## <span data-ttu-id="a9d43-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9d43-134">NOTES</span></span>

## <span data-ttu-id="a9d43-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9d43-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9d43-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d43-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a9d43-137">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d43-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a9d43-138">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d43-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a9d43-139">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d43-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
