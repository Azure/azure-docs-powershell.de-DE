---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2776c768f49dabdea8483ff601f129e80bfc2dc
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840691"
---
# <span data-ttu-id="f7229-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="f7229-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="f7229-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7229-102">SYNOPSIS</span></span>
<span data-ttu-id="f7229-103">Gibt eine Liste von Metriken für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="f7229-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="f7229-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7229-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7229-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7229-105">DESCRIPTION</span></span>
<span data-ttu-id="f7229-106">Gibt eine Liste von Metriken für den Warteschlangendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="f7229-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="f7229-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7229-107">EXAMPLES</span></span>

### <span data-ttu-id="f7229-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7229-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f7229-109">Rufen Sie die Liste der Metriken für den Warteschlangendienst ab.</span><span class="sxs-lookup"><span data-stu-id="f7229-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="f7229-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7229-110">PARAMETERS</span></span>

### <span data-ttu-id="f7229-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f7229-111">-FarmName</span></span>
<span data-ttu-id="f7229-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="f7229-112">Farm Id.</span></span>

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

### <span data-ttu-id="f7229-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7229-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7229-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7229-114">Resource group name.</span></span>

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

### <span data-ttu-id="f7229-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="f7229-115">-Skip</span></span>
<span data-ttu-id="f7229-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7229-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f7229-117">-Top</span><span class="sxs-lookup"><span data-stu-id="f7229-117">-Top</span></span>
<span data-ttu-id="f7229-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="f7229-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f7229-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7229-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f7229-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7229-120">CommonParameters</span></span>
<span data-ttu-id="f7229-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7229-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7229-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7229-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7229-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7229-123">INPUTS</span></span>

## <span data-ttu-id="f7229-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7229-124">OUTPUTS</span></span>

### <span data-ttu-id="f7229-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="f7229-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="f7229-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7229-126">NOTES</span></span>

## <span data-ttu-id="f7229-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7229-127">RELATED LINKS</span></span>
