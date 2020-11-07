---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827915"
---
# <span data-ttu-id="90c2c-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="90c2c-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="90c2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="90c2c-103">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="90c2c-103">List of public IP addresses.</span></span>

## <span data-ttu-id="90c2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90c2c-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="90c2c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="90c2c-106">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="90c2c-106">List of public IP addresses.</span></span>

## <span data-ttu-id="90c2c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="90c2c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90c2c-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="90c2c-109">Rufen Sie die Liste der öffentlichen IP-Adressen ab, die entweder zugewiesen oder nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="90c2c-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="90c2c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c2c-110">PARAMETERS</span></span>

### <span data-ttu-id="90c2c-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="90c2c-111">-Filter</span></span>
<span data-ttu-id="90c2c-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="90c2c-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="90c2c-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="90c2c-113">-OrderBy</span></span>
<span data-ttu-id="90c2c-114">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="90c2c-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="90c2c-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="90c2c-115">-Skip</span></span>
<span data-ttu-id="90c2c-116">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="90c2c-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="90c2c-117">-Top</span><span class="sxs-lookup"><span data-stu-id="90c2c-117">-Top</span></span>
<span data-ttu-id="90c2c-118">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="90c2c-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="90c2c-119">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="90c2c-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="90c2c-120">-Inline count</span><span class="sxs-lookup"><span data-stu-id="90c2c-120">-InlineCount</span></span>
<span data-ttu-id="90c2c-121">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="90c2c-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="90c2c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c2c-122">CommonParameters</span></span>
<span data-ttu-id="90c2c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c2c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c2c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c2c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c2c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90c2c-125">INPUTS</span></span>

## <span data-ttu-id="90c2c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90c2c-126">OUTPUTS</span></span>

### <span data-ttu-id="90c2c-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="90c2c-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="90c2c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="90c2c-128">NOTES</span></span>

## <span data-ttu-id="90c2c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90c2c-129">RELATED LINKS</span></span>
