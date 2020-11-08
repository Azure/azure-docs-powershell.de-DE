---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007196"
---
# <span data-ttu-id="22744-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="22744-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="22744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22744-102">SYNOPSIS</span></span>
<span data-ttu-id="22744-103">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="22744-103">List of public IP addresses.</span></span>

## <span data-ttu-id="22744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22744-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="22744-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22744-105">DESCRIPTION</span></span>
<span data-ttu-id="22744-106">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="22744-106">List of public IP addresses.</span></span>

## <span data-ttu-id="22744-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22744-107">EXAMPLES</span></span>

### <span data-ttu-id="22744-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22744-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="22744-109">Rufen Sie die Liste der öffentlichen IP-Adressen ab, die entweder zugewiesen oder nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="22744-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="22744-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22744-110">PARAMETERS</span></span>

### <span data-ttu-id="22744-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="22744-111">-Filter</span></span>
<span data-ttu-id="22744-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="22744-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="22744-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="22744-113">-OrderBy</span></span>
<span data-ttu-id="22744-114">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="22744-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="22744-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="22744-115">-Skip</span></span>
<span data-ttu-id="22744-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="22744-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="22744-117">-Top</span><span class="sxs-lookup"><span data-stu-id="22744-117">-Top</span></span>
<span data-ttu-id="22744-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="22744-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="22744-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="22744-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="22744-120">-Inline count</span><span class="sxs-lookup"><span data-stu-id="22744-120">-InlineCount</span></span>
<span data-ttu-id="22744-121">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="22744-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="22744-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22744-122">CommonParameters</span></span>
<span data-ttu-id="22744-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22744-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22744-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22744-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22744-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22744-125">INPUTS</span></span>

## <span data-ttu-id="22744-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22744-126">OUTPUTS</span></span>

### <span data-ttu-id="22744-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22744-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="22744-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="22744-128">NOTES</span></span>

## <span data-ttu-id="22744-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22744-129">RELATED LINKS</span></span>
