---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840611"
---
# <span data-ttu-id="80dd9-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="80dd9-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="80dd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="80dd9-103">Gibt eine Liste von metrischen Definitionen für eine Speicher Farm zurück.</span><span class="sxs-lookup"><span data-stu-id="80dd9-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="80dd9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80dd9-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="80dd9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="80dd9-106">Gibt eine Liste von metrischen Definitionen für eine Speicher Farm zurück.</span><span class="sxs-lookup"><span data-stu-id="80dd9-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="80dd9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="80dd9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80dd9-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="80dd9-109">Rufen Sie die Liste der metrischen Definitionen für eine Speicher Farm ab.</span><span class="sxs-lookup"><span data-stu-id="80dd9-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="80dd9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80dd9-110">PARAMETERS</span></span>

### <span data-ttu-id="80dd9-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="80dd9-111">-FarmName</span></span>
<span data-ttu-id="80dd9-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="80dd9-112">Farm Id.</span></span>

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

### <span data-ttu-id="80dd9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80dd9-113">-ResourceGroupName</span></span>
<span data-ttu-id="80dd9-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80dd9-114">Resource group name.</span></span>

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

### <span data-ttu-id="80dd9-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="80dd9-115">-Skip</span></span>
<span data-ttu-id="80dd9-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="80dd9-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="80dd9-117">-Top</span><span class="sxs-lookup"><span data-stu-id="80dd9-117">-Top</span></span>
<span data-ttu-id="80dd9-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="80dd9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="80dd9-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="80dd9-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="80dd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dd9-120">CommonParameters</span></span>
<span data-ttu-id="80dd9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80dd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dd9-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dd9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dd9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80dd9-123">INPUTS</span></span>

## <span data-ttu-id="80dd9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80dd9-124">OUTPUTS</span></span>

### <span data-ttu-id="80dd9-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="80dd9-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="80dd9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="80dd9-126">NOTES</span></span>

## <span data-ttu-id="80dd9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80dd9-127">RELATED LINKS</span></span>
