---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 0725b75c15fa6ab977d0b829a1928943bfd9ed31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503037"
---
# <span data-ttu-id="772e6-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="772e6-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="772e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="772e6-102">SYNOPSIS</span></span>
<span data-ttu-id="772e6-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="772e6-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="772e6-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="772e6-105">DESCRIPTION</span></span>
<span data-ttu-id="772e6-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="772e6-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="772e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="772e6-107">EXAMPLES</span></span>

### <span data-ttu-id="772e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="772e6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="772e6-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="772e6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="772e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="772e6-110">PARAMETERS</span></span>

### <span data-ttu-id="772e6-111">-Access</span><span class="sxs-lookup"><span data-stu-id="772e6-111">-Access</span></span>
<span data-ttu-id="772e6-112">Der Zugriffstyp der Regel.</span><span class="sxs-lookup"><span data-stu-id="772e6-112">The access type of the rule.</span></span>
<span data-ttu-id="772e6-113">Mögliche Werte sind: "zulassen", "verweigern"</span><span class="sxs-lookup"><span data-stu-id="772e6-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="772e6-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="772e6-114">-CommunityList</span></span>
<span data-ttu-id="772e6-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="772e6-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="772e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772e6-116">-DefaultProfile</span></span>
<span data-ttu-id="772e6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="772e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="772e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="772e6-118">-Force</span></span>
<span data-ttu-id="772e6-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="772e6-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="772e6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="772e6-120">-Name</span></span>
<span data-ttu-id="772e6-121">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="772e6-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="772e6-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="772e6-122">-RouteFilter</span></span>
<span data-ttu-id="772e6-123">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="772e6-123">The RouteFilter</span></span>

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

### <span data-ttu-id="772e6-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="772e6-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="772e6-125">Der Typ der Regel für den Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="772e6-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="772e6-126">Mögliche Werte sind: "Community"</span><span class="sxs-lookup"><span data-stu-id="772e6-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="772e6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="772e6-127">-Confirm</span></span>
<span data-ttu-id="772e6-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="772e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772e6-129">-WhatIf</span></span>
<span data-ttu-id="772e6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="772e6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="772e6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="772e6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772e6-132">CommonParameters</span></span>
<span data-ttu-id="772e6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772e6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772e6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772e6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="772e6-135">INPUTS</span></span>

### <span data-ttu-id="772e6-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="772e6-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="772e6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="772e6-137">OUTPUTS</span></span>

### <span data-ttu-id="772e6-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="772e6-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="772e6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="772e6-139">NOTES</span></span>

## <span data-ttu-id="772e6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="772e6-140">RELATED LINKS</span></span>

