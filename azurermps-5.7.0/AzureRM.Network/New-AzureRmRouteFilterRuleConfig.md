---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 6e0ff70671ceff4094d7f1a48bbebcc81398d5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478425"
---
# <span data-ttu-id="721af-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="721af-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="721af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="721af-102">SYNOPSIS</span></span>
<span data-ttu-id="721af-103">Erstellt eine Routenfilter Regel für einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="721af-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="721af-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="721af-105">DESCRIPTION</span></span>
<span data-ttu-id="721af-106">Das New-AzureRmRouteFilterRuleConfig-Cmdlet erstellt eine Routenfilter Regel für einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="721af-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="721af-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="721af-107">EXAMPLES</span></span>

### <span data-ttu-id="721af-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="721af-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="721af-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="721af-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="721af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="721af-110">PARAMETERS</span></span>

### <span data-ttu-id="721af-111">-Access</span><span class="sxs-lookup"><span data-stu-id="721af-111">-Access</span></span>
<span data-ttu-id="721af-112">Access für die Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="721af-112">Access for route filter rule.</span></span>
<span data-ttu-id="721af-113">Gültige Werte sind allow oder Deny.</span><span class="sxs-lookup"><span data-stu-id="721af-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="721af-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="721af-114">-CommunityList</span></span>
<span data-ttu-id="721af-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="721af-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="721af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721af-116">-DefaultProfile</span></span>
<span data-ttu-id="721af-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="721af-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="721af-118">-Force</span></span>
<span data-ttu-id="721af-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="721af-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="721af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="721af-120">-Name</span></span>
<span data-ttu-id="721af-121">Gibt einen Namen für die Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="721af-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="721af-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="721af-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="721af-123">Routen Filter-Regeltyp</span><span class="sxs-lookup"><span data-stu-id="721af-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="721af-124">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="721af-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="721af-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="721af-125">-Confirm</span></span>
<span data-ttu-id="721af-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="721af-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721af-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721af-127">-WhatIf</span></span>
<span data-ttu-id="721af-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="721af-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="721af-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="721af-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721af-130">CommonParameters</span></span>
<span data-ttu-id="721af-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721af-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721af-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721af-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="721af-133">INPUTS</span></span>

### <span data-ttu-id="721af-134">Keine</span><span class="sxs-lookup"><span data-stu-id="721af-134">None</span></span>
<span data-ttu-id="721af-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="721af-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="721af-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="721af-136">OUTPUTS</span></span>

### <span data-ttu-id="721af-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="721af-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="721af-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="721af-138">NOTES</span></span>
<span data-ttu-id="721af-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="721af-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="721af-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="721af-140">RELATED LINKS</span></span>

[<span data-ttu-id="721af-141">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="721af-141">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="721af-142">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="721af-142">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="721af-143">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="721af-143">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="721af-144">Satz-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="721af-144">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

