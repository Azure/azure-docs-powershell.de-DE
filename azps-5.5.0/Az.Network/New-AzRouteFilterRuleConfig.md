---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156873"
---
# <span data-ttu-id="75b65-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75b65-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="75b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b65-102">SYNOPSIS</span></span>
<span data-ttu-id="75b65-103">Erstellt eine Routenfilterregel für einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="75b65-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="75b65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75b65-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b65-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75b65-105">DESCRIPTION</span></span>
<span data-ttu-id="75b65-106">Das New-AzRouteFilterRuleConfig erstellt eine Routenfilterregel für einen Azure-Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="75b65-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="75b65-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75b65-107">EXAMPLES</span></span>

### <span data-ttu-id="75b65-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75b65-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="75b65-109">Der Befehl erstellt eine neue Routenfilterregel und speichert sie in variablen $rule 1.</span><span class="sxs-lookup"><span data-stu-id="75b65-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="75b65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75b65-110">PARAMETERS</span></span>

### <span data-ttu-id="75b65-111">-Access</span><span class="sxs-lookup"><span data-stu-id="75b65-111">-Access</span></span>
<span data-ttu-id="75b65-112">Access für die Routenfilterregel.</span><span class="sxs-lookup"><span data-stu-id="75b65-112">Access for route filter rule.</span></span>
<span data-ttu-id="75b65-113">Gültige Werte sind "Zulassen" oder "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="75b65-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="75b65-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="75b65-114">-CommunityList</span></span>
<span data-ttu-id="75b65-115">Die Liste des Communitywerts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="75b65-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="75b65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b65-116">-DefaultProfile</span></span>
<span data-ttu-id="75b65-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75b65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75b65-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75b65-118">-Force</span></span>
<span data-ttu-id="75b65-119">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="75b65-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="75b65-120">-Name</span><span class="sxs-lookup"><span data-stu-id="75b65-120">-Name</span></span>
<span data-ttu-id="75b65-121">Gibt einen Namen für die Routenfilterregel an.</span><span class="sxs-lookup"><span data-stu-id="75b65-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="75b65-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="75b65-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="75b65-123">Regeltyp "Routenfilter".</span><span class="sxs-lookup"><span data-stu-id="75b65-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="75b65-124">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="75b65-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="75b65-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75b65-125">-Confirm</span></span>
<span data-ttu-id="75b65-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75b65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b65-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="75b65-127">-WhatIf</span></span>
<span data-ttu-id="75b65-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75b65-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75b65-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75b65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b65-130">CommonParameters</span></span>
<span data-ttu-id="75b65-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b65-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b65-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b65-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75b65-133">INPUTS</span></span>

### <span data-ttu-id="75b65-134">Keine</span><span class="sxs-lookup"><span data-stu-id="75b65-134">None</span></span>

## <span data-ttu-id="75b65-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75b65-135">OUTPUTS</span></span>

### <span data-ttu-id="75b65-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="75b65-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="75b65-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75b65-137">NOTES</span></span>
<span data-ttu-id="75b65-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="75b65-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="75b65-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75b65-139">RELATED LINKS</span></span>

[<span data-ttu-id="75b65-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75b65-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75b65-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75b65-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75b65-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75b65-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75b65-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75b65-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="75b65-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75b65-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="75b65-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75b65-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="75b65-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75b65-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="75b65-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="75b65-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
