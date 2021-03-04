---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930923"
---
# <span data-ttu-id="120c4-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="120c4-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="120c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120c4-102">SYNOPSIS</span></span>
<span data-ttu-id="120c4-103">Entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="120c4-103">Removes a route filter.</span></span>

## <span data-ttu-id="120c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="120c4-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="120c4-105">DESCRIPTION</span></span>
<span data-ttu-id="120c4-106">Das **Cmdlet Remove-AzRouteFilter** entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="120c4-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="120c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="120c4-107">EXAMPLES</span></span>

### <span data-ttu-id="120c4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="120c4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="120c4-109">Der Befehl entfernt den Routenfilter mit dem Namen RouteFilter01 in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="120c4-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="120c4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="120c4-110">PARAMETERS</span></span>

### <span data-ttu-id="120c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120c4-111">-DefaultProfile</span></span>
<span data-ttu-id="120c4-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="120c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="120c4-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="120c4-113">-Force</span></span>
<span data-ttu-id="120c4-114">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="120c4-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="120c4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="120c4-115">-Name</span></span>
<span data-ttu-id="120c4-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="120c4-116">The resource name.</span></span>

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

### <span data-ttu-id="120c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="120c4-117">-PassThru</span></span>
<span data-ttu-id="120c4-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="120c4-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="120c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="120c4-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="120c4-120">The resource group name.</span></span>

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

### <span data-ttu-id="120c4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="120c4-121">-Confirm</span></span>
<span data-ttu-id="120c4-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="120c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120c4-123">-WhatIf</span></span>
<span data-ttu-id="120c4-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="120c4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120c4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="120c4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120c4-126">CommonParameters</span></span>
<span data-ttu-id="120c4-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="120c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120c4-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120c4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120c4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="120c4-129">INPUTS</span></span>

### <span data-ttu-id="120c4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="120c4-130">System.String</span></span>

## <span data-ttu-id="120c4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="120c4-131">OUTPUTS</span></span>

### <span data-ttu-id="120c4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="120c4-132">System.Boolean</span></span>

## <span data-ttu-id="120c4-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="120c4-133">NOTES</span></span>

## <span data-ttu-id="120c4-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="120c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="120c4-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="120c4-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="120c4-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="120c4-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="120c4-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="120c4-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="120c4-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="120c4-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="120c4-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="120c4-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="120c4-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="120c4-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="120c4-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="120c4-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="120c4-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="120c4-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
