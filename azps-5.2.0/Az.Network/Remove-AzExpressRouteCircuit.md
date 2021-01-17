---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356683"
---
# <span data-ttu-id="77aff-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77aff-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="77aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77aff-102">SYNOPSIS</span></span>
<span data-ttu-id="77aff-103">Entfernt einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="77aff-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="77aff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77aff-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77aff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77aff-105">DESCRIPTION</span></span>
<span data-ttu-id="77aff-106">Das **Cmdlet "Remove-AzExpressRouteCircuit"** entfernt einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="77aff-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="77aff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77aff-107">EXAMPLES</span></span>

### <span data-ttu-id="77aff-108">Beispiel 1: Löschen eines ExpressRoute-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="77aff-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="77aff-109">Beispiel 2: Löschen eines "ExpressRoute"-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="77aff-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="77aff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77aff-110">PARAMETERS</span></span>

### <span data-ttu-id="77aff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77aff-111">-AsJob</span></span>
<span data-ttu-id="77aff-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="77aff-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77aff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77aff-113">-DefaultProfile</span></span>
<span data-ttu-id="77aff-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77aff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77aff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77aff-115">-Force</span></span>
<span data-ttu-id="77aff-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="77aff-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77aff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="77aff-117">-Name</span></span>
<span data-ttu-id="77aff-118">Der Name des zu entfernende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="77aff-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="77aff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77aff-119">-PassThru</span></span>
<span data-ttu-id="77aff-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="77aff-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="77aff-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="77aff-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77aff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77aff-122">-ResourceGroupName</span></span>
<span data-ttu-id="77aff-123">Gibt den Namen der Ressourcengruppe an, zu der dieser "ExpressRoute"-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="77aff-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="77aff-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77aff-124">-Confirm</span></span>
<span data-ttu-id="77aff-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77aff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77aff-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="77aff-126">-WhatIf</span></span>
<span data-ttu-id="77aff-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77aff-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77aff-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77aff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77aff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77aff-129">CommonParameters</span></span>
<span data-ttu-id="77aff-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77aff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77aff-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77aff-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77aff-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77aff-132">INPUTS</span></span>

### <span data-ttu-id="77aff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="77aff-133">System.String</span></span>

## <span data-ttu-id="77aff-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77aff-134">OUTPUTS</span></span>

### <span data-ttu-id="77aff-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77aff-135">System.Boolean</span></span>

## <span data-ttu-id="77aff-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="77aff-136">NOTES</span></span>

## <span data-ttu-id="77aff-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="77aff-137">RELATED LINKS</span></span>

[<span data-ttu-id="77aff-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77aff-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="77aff-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77aff-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="77aff-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77aff-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="77aff-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77aff-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
