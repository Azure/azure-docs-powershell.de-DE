---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 822452c1c6b83669759bae2c861ee3456a13a0dc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006966"
---
# <span data-ttu-id="b0c81-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="b0c81-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="b0c81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0c81-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c81-103">Gibt eine Liste von Metriken für den BLOB-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="b0c81-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="b0c81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0c81-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0c81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0c81-105">DESCRIPTION</span></span>
<span data-ttu-id="b0c81-106">Gibt eine Liste von Metriken für den BLOB-Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="b0c81-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="b0c81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0c81-107">EXAMPLES</span></span>

### <span data-ttu-id="b0c81-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0c81-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b0c81-109">Abrufen einer Liste der Metriken für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="b0c81-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="b0c81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c81-110">PARAMETERS</span></span>

### <span data-ttu-id="b0c81-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="b0c81-111">-FarmName</span></span>
<span data-ttu-id="b0c81-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="b0c81-112">Farm Id.</span></span>

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

### <span data-ttu-id="b0c81-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c81-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0c81-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0c81-114">Resource group name.</span></span>

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

### <span data-ttu-id="b0c81-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b0c81-115">-Skip</span></span>
<span data-ttu-id="b0c81-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="b0c81-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b0c81-117">-Top</span><span class="sxs-lookup"><span data-stu-id="b0c81-117">-Top</span></span>
<span data-ttu-id="b0c81-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="b0c81-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b0c81-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b0c81-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b0c81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c81-120">CommonParameters</span></span>
<span data-ttu-id="b0c81-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c81-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c81-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c81-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0c81-123">INPUTS</span></span>

## <span data-ttu-id="b0c81-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0c81-124">OUTPUTS</span></span>

### <span data-ttu-id="b0c81-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="b0c81-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="b0c81-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0c81-126">NOTES</span></span>

## <span data-ttu-id="b0c81-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0c81-127">RELATED LINKS</span></span>
