---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924603"
---
# <span data-ttu-id="165a3-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="165a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="165a3-102">SYNOPSIS</span></span>
<span data-ttu-id="165a3-103">Ändert einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="165a3-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="165a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="165a3-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="165a3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="165a3-105">DESCRIPTION</span></span>
<span data-ttu-id="165a3-106">Das **Cmdlet Set-AzExpressRoutePort** speichert den geänderten ExpressRoutePort in Azure.</span><span class="sxs-lookup"><span data-stu-id="165a3-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="165a3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="165a3-107">EXAMPLES</span></span>

### <span data-ttu-id="165a3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="165a3-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="165a3-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="165a3-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="165a3-110">Ändert den Administratorstatus eines Links eines ExpressRoutePorts</span><span class="sxs-lookup"><span data-stu-id="165a3-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="165a3-111">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="165a3-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="165a3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="165a3-112">PARAMETERS</span></span>

### <span data-ttu-id="165a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="165a3-113">-AsJob</span></span>
<span data-ttu-id="165a3-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="165a3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="165a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165a3-115">-DefaultProfile</span></span>
<span data-ttu-id="165a3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="165a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="165a3-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-117">-ExpressRoutePort</span></span>
<span data-ttu-id="165a3-118">Das ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="165a3-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="165a3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="165a3-119">-Confirm</span></span>
<span data-ttu-id="165a3-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="165a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="165a3-121">-WhatIf</span></span>
<span data-ttu-id="165a3-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="165a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="165a3-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="165a3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165a3-124">CommonParameters</span></span>
<span data-ttu-id="165a3-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="165a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165a3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165a3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165a3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="165a3-127">INPUTS</span></span>

### <span data-ttu-id="165a3-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="165a3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="165a3-129">OUTPUTS</span></span>

### <span data-ttu-id="165a3-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="165a3-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="165a3-131">NOTES</span></span>

## <span data-ttu-id="165a3-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="165a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="165a3-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="165a3-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="165a3-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="165a3-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
