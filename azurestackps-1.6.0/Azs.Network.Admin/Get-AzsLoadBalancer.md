---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87966f8ac96ab70f7617f857d9f1d83945b5e639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475245"
---
# <span data-ttu-id="6c76d-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c76d-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="6c76d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c76d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c76d-103">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="6c76d-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="6c76d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c76d-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c76d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c76d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c76d-106">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="6c76d-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="6c76d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c76d-107">EXAMPLES</span></span>

### <span data-ttu-id="6c76d-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c76d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="6c76d-109">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="6c76d-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="6c76d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c76d-110">PARAMETERS</span></span>

### <span data-ttu-id="6c76d-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="6c76d-111">-Filter</span></span>
<span data-ttu-id="6c76d-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="6c76d-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c76d-113">-Inline count</span><span class="sxs-lookup"><span data-stu-id="6c76d-113">-InlineCount</span></span>
<span data-ttu-id="6c76d-114">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="6c76d-114">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c76d-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6c76d-115">-OrderBy</span></span>
<span data-ttu-id="6c76d-116">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="6c76d-116">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c76d-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="6c76d-117">-Skip</span></span>
<span data-ttu-id="6c76d-118">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c76d-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c76d-119">-Top</span><span class="sxs-lookup"><span data-stu-id="6c76d-119">-Top</span></span>
<span data-ttu-id="6c76d-120">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="6c76d-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6c76d-121">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c76d-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6c76d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c76d-122">CommonParameters</span></span>
<span data-ttu-id="6c76d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c76d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c76d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c76d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c76d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c76d-125">INPUTS</span></span>

## <span data-ttu-id="6c76d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c76d-126">OUTPUTS</span></span>

### <span data-ttu-id="6c76d-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c76d-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="6c76d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c76d-128">NOTES</span></span>

## <span data-ttu-id="6c76d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c76d-129">RELATED LINKS</span></span>

