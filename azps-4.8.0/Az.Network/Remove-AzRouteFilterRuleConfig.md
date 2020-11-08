---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166236"
---
# <span data-ttu-id="dd637-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd637-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="dd637-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd637-102">SYNOPSIS</span></span>
<span data-ttu-id="dd637-103">Entfernt eine Routenfilter Regel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="dd637-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="dd637-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd637-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd637-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd637-105">DESCRIPTION</span></span>
<span data-ttu-id="dd637-106">Das Cmdlet " **Remove-AzRouteFilterRuleConfig** " entfernt eine Routenfilter Regel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="dd637-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="dd637-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd637-107">EXAMPLES</span></span>

### <span data-ttu-id="dd637-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd637-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="dd637-109">Der erste Befehl ruft einen Routenfilter mit dem Namen RouteFilter01 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert ihn in der $RF Variablen.</span><span class="sxs-lookup"><span data-stu-id="dd637-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="dd637-110">Der zweite Befehl entfernt die Routenfilter Regel namens Rule01 aus dem in $RF gespeicherten Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="dd637-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="dd637-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd637-111">PARAMETERS</span></span>

### <span data-ttu-id="dd637-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd637-112">-DefaultProfile</span></span>
<span data-ttu-id="dd637-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd637-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd637-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dd637-114">-Force</span></span>
<span data-ttu-id="dd637-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="dd637-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dd637-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dd637-116">-Name</span></span>
<span data-ttu-id="dd637-117">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="dd637-117">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd637-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-118">-RouteFilter</span></span>
<span data-ttu-id="dd637-119">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-119">The RouteFilter</span></span>

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

### <span data-ttu-id="dd637-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd637-120">-Confirm</span></span>
<span data-ttu-id="dd637-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd637-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd637-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd637-122">-WhatIf</span></span>
<span data-ttu-id="dd637-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd637-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd637-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd637-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd637-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd637-125">CommonParameters</span></span>
<span data-ttu-id="dd637-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd637-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd637-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd637-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd637-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd637-128">INPUTS</span></span>

### <span data-ttu-id="dd637-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="dd637-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd637-130">OUTPUTS</span></span>

### <span data-ttu-id="dd637-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="dd637-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="dd637-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd637-132">NOTES</span></span>

## <span data-ttu-id="dd637-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd637-133">RELATED LINKS</span></span>

[<span data-ttu-id="dd637-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd637-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dd637-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd637-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dd637-136">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd637-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dd637-137">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd637-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dd637-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="dd637-139">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="dd637-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="dd637-141">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd637-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
