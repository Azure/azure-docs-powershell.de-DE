---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850787"
---
# <span data-ttu-id="dd42b-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd42b-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="dd42b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd42b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd42b-103">Fügt eine Routenfilter Regel zu einem Routenfilter hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd42b-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd42b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd42b-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd42b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd42b-105">DESCRIPTION</span></span>
<span data-ttu-id="dd42b-106">Mit dem Add-AzureRmRouteFilterRuleConfig-Cmdlet wird eine Routenfilter Regel zu einem Azure Route-Filter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd42b-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="dd42b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd42b-107">EXAMPLES</span></span>

### <span data-ttu-id="dd42b-108">--------------------------Beispiel 1: Hinzufügen einer Routenfilter Regel zu einem Routenfilter--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd42b-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="dd42b-109">Der erste Befehl ruft einen Routenfilter mit dem Namen routefilter01 mithilfe des Get-AzureRmRouteFilter-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="dd42b-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="dd42b-110">Der Befehl speichert den Filter in der $RouteFilter-Variablen.</span><span class="sxs-lookup"><span data-stu-id="dd42b-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="dd42b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd42b-111">PARAMETERS</span></span>

### <span data-ttu-id="dd42b-112">-Access</span><span class="sxs-lookup"><span data-stu-id="dd42b-112">-Access</span></span>
<span data-ttu-id="dd42b-113">Gibt den Zugriff auf die Routenfilter Regel an, gültige Werte sind "verweigern" oder "zulassen".</span><span class="sxs-lookup"><span data-stu-id="dd42b-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="dd42b-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="dd42b-114">-CommunityList</span></span>
<span data-ttu-id="dd42b-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="dd42b-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="dd42b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd42b-116">-DefaultProfile</span></span>
<span data-ttu-id="dd42b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd42b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd42b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd42b-118">-Force</span></span>
<span data-ttu-id="dd42b-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="dd42b-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="dd42b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dd42b-120">-Name</span></span>
<span data-ttu-id="dd42b-121">Gibt einen Namen der Routenfilter Regel an, die dem Routenfilter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd42b-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="dd42b-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd42b-122">-RouteFilter</span></span>
<span data-ttu-id="dd42b-123">Gibt den Routenfilter an, dem dieses Cmdlet eine Routenfilter Regel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="dd42b-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="dd42b-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="dd42b-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="dd42b-125">Gibt den Typ der Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="dd42b-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="dd42b-126">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="dd42b-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="dd42b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd42b-127">-Confirm</span></span>
<span data-ttu-id="dd42b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd42b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd42b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd42b-129">-WhatIf</span></span>
<span data-ttu-id="dd42b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd42b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd42b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd42b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd42b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd42b-132">CommonParameters</span></span>
<span data-ttu-id="dd42b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd42b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd42b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd42b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd42b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd42b-135">INPUTS</span></span>

### <span data-ttu-id="dd42b-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd42b-136">PSRouteFilter</span></span>
<span data-ttu-id="dd42b-137">Der Parameter "RouteFilter" akzeptiert den Wert vom Typ "PSRouteFilter" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd42b-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="dd42b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd42b-138">OUTPUTS</span></span>

### <span data-ttu-id="dd42b-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd42b-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="dd42b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd42b-140">NOTES</span></span>
<span data-ttu-id="dd42b-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="dd42b-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dd42b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd42b-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd42b-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd42b-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="dd42b-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd42b-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="dd42b-145">Satz-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="dd42b-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

