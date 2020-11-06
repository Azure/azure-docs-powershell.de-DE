---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 3ea8e43710d9e195218cc1b96a2656af2a7e2adf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479682"
---
# <span data-ttu-id="ec9a7-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec9a7-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="ec9a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9a7-103">Entfernt einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec9a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9a7-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec9a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9a7-106">Mit dem Cmdlet **Remove-AzureRmExpressRouteCircuit** wird ein Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ec9a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec9a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9a7-108">Beispiel 1: Löschen eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="ec9a7-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="ec9a7-109">Beispiel 2: Löschen eines Express Route-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ec9a7-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="ec9a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec9a7-110">PARAMETERS</span></span>

### <span data-ttu-id="ec9a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec9a7-111">-AsJob</span></span>
<span data-ttu-id="ec9a7-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ec9a7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec9a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9a7-113">-DefaultProfile</span></span>
<span data-ttu-id="ec9a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec9a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ec9a7-115">-Force</span></span>
<span data-ttu-id="ec9a7-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec9a7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ec9a7-117">-Name</span></span>
<span data-ttu-id="ec9a7-118">Der Name des Express Route-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="ec9a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec9a7-119">-PassThru</span></span>
<span data-ttu-id="ec9a7-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ec9a7-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec9a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec9a7-123">Gibt den Namen der Ressourcengruppe an, zu der dieser Express Route-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="ec9a7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec9a7-124">-Confirm</span></span>
<span data-ttu-id="ec9a7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec9a7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9a7-126">-WhatIf</span></span>
<span data-ttu-id="ec9a7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec9a7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec9a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9a7-129">CommonParameters</span></span>
<span data-ttu-id="ec9a7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9a7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9a7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec9a7-132">INPUTS</span></span>

### <span data-ttu-id="ec9a7-133">Keine</span><span class="sxs-lookup"><span data-stu-id="ec9a7-133">None</span></span>
<span data-ttu-id="ec9a7-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ec9a7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec9a7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec9a7-135">OUTPUTS</span></span>

## <span data-ttu-id="ec9a7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec9a7-136">NOTES</span></span>

## <span data-ttu-id="ec9a7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec9a7-137">RELATED LINKS</span></span>

[<span data-ttu-id="ec9a7-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec9a7-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ec9a7-139">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec9a7-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ec9a7-140">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec9a7-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ec9a7-141">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec9a7-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
