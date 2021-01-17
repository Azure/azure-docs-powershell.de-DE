---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98461016"
---
# <span data-ttu-id="a99a6-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="a99a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a99a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a99a6-103">Ändert einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a99a6-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="a99a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a99a6-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99a6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a99a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a99a6-106">Das **Cmdlet Set-AzExpressRoutePort** speichert den geänderten ExpressRoutePort in Azure.</span><span class="sxs-lookup"><span data-stu-id="a99a6-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="a99a6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a99a6-107">EXAMPLES</span></span>

### <span data-ttu-id="a99a6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a99a6-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="a99a6-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a99a6-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="a99a6-110">Ändert den Administratorstatus eines Links eines ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="a99a6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a99a6-111">PARAMETERS</span></span>

### <span data-ttu-id="a99a6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a99a6-112">-AsJob</span></span>
<span data-ttu-id="a99a6-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a99a6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a99a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99a6-114">-DefaultProfile</span></span>
<span data-ttu-id="a99a6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a99a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a99a6-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-116">-ExpressRoutePort</span></span>
<span data-ttu-id="a99a6-117">Das ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a99a6-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="a99a6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a99a6-118">-Confirm</span></span>
<span data-ttu-id="a99a6-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a99a6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99a6-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a99a6-120">-WhatIf</span></span>
<span data-ttu-id="a99a6-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a99a6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99a6-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a99a6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99a6-123">CommonParameters</span></span>
<span data-ttu-id="a99a6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99a6-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99a6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99a6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a99a6-126">INPUTS</span></span>

### <span data-ttu-id="a99a6-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a99a6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a99a6-128">OUTPUTS</span></span>

### <span data-ttu-id="a99a6-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a99a6-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a99a6-130">NOTES</span></span>

## <span data-ttu-id="a99a6-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a99a6-131">RELATED LINKS</span></span>

[<span data-ttu-id="a99a6-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="a99a6-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="a99a6-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a99a6-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
