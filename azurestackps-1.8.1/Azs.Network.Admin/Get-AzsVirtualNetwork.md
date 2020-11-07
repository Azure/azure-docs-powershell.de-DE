---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840723"
---
# <span data-ttu-id="b82d9-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b82d9-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="b82d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b82d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b82d9-103">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b82d9-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="b82d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b82d9-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b82d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b82d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b82d9-106">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b82d9-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="b82d9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b82d9-107">EXAMPLES</span></span>

### <span data-ttu-id="b82d9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b82d9-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="b82d9-109">Gibt eine Liste der virtuellen Netzwerke für den Azure-Stapel Stempel zurück.</span><span class="sxs-lookup"><span data-stu-id="b82d9-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="b82d9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b82d9-110">PARAMETERS</span></span>

### <span data-ttu-id="b82d9-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="b82d9-111">-Filter</span></span>
<span data-ttu-id="b82d9-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="b82d9-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="b82d9-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b82d9-113">-OrderBy</span></span>
<span data-ttu-id="b82d9-114">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="b82d9-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b82d9-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="b82d9-115">-Skip</span></span>
<span data-ttu-id="b82d9-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="b82d9-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b82d9-117">-Top</span><span class="sxs-lookup"><span data-stu-id="b82d9-117">-Top</span></span>
<span data-ttu-id="b82d9-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="b82d9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b82d9-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b82d9-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b82d9-120">-Inline count</span><span class="sxs-lookup"><span data-stu-id="b82d9-120">-InlineCount</span></span>
<span data-ttu-id="b82d9-121">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="b82d9-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b82d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82d9-122">CommonParameters</span></span>
<span data-ttu-id="b82d9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82d9-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b82d9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82d9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b82d9-125">INPUTS</span></span>

## <span data-ttu-id="b82d9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b82d9-126">OUTPUTS</span></span>

### <span data-ttu-id="b82d9-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b82d9-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="b82d9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b82d9-128">NOTES</span></span>

## <span data-ttu-id="b82d9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b82d9-129">RELATED LINKS</span></span>
