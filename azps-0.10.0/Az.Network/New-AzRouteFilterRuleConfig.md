---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841279"
---
# <span data-ttu-id="4ffc0-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffc0-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4ffc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ffc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffc0-103">Erstellt eine Routenfilter Regel für einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="4ffc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ffc0-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ffc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ffc0-105">DESCRIPTION</span></span>
<span data-ttu-id="4ffc0-106">Das New-AzRouteFilterRuleConfig-Cmdlet erstellt eine Routenfilter Regel für einen Azure Route-Filter.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="4ffc0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ffc0-107">EXAMPLES</span></span>

### <span data-ttu-id="4ffc0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ffc0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4ffc0-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="4ffc0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4ffc0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ffc0-110">PARAMETERS</span></span>

### <span data-ttu-id="4ffc0-111">-Access</span><span class="sxs-lookup"><span data-stu-id="4ffc0-111">-Access</span></span>
<span data-ttu-id="4ffc0-112">Access für die Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="4ffc0-112">Access for route filter rule.</span></span>
<span data-ttu-id="4ffc0-113">Gültige Werte sind allow oder Deny.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="4ffc0-114">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="4ffc0-114">-CommunityList</span></span>
<span data-ttu-id="4ffc0-115">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="4ffc0-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="4ffc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffc0-116">-DefaultProfile</span></span>
<span data-ttu-id="4ffc0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ffc0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4ffc0-118">-Force</span></span>
<span data-ttu-id="4ffc0-119">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="4ffc0-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4ffc0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4ffc0-120">-Name</span></span>
<span data-ttu-id="4ffc0-121">Gibt einen Namen für die Routenfilter Regel an.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="4ffc0-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4ffc0-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="4ffc0-123">Routen Filter-Regeltyp</span><span class="sxs-lookup"><span data-stu-id="4ffc0-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="4ffc0-124">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="4ffc0-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="4ffc0-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ffc0-125">-Confirm</span></span>
<span data-ttu-id="4ffc0-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ffc0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffc0-127">-WhatIf</span></span>
<span data-ttu-id="4ffc0-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ffc0-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ffc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffc0-130">CommonParameters</span></span>
<span data-ttu-id="4ffc0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffc0-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffc0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffc0-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ffc0-133">INPUTS</span></span>

## <span data-ttu-id="4ffc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ffc0-134">OUTPUTS</span></span>

### <span data-ttu-id="4ffc0-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="4ffc0-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="4ffc0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ffc0-136">NOTES</span></span>
<span data-ttu-id="4ffc0-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="4ffc0-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4ffc0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ffc0-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ffc0-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffc0-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ffc0-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffc0-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ffc0-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffc0-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ffc0-142">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffc0-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

