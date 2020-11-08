---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d81043e165600a549bace91458449577b23dbd8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007256"
---
# <span data-ttu-id="46e00-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="46e00-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="46e00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46e00-102">SYNOPSIS</span></span>
<span data-ttu-id="46e00-103">Gibt eine Liste von metrischen Definitionen für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="46e00-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="46e00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e00-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="46e00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46e00-105">DESCRIPTION</span></span>
<span data-ttu-id="46e00-106">Gibt eine Liste von metrischen Definitionen für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="46e00-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="46e00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46e00-107">EXAMPLES</span></span>

### <span data-ttu-id="46e00-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46e00-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="46e00-109">Rufen Sie die Liste der metrischen Definitionen für den Warteschlangendienst ab.</span><span class="sxs-lookup"><span data-stu-id="46e00-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="46e00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e00-110">PARAMETERS</span></span>

### <span data-ttu-id="46e00-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="46e00-111">-FarmName</span></span>
<span data-ttu-id="46e00-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="46e00-112">Farm Id.</span></span>

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

### <span data-ttu-id="46e00-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e00-113">-ResourceGroupName</span></span>
<span data-ttu-id="46e00-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46e00-114">Resource group name.</span></span>

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

### <span data-ttu-id="46e00-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="46e00-115">-Skip</span></span>
<span data-ttu-id="46e00-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="46e00-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="46e00-117">-Top</span><span class="sxs-lookup"><span data-stu-id="46e00-117">-Top</span></span>
<span data-ttu-id="46e00-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="46e00-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="46e00-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="46e00-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="46e00-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e00-120">CommonParameters</span></span>
<span data-ttu-id="46e00-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e00-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e00-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e00-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e00-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46e00-123">INPUTS</span></span>

## <span data-ttu-id="46e00-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46e00-124">OUTPUTS</span></span>

### <span data-ttu-id="46e00-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="46e00-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="46e00-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="46e00-126">NOTES</span></span>

## <span data-ttu-id="46e00-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46e00-127">RELATED LINKS</span></span>
