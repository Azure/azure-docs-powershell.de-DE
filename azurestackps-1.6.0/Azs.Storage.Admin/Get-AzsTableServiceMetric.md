---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 007f5116c17e9bf2c1df742e0f11c9a86844134b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475125"
---
# <span data-ttu-id="3f89c-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="3f89c-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="3f89c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f89c-103">Gibt eine Liste von Metriken für den tabellendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="3f89c-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="3f89c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f89c-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f89c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f89c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f89c-106">Gibt eine Liste von Metriken für den tabellendienst zurück.</span><span class="sxs-lookup"><span data-stu-id="3f89c-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="3f89c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f89c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f89c-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f89c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="3f89c-109">Rufen Sie die Liste der Metriken für den tabellendienst ab.</span><span class="sxs-lookup"><span data-stu-id="3f89c-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="3f89c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f89c-110">PARAMETERS</span></span>

### <span data-ttu-id="3f89c-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="3f89c-111">-FarmName</span></span>
<span data-ttu-id="3f89c-112">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="3f89c-112">Farm Id.</span></span>

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

### <span data-ttu-id="3f89c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f89c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3f89c-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f89c-114">Resource group name.</span></span>

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

### <span data-ttu-id="3f89c-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="3f89c-115">-Skip</span></span>
<span data-ttu-id="3f89c-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="3f89c-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3f89c-117">-Top</span><span class="sxs-lookup"><span data-stu-id="3f89c-117">-Top</span></span>
<span data-ttu-id="3f89c-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="3f89c-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3f89c-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f89c-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3f89c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f89c-120">CommonParameters</span></span>
<span data-ttu-id="3f89c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f89c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f89c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f89c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f89c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f89c-123">INPUTS</span></span>

## <span data-ttu-id="3f89c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f89c-124">OUTPUTS</span></span>

### <span data-ttu-id="3f89c-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="3f89c-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="3f89c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f89c-126">NOTES</span></span>

## <span data-ttu-id="3f89c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f89c-127">RELATED LINKS</span></span>

