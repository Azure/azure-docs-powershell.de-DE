---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007169"
---
# <span data-ttu-id="99c85-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99c85-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="99c85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99c85-102">SYNOPSIS</span></span>
<span data-ttu-id="99c85-103">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="99c85-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="99c85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c85-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="99c85-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99c85-105">DESCRIPTION</span></span>
<span data-ttu-id="99c85-106">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="99c85-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="99c85-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99c85-107">EXAMPLES</span></span>

### <span data-ttu-id="99c85-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99c85-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="99c85-109">Gibt eine Liste der virtuellen Netzwerke für den Azure-Stapel Stempel zurück.</span><span class="sxs-lookup"><span data-stu-id="99c85-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="99c85-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99c85-110">PARAMETERS</span></span>

### <span data-ttu-id="99c85-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="99c85-111">-Filter</span></span>
<span data-ttu-id="99c85-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="99c85-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="99c85-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="99c85-113">-OrderBy</span></span>
<span data-ttu-id="99c85-114">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c85-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="99c85-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="99c85-115">-Skip</span></span>
<span data-ttu-id="99c85-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="99c85-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="99c85-117">-Top</span><span class="sxs-lookup"><span data-stu-id="99c85-117">-Top</span></span>
<span data-ttu-id="99c85-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="99c85-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="99c85-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="99c85-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="99c85-120">-Inline count</span><span class="sxs-lookup"><span data-stu-id="99c85-120">-InlineCount</span></span>
<span data-ttu-id="99c85-121">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c85-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="99c85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c85-122">CommonParameters</span></span>
<span data-ttu-id="99c85-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c85-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c85-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c85-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99c85-125">INPUTS</span></span>

## <span data-ttu-id="99c85-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99c85-126">OUTPUTS</span></span>

### <span data-ttu-id="99c85-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99c85-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="99c85-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="99c85-128">NOTES</span></span>

## <span data-ttu-id="99c85-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99c85-129">RELATED LINKS</span></span>
