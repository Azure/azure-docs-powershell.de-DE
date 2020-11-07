---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 4dbddf7e78297acc3f12f69dd2a44f9698f7b891
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841167"
---
# <span data-ttu-id="6d3c7-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d3c7-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="6d3c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3c7-103">Entfernt einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6d3c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d3c7-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d3c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d3c7-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3c7-106">Mit dem Cmdlet **Remove-AzExpressRouteCircuit** wird ein Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6d3c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d3c7-107">EXAMPLES</span></span>

### <span data-ttu-id="6d3c7-108">Beispiel 1: Löschen eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="6d3c7-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="6d3c7-109">Beispiel 2: Löschen eines Express Route-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="6d3c7-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="6d3c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d3c7-110">PARAMETERS</span></span>

### <span data-ttu-id="6d3c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d3c7-111">-AsJob</span></span>
<span data-ttu-id="6d3c7-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6d3c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d3c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3c7-113">-DefaultProfile</span></span>
<span data-ttu-id="6d3c7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d3c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6d3c7-115">-Force</span></span>
<span data-ttu-id="6d3c7-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d3c7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6d3c7-117">-Name</span></span>
<span data-ttu-id="6d3c7-118">Der Name des Express Route-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="6d3c7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d3c7-119">-PassThru</span></span>
<span data-ttu-id="6d3c7-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6d3c7-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6d3c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d3c7-123">Gibt den Namen der Ressourcengruppe an, zu der dieser Express Route-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="6d3c7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d3c7-124">-Confirm</span></span>
<span data-ttu-id="6d3c7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d3c7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3c7-126">-WhatIf</span></span>
<span data-ttu-id="6d3c7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d3c7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d3c7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3c7-129">CommonParameters</span></span>
<span data-ttu-id="6d3c7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3c7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3c7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3c7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3c7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d3c7-132">INPUTS</span></span>

## <span data-ttu-id="6d3c7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d3c7-133">OUTPUTS</span></span>

## <span data-ttu-id="6d3c7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d3c7-134">NOTES</span></span>

## <span data-ttu-id="6d3c7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d3c7-135">RELATED LINKS</span></span>

[<span data-ttu-id="6d3c7-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d3c7-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6d3c7-137">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d3c7-137">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="6d3c7-138">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d3c7-138">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="6d3c7-139">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d3c7-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
