---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 0cf13aa5aa1fb558e72a4896bc810859409b5ae1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848400"
---
# <span data-ttu-id="1ebcd-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ebcd-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1ebcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ebcd-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebcd-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="1ebcd-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ebcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ebcd-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ebcd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ebcd-105">DESCRIPTION</span></span>
<span data-ttu-id="1ebcd-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="1ebcd-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1ebcd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ebcd-107">EXAMPLES</span></span>

### <span data-ttu-id="1ebcd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ebcd-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1ebcd-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="1ebcd-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1ebcd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ebcd-110">PARAMETERS</span></span>

### <span data-ttu-id="1ebcd-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1ebcd-111">-Access</span></span>
<span data-ttu-id="1ebcd-112">Der Zugriffstyp der Regel.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-112">The access type of the rule.</span></span>
<span data-ttu-id="1ebcd-113">Mögliche Werte sind: "zulassen", "verweigern"</span><span class="sxs-lookup"><span data-stu-id="1ebcd-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="1ebcd-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="1ebcd-114">-CommunityList</span></span>
<span data-ttu-id="1ebcd-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="1ebcd-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1ebcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebcd-116">-DefaultProfile</span></span>
<span data-ttu-id="1ebcd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ebcd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1ebcd-118">-Force</span></span>
<span data-ttu-id="1ebcd-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="1ebcd-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1ebcd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1ebcd-120">-Name</span></span>
<span data-ttu-id="1ebcd-121">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="1ebcd-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="1ebcd-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ebcd-122">-RouteFilter</span></span>
<span data-ttu-id="1ebcd-123">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ebcd-123">The RouteFilter</span></span>

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

### <span data-ttu-id="1ebcd-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1ebcd-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="1ebcd-125">Der Typ der Regel für den Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="1ebcd-126">Mögliche Werte sind: "Community"</span><span class="sxs-lookup"><span data-stu-id="1ebcd-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="1ebcd-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ebcd-127">-Confirm</span></span>
<span data-ttu-id="1ebcd-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ebcd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ebcd-129">-WhatIf</span></span>
<span data-ttu-id="1ebcd-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ebcd-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ebcd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebcd-132">CommonParameters</span></span>
<span data-ttu-id="1ebcd-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebcd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebcd-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ebcd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebcd-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ebcd-135">INPUTS</span></span>

### <span data-ttu-id="1ebcd-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ebcd-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1ebcd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ebcd-137">OUTPUTS</span></span>

### <span data-ttu-id="1ebcd-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1ebcd-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1ebcd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ebcd-139">NOTES</span></span>

## <span data-ttu-id="1ebcd-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ebcd-140">RELATED LINKS</span></span>

