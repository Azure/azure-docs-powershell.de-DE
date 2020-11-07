---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848776"
---
# <span data-ttu-id="09eef-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09eef-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="09eef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09eef-102">SYNOPSIS</span></span>
<span data-ttu-id="09eef-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="09eef-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09eef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09eef-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09eef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09eef-105">DESCRIPTION</span></span>
<span data-ttu-id="09eef-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="09eef-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="09eef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09eef-107">EXAMPLES</span></span>

### <span data-ttu-id="09eef-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09eef-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="09eef-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="09eef-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="09eef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09eef-110">PARAMETERS</span></span>

### <span data-ttu-id="09eef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09eef-111">-DefaultProfile</span></span>
<span data-ttu-id="09eef-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09eef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09eef-113">-Name</span><span class="sxs-lookup"><span data-stu-id="09eef-113">-Name</span></span>
<span data-ttu-id="09eef-114">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="09eef-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09eef-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="09eef-115">-RouteFilter</span></span>
<span data-ttu-id="09eef-116">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="09eef-116">The RouteFilter</span></span>

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

### <span data-ttu-id="09eef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09eef-117">CommonParameters</span></span>
<span data-ttu-id="09eef-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09eef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09eef-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09eef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09eef-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09eef-120">INPUTS</span></span>

### <span data-ttu-id="09eef-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="09eef-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="09eef-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09eef-122">OUTPUTS</span></span>

### <span data-ttu-id="09eef-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="09eef-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="09eef-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="09eef-124">NOTES</span></span>

## <span data-ttu-id="09eef-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09eef-125">RELATED LINKS</span></span>

