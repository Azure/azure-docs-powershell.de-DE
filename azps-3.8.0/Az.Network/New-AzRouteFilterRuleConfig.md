---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003454"
---
# <span data-ttu-id="fe0e8-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe0e8-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="fe0e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0e8-103">Erstellt eine Routenfilter Regel für einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="fe0e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe0e8-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="fe0e8-106">Das New-AzRouteFilterRuleConfig-Cmdlet erstellt eine Routenfilter Regel für einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="fe0e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe0e8-107">EXAMPLES</span></span>

### <span data-ttu-id="fe0e8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe0e8-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="fe0e8-109">Der Befehl erstellt eine neue Routenfilter Regel und speichert Sie in der Variablen $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="fe0e8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe0e8-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0e8-111">-Access</span><span class="sxs-lookup"><span data-stu-id="fe0e8-111">-Access</span></span>
<span data-ttu-id="fe0e8-112">Access für die Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="fe0e8-112">Access for route filter rule.</span></span>
<span data-ttu-id="fe0e8-113">Gültige Werte sind allow oder Deny.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="fe0e8-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="fe0e8-114">-CommunityList</span></span>
<span data-ttu-id="fe0e8-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="fe0e8-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="fe0e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0e8-116">-DefaultProfile</span></span>
<span data-ttu-id="fe0e8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0e8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fe0e8-118">-Force</span></span>
<span data-ttu-id="fe0e8-119">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="fe0e8-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fe0e8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fe0e8-120">-Name</span></span>
<span data-ttu-id="fe0e8-121">Gibt einen Namen für die Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="fe0e8-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="fe0e8-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="fe0e8-123">Routen Filter-Regeltyp</span><span class="sxs-lookup"><span data-stu-id="fe0e8-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="fe0e8-124">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="fe0e8-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="fe0e8-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe0e8-125">-Confirm</span></span>
<span data-ttu-id="fe0e8-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0e8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0e8-127">-WhatIf</span></span>
<span data-ttu-id="fe0e8-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe0e8-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0e8-130">CommonParameters</span></span>
<span data-ttu-id="fe0e8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0e8-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0e8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0e8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe0e8-133">INPUTS</span></span>

### <span data-ttu-id="fe0e8-134">Keine</span><span class="sxs-lookup"><span data-stu-id="fe0e8-134">None</span></span>

## <span data-ttu-id="fe0e8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe0e8-135">OUTPUTS</span></span>

### <span data-ttu-id="fe0e8-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="fe0e8-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="fe0e8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe0e8-137">NOTES</span></span>
<span data-ttu-id="fe0e8-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="fe0e8-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe0e8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe0e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="fe0e8-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe0e8-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe0e8-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe0e8-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe0e8-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe0e8-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe0e8-143">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe0e8-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fe0e8-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0e8-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="fe0e8-145">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0e8-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="fe0e8-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0e8-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="fe0e8-147">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe0e8-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
