---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938531"
---
# <span data-ttu-id="d9a01-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="d9a01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a01-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a01-103">Aktualisiert einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="d9a01-103">Updates a route filter.</span></span>

## <span data-ttu-id="d9a01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9a01-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9a01-105">DESCRIPTION</span></span>
<span data-ttu-id="d9a01-106">Das **Cmdlet Set-AzApplicationGateway** aktualisiert einen Routenfilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="d9a01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9a01-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a01-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9a01-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="d9a01-109">Mit diesem Befehl wird der Routenfilter mit Einstellungen in der Variablen $rf aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d9a01-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="d9a01-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9a01-110">PARAMETERS</span></span>

### <span data-ttu-id="d9a01-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9a01-111">-AsJob</span></span>
<span data-ttu-id="d9a01-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9a01-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9a01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a01-113">-DefaultProfile</span></span>
<span data-ttu-id="d9a01-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9a01-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9a01-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d9a01-115">-Force</span></span>
<span data-ttu-id="d9a01-116">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d9a01-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d9a01-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-117">-RouteFilter</span></span>
<span data-ttu-id="d9a01-118">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a01-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9a01-119">-Confirm</span></span>
<span data-ttu-id="d9a01-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9a01-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a01-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a01-121">-WhatIf</span></span>
<span data-ttu-id="d9a01-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a01-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9a01-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9a01-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a01-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a01-124">CommonParameters</span></span>
<span data-ttu-id="d9a01-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a01-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a01-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a01-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a01-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9a01-127">INPUTS</span></span>

### <span data-ttu-id="d9a01-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d9a01-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9a01-129">OUTPUTS</span></span>

### <span data-ttu-id="d9a01-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d9a01-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9a01-131">NOTES</span></span>

## <span data-ttu-id="d9a01-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9a01-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9a01-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="d9a01-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="d9a01-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d9a01-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="d9a01-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d9a01-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d9a01-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d9a01-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d9a01-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d9a01-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d9a01-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d9a01-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d9a01-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d9a01-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
