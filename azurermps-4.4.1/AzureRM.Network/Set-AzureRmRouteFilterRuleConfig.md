---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481798"
---
# <span data-ttu-id="0dd31-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0dd31-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0dd31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0dd31-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd31-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="0dd31-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dd31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dd31-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd31-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dd31-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd31-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="0dd31-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0dd31-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0dd31-107">EXAMPLES</span></span>

### <span data-ttu-id="0dd31-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dd31-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0dd31-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="0dd31-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0dd31-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd31-110">PARAMETERS</span></span>

### <span data-ttu-id="0dd31-111">-Access</span><span class="sxs-lookup"><span data-stu-id="0dd31-111">-Access</span></span>
<span data-ttu-id="0dd31-112">Der Zugriffstyp der Regel.</span><span class="sxs-lookup"><span data-stu-id="0dd31-112">The access type of the rule.</span></span>
<span data-ttu-id="0dd31-113">Mögliche Werte sind: "zulassen", "verweigern"</span><span class="sxs-lookup"><span data-stu-id="0dd31-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="0dd31-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="0dd31-114">-CommunityList</span></span>
<span data-ttu-id="0dd31-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="0dd31-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="0dd31-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd31-116">-Force</span></span>
<span data-ttu-id="0dd31-117">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="0dd31-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="0dd31-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0dd31-118">-Name</span></span>
<span data-ttu-id="0dd31-119">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="0dd31-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="0dd31-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dd31-120">-RouteFilter</span></span>
<span data-ttu-id="0dd31-121">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dd31-121">The RouteFilter</span></span>

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

### <span data-ttu-id="0dd31-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="0dd31-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="0dd31-123">Der Typ der Regel für den Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="0dd31-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="0dd31-124">Mögliche Werte sind: "Community"</span><span class="sxs-lookup"><span data-stu-id="0dd31-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="0dd31-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0dd31-125">-Confirm</span></span>
<span data-ttu-id="0dd31-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dd31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd31-127">-WhatIf</span></span>
<span data-ttu-id="0dd31-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dd31-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dd31-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dd31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd31-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd31-130">-DefaultProfile</span></span>
<span data-ttu-id="0dd31-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0dd31-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dd31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd31-132">CommonParameters</span></span>
<span data-ttu-id="0dd31-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd31-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd31-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0dd31-135">INPUTS</span></span>

### <span data-ttu-id="0dd31-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dd31-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0dd31-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0dd31-137">OUTPUTS</span></span>

### <span data-ttu-id="0dd31-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0dd31-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0dd31-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0dd31-139">NOTES</span></span>

## <span data-ttu-id="0dd31-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0dd31-140">RELATED LINKS</span></span>

