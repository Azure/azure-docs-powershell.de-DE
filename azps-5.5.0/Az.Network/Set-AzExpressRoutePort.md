---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172451"
---
# <span data-ttu-id="956e6-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="956e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956e6-102">SYNOPSIS</span></span>
<span data-ttu-id="956e6-103">Ändert einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="956e6-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="956e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="956e6-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="956e6-105">DESCRIPTION</span></span>
<span data-ttu-id="956e6-106">Das **Cmdlet Set-AzExpressRoutePort** speichert den geänderten ExpressRoutePort in Azure.</span><span class="sxs-lookup"><span data-stu-id="956e6-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="956e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="956e6-107">EXAMPLES</span></span>

### <span data-ttu-id="956e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="956e6-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="956e6-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="956e6-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="956e6-110">Ändert den Administratorstatus eines Links eines ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="956e6-111">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="956e6-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="956e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="956e6-112">PARAMETERS</span></span>

### <span data-ttu-id="956e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="956e6-113">-AsJob</span></span>
<span data-ttu-id="956e6-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="956e6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="956e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956e6-115">-DefaultProfile</span></span>
<span data-ttu-id="956e6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="956e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="956e6-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-117">-ExpressRoutePort</span></span>
<span data-ttu-id="956e6-118">Das ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="956e6-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="956e6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="956e6-119">-Confirm</span></span>
<span data-ttu-id="956e6-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="956e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956e6-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="956e6-121">-WhatIf</span></span>
<span data-ttu-id="956e6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="956e6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956e6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="956e6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956e6-124">CommonParameters</span></span>
<span data-ttu-id="956e6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956e6-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956e6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956e6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="956e6-127">INPUTS</span></span>

### <span data-ttu-id="956e6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="956e6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="956e6-129">OUTPUTS</span></span>

### <span data-ttu-id="956e6-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="956e6-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="956e6-131">NOTES</span></span>

## <span data-ttu-id="956e6-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="956e6-132">RELATED LINKS</span></span>

[<span data-ttu-id="956e6-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="956e6-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="956e6-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="956e6-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
