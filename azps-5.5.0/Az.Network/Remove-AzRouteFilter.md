---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169691"
---
# <span data-ttu-id="1acda-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1acda-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="1acda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1acda-102">SYNOPSIS</span></span>
<span data-ttu-id="1acda-103">Entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="1acda-103">Removes a route filter.</span></span>

## <span data-ttu-id="1acda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1acda-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1acda-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1acda-105">DESCRIPTION</span></span>
<span data-ttu-id="1acda-106">Das **Cmdlet "Remove-AzRouteFilter"** entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="1acda-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="1acda-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1acda-107">EXAMPLES</span></span>

### <span data-ttu-id="1acda-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1acda-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1acda-109">Der Befehl entfernt den Routenfilter namens "RouteFilter01" in der Ressourcengruppe mit dem Namen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1acda-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1acda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1acda-110">PARAMETERS</span></span>

### <span data-ttu-id="1acda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1acda-111">-DefaultProfile</span></span>
<span data-ttu-id="1acda-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1acda-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1acda-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1acda-113">-Force</span></span>
<span data-ttu-id="1acda-114">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="1acda-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1acda-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1acda-115">-Name</span></span>
<span data-ttu-id="1acda-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1acda-116">The resource name.</span></span>

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

### <span data-ttu-id="1acda-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1acda-117">-PassThru</span></span>
<span data-ttu-id="1acda-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1acda-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="1acda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1acda-119">-ResourceGroupName</span></span>
<span data-ttu-id="1acda-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1acda-120">The resource group name.</span></span>

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

### <span data-ttu-id="1acda-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1acda-121">-Confirm</span></span>
<span data-ttu-id="1acda-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1acda-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1acda-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1acda-123">-WhatIf</span></span>
<span data-ttu-id="1acda-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1acda-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1acda-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1acda-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1acda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acda-126">CommonParameters</span></span>
<span data-ttu-id="1acda-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acda-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1acda-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acda-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1acda-129">INPUTS</span></span>

### <span data-ttu-id="1acda-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1acda-130">System.String</span></span>

## <span data-ttu-id="1acda-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1acda-131">OUTPUTS</span></span>

### <span data-ttu-id="1acda-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1acda-132">System.Boolean</span></span>

## <span data-ttu-id="1acda-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1acda-133">NOTES</span></span>

## <span data-ttu-id="1acda-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1acda-134">RELATED LINKS</span></span>

[<span data-ttu-id="1acda-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1acda-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1acda-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1acda-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1acda-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1acda-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="1acda-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1acda-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1acda-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1acda-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1acda-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1acda-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1acda-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1acda-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1acda-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1acda-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
