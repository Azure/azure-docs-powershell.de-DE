---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497057"
---
# <span data-ttu-id="2d4ad-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="2d4ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4ad-103">Entfernt einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d4ad-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d4ad-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4ad-106">Mit dem Cmdlet **Remove-AzureRmExpressRouteCircuit** wird ein Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2d4ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d4ad-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4ad-108">Beispiel 1: Löschen eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="2d4ad-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="2d4ad-109">Beispiel 2: Löschen eines Express Route-Schaltkreises mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2d4ad-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="2d4ad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d4ad-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4ad-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2d4ad-111">-Force</span></span>
<span data-ttu-id="2d4ad-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d4ad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2d4ad-113">-Name</span></span>
<span data-ttu-id="2d4ad-114">Der Name des Express Route-Schaltkreises, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="2d4ad-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4ad-115">-PassThru</span></span>
<span data-ttu-id="2d4ad-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2d4ad-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d4ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="2d4ad-119">Gibt den Namen der Ressourcengruppe an, zu der dieser Express Route-Schaltkreis gehört.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="2d4ad-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d4ad-120">-Confirm</span></span>
<span data-ttu-id="2d4ad-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4ad-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4ad-122">-WhatIf</span></span>
<span data-ttu-id="2d4ad-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4ad-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4ad-125">-DefaultProfile</span></span>
<span data-ttu-id="2d4ad-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4ad-127">CommonParameters</span></span>
<span data-ttu-id="2d4ad-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4ad-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4ad-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d4ad-130">INPUTS</span></span>

## <span data-ttu-id="2d4ad-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d4ad-131">OUTPUTS</span></span>

## <span data-ttu-id="2d4ad-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d4ad-132">NOTES</span></span>

## <span data-ttu-id="2d4ad-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d4ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d4ad-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2d4ad-135">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2d4ad-136">Neu – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2d4ad-137">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
