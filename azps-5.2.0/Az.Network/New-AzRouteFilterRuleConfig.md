---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367518"
---
# <span data-ttu-id="fe18a-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe18a-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="fe18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe18a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe18a-103">Erstellt eine Routenfilterregel für einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="fe18a-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="fe18a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe18a-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe18a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe18a-105">DESCRIPTION</span></span>
<span data-ttu-id="fe18a-106">Das New-AzRouteFilterRuleConfig erstellt eine Routenfilterregel für einen Azure-Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="fe18a-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="fe18a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe18a-107">EXAMPLES</span></span>

### <span data-ttu-id="fe18a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe18a-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="fe18a-109">Der Befehl erstellt eine neue Routenfilterregel und speichert sie in variablen $rule 1.</span><span class="sxs-lookup"><span data-stu-id="fe18a-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="fe18a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe18a-110">PARAMETERS</span></span>

### <span data-ttu-id="fe18a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="fe18a-111">-Access</span></span>
<span data-ttu-id="fe18a-112">Access für die Routenfilterregel.</span><span class="sxs-lookup"><span data-stu-id="fe18a-112">Access for route filter rule.</span></span>
<span data-ttu-id="fe18a-113">Gültige Werte sind "Zulassen" oder "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="fe18a-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe18a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="fe18a-114">-CommunityList</span></span>
<span data-ttu-id="fe18a-115">Die Liste des Communitywerts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="fe18a-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe18a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe18a-116">-DefaultProfile</span></span>
<span data-ttu-id="fe18a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe18a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe18a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fe18a-118">-Force</span></span>
<span data-ttu-id="fe18a-119">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="fe18a-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fe18a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fe18a-120">-Name</span></span>
<span data-ttu-id="fe18a-121">Gibt einen Namen für die Routenfilterregel an.</span><span class="sxs-lookup"><span data-stu-id="fe18a-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="fe18a-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="fe18a-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="fe18a-123">Route Filter Rule Type.</span><span class="sxs-lookup"><span data-stu-id="fe18a-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="fe18a-124">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="fe18a-124">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe18a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe18a-125">-Confirm</span></span>
<span data-ttu-id="fe18a-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe18a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe18a-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe18a-127">-WhatIf</span></span>
<span data-ttu-id="fe18a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe18a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe18a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe18a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe18a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe18a-130">CommonParameters</span></span>
<span data-ttu-id="fe18a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe18a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe18a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe18a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe18a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe18a-133">INPUTS</span></span>

### <span data-ttu-id="fe18a-134">Keine</span><span class="sxs-lookup"><span data-stu-id="fe18a-134">None</span></span>

## <span data-ttu-id="fe18a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe18a-135">OUTPUTS</span></span>

### <span data-ttu-id="fe18a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="fe18a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="fe18a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe18a-137">NOTES</span></span>
<span data-ttu-id="fe18a-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="fe18a-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe18a-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe18a-139">RELATED LINKS</span></span>

[<span data-ttu-id="fe18a-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe18a-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe18a-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe18a-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe18a-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe18a-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe18a-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe18a-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe18a-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe18a-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="fe18a-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe18a-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="fe18a-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe18a-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="fe18a-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe18a-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
