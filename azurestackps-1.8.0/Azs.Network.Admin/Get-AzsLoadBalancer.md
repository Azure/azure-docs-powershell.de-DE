---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827935"
---
# <span data-ttu-id="a7c83-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7c83-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="a7c83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7c83-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c83-103">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="a7c83-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a7c83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7c83-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a7c83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7c83-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c83-106">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="a7c83-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a7c83-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7c83-107">EXAMPLES</span></span>

### <span data-ttu-id="a7c83-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7c83-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="a7c83-109">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="a7c83-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="a7c83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c83-110">PARAMETERS</span></span>

### <span data-ttu-id="a7c83-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="a7c83-111">-Filter</span></span>
<span data-ttu-id="a7c83-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="a7c83-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="a7c83-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a7c83-113">-OrderBy</span></span>
<span data-ttu-id="a7c83-114">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c83-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="a7c83-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="a7c83-115">-Skip</span></span>
<span data-ttu-id="a7c83-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="a7c83-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a7c83-117">-Top</span><span class="sxs-lookup"><span data-stu-id="a7c83-117">-Top</span></span>
<span data-ttu-id="a7c83-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="a7c83-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a7c83-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="a7c83-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a7c83-120">-Inline count</span><span class="sxs-lookup"><span data-stu-id="a7c83-120">-InlineCount</span></span>
<span data-ttu-id="a7c83-121">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c83-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="a7c83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c83-122">CommonParameters</span></span>
<span data-ttu-id="a7c83-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c83-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c83-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c83-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7c83-125">INPUTS</span></span>

## <span data-ttu-id="a7c83-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7c83-126">OUTPUTS</span></span>

### <span data-ttu-id="a7c83-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a7c83-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="a7c83-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7c83-128">NOTES</span></span>

## <span data-ttu-id="a7c83-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7c83-129">RELATED LINKS</span></span>
