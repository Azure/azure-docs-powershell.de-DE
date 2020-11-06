---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501754"
---
# <span data-ttu-id="951db-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="951db-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="951db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="951db-102">SYNOPSIS</span></span>
<span data-ttu-id="951db-103">Fügt eine Routenfilter Regel zu einem Routenfilter hinzu.</span><span class="sxs-lookup"><span data-stu-id="951db-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="951db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="951db-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="951db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="951db-105">DESCRIPTION</span></span>
<span data-ttu-id="951db-106">Mit dem Add-AzureRmRouteFilterRuleConfig-Cmdlet wird eine Routenfilter Regel zu einem Azure Route-Filter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="951db-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="951db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="951db-107">EXAMPLES</span></span>

### <span data-ttu-id="951db-108">--------------------------Beispiel 1: Hinzufügen einer Routenfilter Regel zu einem Routenfilter--------------------------</span><span class="sxs-lookup"><span data-stu-id="951db-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="951db-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="951db-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="951db-110">Der erste Befehl ruft einen Routenfilter mit dem Namen routefilter01 mithilfe des Get-AzureRmRouteFilter-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="951db-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="951db-111">Der Befehl speichert den Filter in der $RouteFilter-Variablen.</span><span class="sxs-lookup"><span data-stu-id="951db-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="951db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="951db-112">PARAMETERS</span></span>

### <span data-ttu-id="951db-113">-Access</span><span class="sxs-lookup"><span data-stu-id="951db-113">-Access</span></span>
<span data-ttu-id="951db-114">Gibt den Zugriff auf die Routenfilter Regel an, gültige Werte sind "verweigern" oder "zulassen".</span><span class="sxs-lookup"><span data-stu-id="951db-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="951db-115">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="951db-115">-CommunityList</span></span>
<span data-ttu-id="951db-116">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="951db-116">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951db-117">-Force</span><span class="sxs-lookup"><span data-stu-id="951db-117">-Force</span></span>
<span data-ttu-id="951db-118">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="951db-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="951db-119">-Name</span><span class="sxs-lookup"><span data-stu-id="951db-119">-Name</span></span>
<span data-ttu-id="951db-120">Gibt einen Namen der Routenfilter Regel an, die dem Routenfilter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="951db-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="951db-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="951db-121">-RouteFilter</span></span>
<span data-ttu-id="951db-122">Gibt den Routenfilter an, dem dieses Cmdlet eine Routenfilter Regel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="951db-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="951db-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="951db-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="951db-124">Gibt den Typ der Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="951db-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="951db-125">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="951db-125">Valid values are: Community</span></span>

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

### <span data-ttu-id="951db-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="951db-126">-Confirm</span></span>
<span data-ttu-id="951db-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="951db-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951db-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951db-128">-WhatIf</span></span>
<span data-ttu-id="951db-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="951db-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="951db-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="951db-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951db-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951db-131">-DefaultProfile</span></span>
<span data-ttu-id="951db-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="951db-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951db-133">CommonParameters</span></span>
<span data-ttu-id="951db-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951db-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951db-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951db-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="951db-136">INPUTS</span></span>

### <span data-ttu-id="951db-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="951db-137">PSRouteFilter</span></span>
<span data-ttu-id="951db-138">Der Parameter "RouteFilter" akzeptiert den Wert vom Typ "PSRouteFilter" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="951db-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="951db-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="951db-139">OUTPUTS</span></span>

### <span data-ttu-id="951db-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="951db-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="951db-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="951db-141">NOTES</span></span>
<span data-ttu-id="951db-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="951db-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="951db-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="951db-143">RELATED LINKS</span></span>

[<span data-ttu-id="951db-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="951db-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="951db-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="951db-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="951db-146">Neu – AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="951db-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="951db-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="951db-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="951db-148">Satz-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="951db-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="951db-149">Satz-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="951db-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

