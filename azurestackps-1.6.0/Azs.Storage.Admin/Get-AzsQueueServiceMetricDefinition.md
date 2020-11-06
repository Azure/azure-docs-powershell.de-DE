---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f93ea2ebe9bc2d9b5ca63dd0f2ae4d145c8b038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475345"
---
# <span data-ttu-id="cdd02-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="cdd02-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="cdd02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdd02-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd02-103">Gibt eine Liste von metrischen Definitionen für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd02-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="cdd02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd02-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cdd02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdd02-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd02-106">Gibt eine Liste von metrischen Definitionen für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd02-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="cdd02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdd02-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd02-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cdd02-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="cdd02-109">Rufen Sie die Liste der metrischen Definitionen für den Warteschlangendienst ab.</span><span class="sxs-lookup"><span data-stu-id="cdd02-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="cdd02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd02-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd02-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="cdd02-111">-FarmName</span></span>
<span data-ttu-id="cdd02-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="cdd02-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd02-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd02-113">-ResourceGroupName</span></span>
<span data-ttu-id="cdd02-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cdd02-114">Resource group name.</span></span>

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

### <span data-ttu-id="cdd02-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="cdd02-115">-Skip</span></span>
<span data-ttu-id="cdd02-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdd02-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd02-117">-Top</span><span class="sxs-lookup"><span data-stu-id="cdd02-117">-Top</span></span>
<span data-ttu-id="cdd02-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd02-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cdd02-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="cdd02-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd02-120">CommonParameters</span></span>
<span data-ttu-id="cdd02-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd02-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd02-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd02-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdd02-123">INPUTS</span></span>

## <span data-ttu-id="cdd02-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdd02-124">OUTPUTS</span></span>

### <span data-ttu-id="cdd02-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="cdd02-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="cdd02-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdd02-126">NOTES</span></span>

## <span data-ttu-id="cdd02-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdd02-127">RELATED LINKS</span></span>

