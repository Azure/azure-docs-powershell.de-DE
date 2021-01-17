---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473369"
---
# <span data-ttu-id="ef438-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="ef438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef438-102">SYNOPSIS</span></span>
<span data-ttu-id="ef438-103">Aktualisiert einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="ef438-103">Updates a route filter.</span></span>

## <span data-ttu-id="ef438-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef438-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef438-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef438-105">DESCRIPTION</span></span>
<span data-ttu-id="ef438-106">Das **Cmdlet Set-AzApplicationGateway** aktualisiert einen Routenfilter</span><span class="sxs-lookup"><span data-stu-id="ef438-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="ef438-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef438-107">EXAMPLES</span></span>

### <span data-ttu-id="ef438-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef438-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="ef438-109">Mit diesem Befehl wird der Routenfilter mit den Einstellungen in der Variablen $rf aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ef438-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="ef438-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef438-110">PARAMETERS</span></span>

### <span data-ttu-id="ef438-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef438-111">-AsJob</span></span>
<span data-ttu-id="ef438-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ef438-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef438-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef438-113">-DefaultProfile</span></span>
<span data-ttu-id="ef438-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef438-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef438-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef438-115">-Force</span></span>
<span data-ttu-id="ef438-116">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="ef438-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ef438-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-117">-RouteFilter</span></span>
<span data-ttu-id="ef438-118">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ef438-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef438-119">-Confirm</span></span>
<span data-ttu-id="ef438-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef438-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef438-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef438-121">-WhatIf</span></span>
<span data-ttu-id="ef438-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef438-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef438-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef438-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef438-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef438-124">CommonParameters</span></span>
<span data-ttu-id="ef438-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef438-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef438-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef438-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef438-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef438-127">INPUTS</span></span>

### <span data-ttu-id="ef438-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ef438-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef438-129">OUTPUTS</span></span>

### <span data-ttu-id="ef438-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ef438-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef438-131">NOTES</span></span>

## <span data-ttu-id="ef438-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef438-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef438-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ef438-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ef438-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ef438-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ef438-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef438-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef438-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef438-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef438-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef438-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef438-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef438-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ef438-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ef438-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
