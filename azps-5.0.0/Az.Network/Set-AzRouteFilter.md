---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303118"
---
# <span data-ttu-id="9ea5d-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="9ea5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ea5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea5d-103">Aktualisiert einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-103">Updates a route filter.</span></span>

## <span data-ttu-id="9ea5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ea5d-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea5d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ea5d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea5d-106">Das Cmdlet " **Satz-AzApplicationGateway** " aktualisiert einen Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="9ea5d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ea5d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea5d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ea5d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="9ea5d-109">Dieser Befehl aktualisiert den Routenfilter mit den Einstellungen in der $RF Variablen.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="9ea5d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea5d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ea5d-111">-AsJob</span></span>
<span data-ttu-id="9ea5d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9ea5d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ea5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea5d-113">-DefaultProfile</span></span>
<span data-ttu-id="9ea5d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ea5d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9ea5d-115">-Force</span></span>
<span data-ttu-id="9ea5d-116">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="9ea5d-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9ea5d-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-117">-RouteFilter</span></span>
<span data-ttu-id="9ea5d-118">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-118">The RouteFilter</span></span>

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

### <span data-ttu-id="9ea5d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ea5d-119">-Confirm</span></span>
<span data-ttu-id="9ea5d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea5d-121">-WhatIf</span></span>
<span data-ttu-id="9ea5d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ea5d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea5d-124">CommonParameters</span></span>
<span data-ttu-id="9ea5d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea5d-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea5d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea5d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ea5d-127">INPUTS</span></span>

### <span data-ttu-id="9ea5d-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9ea5d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ea5d-129">OUTPUTS</span></span>

### <span data-ttu-id="9ea5d-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9ea5d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ea5d-131">NOTES</span></span>

## <span data-ttu-id="9ea5d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ea5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ea5d-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9ea5d-134">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="9ea5d-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ea5d-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="9ea5d-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ea5d-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9ea5d-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ea5d-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9ea5d-138">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ea5d-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9ea5d-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ea5d-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9ea5d-140">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9ea5d-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
