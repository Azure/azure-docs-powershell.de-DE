---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473444"
---
# <span data-ttu-id="b24bf-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b24bf-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="b24bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24bf-102">SYNOPSIS</span></span>
<span data-ttu-id="b24bf-103">Entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="b24bf-103">Removes a route filter.</span></span>

## <span data-ttu-id="b24bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b24bf-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b24bf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b24bf-105">DESCRIPTION</span></span>
<span data-ttu-id="b24bf-106">Das **Cmdlet "Remove-AzRouteFilter"** entfernt einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="b24bf-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="b24bf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b24bf-107">EXAMPLES</span></span>

### <span data-ttu-id="b24bf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b24bf-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b24bf-109">Der Befehl entfernt den Routenfilter namens "RouteFilter01" in der Ressourcengruppe mit dem Namen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b24bf-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b24bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24bf-110">PARAMETERS</span></span>

### <span data-ttu-id="b24bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24bf-111">-DefaultProfile</span></span>
<span data-ttu-id="b24bf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b24bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b24bf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b24bf-113">-Force</span></span>
<span data-ttu-id="b24bf-114">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="b24bf-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b24bf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b24bf-115">-Name</span></span>
<span data-ttu-id="b24bf-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b24bf-116">The resource name.</span></span>

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

### <span data-ttu-id="b24bf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b24bf-117">-PassThru</span></span>
<span data-ttu-id="b24bf-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b24bf-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b24bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="b24bf-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b24bf-120">The resource group name.</span></span>

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

### <span data-ttu-id="b24bf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b24bf-121">-Confirm</span></span>
<span data-ttu-id="b24bf-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b24bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b24bf-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b24bf-123">-WhatIf</span></span>
<span data-ttu-id="b24bf-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b24bf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b24bf-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b24bf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b24bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24bf-126">CommonParameters</span></span>
<span data-ttu-id="b24bf-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24bf-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24bf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24bf-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b24bf-129">INPUTS</span></span>

### <span data-ttu-id="b24bf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b24bf-130">System.String</span></span>

## <span data-ttu-id="b24bf-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b24bf-131">OUTPUTS</span></span>

### <span data-ttu-id="b24bf-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b24bf-132">System.Boolean</span></span>

## <span data-ttu-id="b24bf-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b24bf-133">NOTES</span></span>

## <span data-ttu-id="b24bf-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b24bf-134">RELATED LINKS</span></span>

[<span data-ttu-id="b24bf-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b24bf-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b24bf-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b24bf-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b24bf-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b24bf-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="b24bf-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b24bf-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b24bf-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b24bf-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b24bf-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b24bf-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b24bf-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b24bf-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b24bf-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b24bf-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
