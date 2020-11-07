---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841795"
---
# <span data-ttu-id="8a8a9-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a8a9-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8a8a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8a9-103">Fügt eine Routenfilter Regel zu einem Routenfilter hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="8a8a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a8a9-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a8a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a8a9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8a9-106">Mit dem Add-AzRouteFilterRuleConfig-Cmdlet wird eine Routenfilter Regel zu einem Azure Route-Filter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="8a8a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a8a9-107">EXAMPLES</span></span>

### <span data-ttu-id="8a8a9-108">--------------------------Beispiel 1: Hinzufügen einer Routenfilter Regel zu einem Routenfilter--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a8a9-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="8a8a9-109">Der erste Befehl ruft einen Routenfilter mit dem Namen routefilter01 mithilfe des Get-AzRouteFilter-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="8a8a9-110">Der Befehl speichert den Filter in der $RouteFilter-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="8a8a9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-111">PARAMETERS</span></span>

### <span data-ttu-id="8a8a9-112">-Access</span><span class="sxs-lookup"><span data-stu-id="8a8a9-112">-Access</span></span>
<span data-ttu-id="8a8a9-113">Gibt den Zugriff auf die Routenfilter Regel an, gültige Werte sind "verweigern" oder "zulassen".</span><span class="sxs-lookup"><span data-stu-id="8a8a9-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="8a8a9-114">-CommunityList</span></span>
<span data-ttu-id="8a8a9-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="8a8a9-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8a8a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8a9-116">-DefaultProfile</span></span>
<span data-ttu-id="8a8a9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8a8a9-118">-Force</span></span>
<span data-ttu-id="8a8a9-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="8a8a9-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8a8a9-120">-Name</span></span>
<span data-ttu-id="8a8a9-121">Gibt einen Namen der Routenfilter Regel an, die dem Routenfilter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-122">-RouteFilter</span></span>
<span data-ttu-id="8a8a9-123">Gibt den Routenfilter an, dem dieses Cmdlet eine Routenfilter Regel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8a8a9-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="8a8a9-125">Gibt den Typ der Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="8a8a9-126">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="8a8a9-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a8a9-127">-Confirm</span></span>
<span data-ttu-id="8a8a9-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8a9-129">-WhatIf</span></span>
<span data-ttu-id="8a8a9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a8a9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8a9-132">CommonParameters</span></span>
<span data-ttu-id="8a8a9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8a9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8a9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8a9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a8a9-135">INPUTS</span></span>

### <span data-ttu-id="8a8a9-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-136">PSRouteFilter</span></span>
<span data-ttu-id="8a8a9-137">Der Parameter "RouteFilter" akzeptiert den Wert vom Typ "PSRouteFilter" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a8a9-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="8a8a9-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a8a9-138">OUTPUTS</span></span>

### <span data-ttu-id="8a8a9-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8a8a9-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a8a9-140">NOTES</span></span>
<span data-ttu-id="8a8a9-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="8a8a9-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8a8a9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a8a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a8a9-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8a8a9-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8a8a9-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8a8a9-145">Neu – AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8a8a9-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8a8a9-146">Remove-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8a8a9-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8a8a9-147">Satz-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="8a8a9-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="8a8a9-148">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8a8a9-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

