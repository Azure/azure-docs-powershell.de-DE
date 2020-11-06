---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503237"
---
# <span data-ttu-id="d05cf-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d05cf-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d05cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d05cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d05cf-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="d05cf-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d05cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d05cf-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d05cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d05cf-105">DESCRIPTION</span></span>
<span data-ttu-id="d05cf-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="d05cf-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d05cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d05cf-107">EXAMPLES</span></span>

### <span data-ttu-id="d05cf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d05cf-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d05cf-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="d05cf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d05cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d05cf-110">PARAMETERS</span></span>

### <span data-ttu-id="d05cf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d05cf-111">-Force</span></span>
<span data-ttu-id="d05cf-112">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="d05cf-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d05cf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d05cf-113">-Name</span></span>
<span data-ttu-id="d05cf-114">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="d05cf-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="d05cf-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d05cf-115">-RouteFilter</span></span>
<span data-ttu-id="d05cf-116">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d05cf-116">The RouteFilter</span></span>

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

### <span data-ttu-id="d05cf-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d05cf-117">-Confirm</span></span>
<span data-ttu-id="d05cf-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d05cf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d05cf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d05cf-119">-WhatIf</span></span>
<span data-ttu-id="d05cf-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d05cf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d05cf-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d05cf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d05cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05cf-122">-DefaultProfile</span></span>
<span data-ttu-id="d05cf-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d05cf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d05cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05cf-124">CommonParameters</span></span>
<span data-ttu-id="d05cf-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d05cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05cf-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05cf-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d05cf-127">INPUTS</span></span>

### <span data-ttu-id="d05cf-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d05cf-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d05cf-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d05cf-129">OUTPUTS</span></span>

### <span data-ttu-id="d05cf-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="d05cf-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="d05cf-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d05cf-131">NOTES</span></span>

## <span data-ttu-id="d05cf-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d05cf-132">RELATED LINKS</span></span>

