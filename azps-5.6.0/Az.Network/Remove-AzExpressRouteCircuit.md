---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 94730c362ae9854179525212971dda5c2ad1feae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941691"
---
# <span data-ttu-id="27b7f-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27b7f-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="27b7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="27b7f-103">Entfernt einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="27b7f-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="27b7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27b7f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b7f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="27b7f-106">Das **Cmdlet Remove-AzExpressRouteCircuit** entfernt einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="27b7f-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="27b7f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="27b7f-108">Beispiel 1: Löschen eines ExpressRoute-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="27b7f-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="27b7f-109">Beispiel 2: Löschen eines ExpressRoute-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="27b7f-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="27b7f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="27b7f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27b7f-111">-AsJob</span></span>
<span data-ttu-id="27b7f-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="27b7f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27b7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b7f-113">-DefaultProfile</span></span>
<span data-ttu-id="27b7f-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27b7f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b7f-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="27b7f-115">-Force</span></span>
<span data-ttu-id="27b7f-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="27b7f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27b7f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27b7f-117">-Name</span></span>
<span data-ttu-id="27b7f-118">Der Name des expressRoute-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27b7f-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="27b7f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27b7f-119">-PassThru</span></span>
<span data-ttu-id="27b7f-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="27b7f-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="27b7f-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="27b7f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27b7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="27b7f-123">Gibt den Namen der Ressourcengruppe an, zu der dieser ExpressRoute-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="27b7f-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="27b7f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27b7f-124">-Confirm</span></span>
<span data-ttu-id="27b7f-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27b7f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b7f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b7f-126">-WhatIf</span></span>
<span data-ttu-id="27b7f-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27b7f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b7f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27b7f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b7f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b7f-129">CommonParameters</span></span>
<span data-ttu-id="27b7f-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b7f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b7f-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b7f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b7f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27b7f-132">INPUTS</span></span>

### <span data-ttu-id="27b7f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27b7f-133">System.String</span></span>

## <span data-ttu-id="27b7f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27b7f-134">OUTPUTS</span></span>

### <span data-ttu-id="27b7f-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27b7f-135">System.Boolean</span></span>

## <span data-ttu-id="27b7f-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="27b7f-136">NOTES</span></span>

## <span data-ttu-id="27b7f-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="27b7f-137">RELATED LINKS</span></span>

[<span data-ttu-id="27b7f-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27b7f-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="27b7f-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27b7f-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="27b7f-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27b7f-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="27b7f-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27b7f-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
