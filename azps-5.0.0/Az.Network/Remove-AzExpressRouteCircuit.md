---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179850"
---
# <span data-ttu-id="b1bc6-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b1bc6-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b1bc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1bc6-103">Entfernt einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b1bc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1bc6-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1bc6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1bc6-105">DESCRIPTION</span></span>
<span data-ttu-id="b1bc6-106">Mit dem Cmdlet **Remove-AzExpressRouteCircuit** wird ein Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b1bc6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1bc6-107">EXAMPLES</span></span>

### <span data-ttu-id="b1bc6-108">Beispiel 1: Löschen eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="b1bc6-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="b1bc6-109">Beispiel 2: Löschen eines Express Route-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b1bc6-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="b1bc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1bc6-110">PARAMETERS</span></span>

### <span data-ttu-id="b1bc6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1bc6-111">-AsJob</span></span>
<span data-ttu-id="b1bc6-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b1bc6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1bc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1bc6-113">-DefaultProfile</span></span>
<span data-ttu-id="b1bc6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1bc6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b1bc6-115">-Force</span></span>
<span data-ttu-id="b1bc6-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1bc6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b1bc6-117">-Name</span></span>
<span data-ttu-id="b1bc6-118">Der Name des Express Route-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="b1bc6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1bc6-119">-PassThru</span></span>
<span data-ttu-id="b1bc6-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b1bc6-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1bc6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1bc6-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1bc6-123">Gibt den Namen der Ressourcengruppe an, zu der dieser Express Route-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="b1bc6-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1bc6-124">-Confirm</span></span>
<span data-ttu-id="b1bc6-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1bc6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1bc6-126">-WhatIf</span></span>
<span data-ttu-id="b1bc6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1bc6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1bc6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1bc6-129">CommonParameters</span></span>
<span data-ttu-id="b1bc6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1bc6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1bc6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1bc6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1bc6-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1bc6-132">INPUTS</span></span>

### <span data-ttu-id="b1bc6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b1bc6-133">System.String</span></span>

## <span data-ttu-id="b1bc6-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1bc6-134">OUTPUTS</span></span>

### <span data-ttu-id="b1bc6-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1bc6-135">System.Boolean</span></span>

## <span data-ttu-id="b1bc6-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1bc6-136">NOTES</span></span>

## <span data-ttu-id="b1bc6-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1bc6-137">RELATED LINKS</span></span>

[<span data-ttu-id="b1bc6-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b1bc6-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b1bc6-139">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b1bc6-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="b1bc6-140">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b1bc6-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="b1bc6-141">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b1bc6-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
