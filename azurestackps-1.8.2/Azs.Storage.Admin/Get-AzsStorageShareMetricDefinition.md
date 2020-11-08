---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007297"
---
# <span data-ttu-id="57714-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="57714-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="57714-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57714-102">SYNOPSIS</span></span>
<span data-ttu-id="57714-103">Gibt eine Liste von metrischen Definitionen für eine Speicherfreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="57714-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="57714-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57714-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="57714-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57714-105">DESCRIPTION</span></span>
<span data-ttu-id="57714-106">Gibt eine Liste von metrischen Definitionen für eine Speicherfreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="57714-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="57714-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57714-107">EXAMPLES</span></span>

### <span data-ttu-id="57714-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57714-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="57714-109">Rufen Sie die Liste der metrischen Definitionen für eine Speicherfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="57714-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="57714-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57714-110">PARAMETERS</span></span>

### <span data-ttu-id="57714-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="57714-111">-FarmName</span></span>
<span data-ttu-id="57714-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="57714-112">Farm Id.</span></span>

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

### <span data-ttu-id="57714-113">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="57714-113">-ShareName</span></span>
<span data-ttu-id="57714-114">Freigabename.</span><span class="sxs-lookup"><span data-stu-id="57714-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57714-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57714-115">-ResourceGroupName</span></span>
<span data-ttu-id="57714-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57714-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57714-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="57714-117">-Skip</span></span>
<span data-ttu-id="57714-118">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="57714-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57714-119">-Top</span><span class="sxs-lookup"><span data-stu-id="57714-119">-Top</span></span>
<span data-ttu-id="57714-120">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="57714-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="57714-121">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="57714-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57714-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57714-122">CommonParameters</span></span>
<span data-ttu-id="57714-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57714-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57714-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57714-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57714-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57714-125">INPUTS</span></span>

## <span data-ttu-id="57714-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57714-126">OUTPUTS</span></span>

### <span data-ttu-id="57714-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="57714-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="57714-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="57714-128">NOTES</span></span>

## <span data-ttu-id="57714-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57714-129">RELATED LINKS</span></span>
