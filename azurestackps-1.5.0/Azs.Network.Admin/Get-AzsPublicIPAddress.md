---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3996096b692a7e242fc6cf42288508bdc4625cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474994"
---
# <span data-ttu-id="1e59e-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e59e-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="1e59e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e59e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e59e-103">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1e59e-103">List of public IP addresses.</span></span>

## <span data-ttu-id="1e59e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e59e-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e59e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e59e-105">DESCRIPTION</span></span>
<span data-ttu-id="1e59e-106">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="1e59e-106">List of public IP addresses.</span></span>

## <span data-ttu-id="1e59e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e59e-107">EXAMPLES</span></span>

### <span data-ttu-id="1e59e-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e59e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="1e59e-109">Rufen Sie die Liste der öffentlichen IP-Adressen ab, die entweder zugewiesen oder nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="1e59e-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="1e59e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e59e-110">PARAMETERS</span></span>

### <span data-ttu-id="1e59e-111">-Filter</span><span class="sxs-lookup"><span data-stu-id="1e59e-111">-Filter</span></span>
<span data-ttu-id="1e59e-112">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="1e59e-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="1e59e-113">-Inline count</span><span class="sxs-lookup"><span data-stu-id="1e59e-113">-InlineCount</span></span>
<span data-ttu-id="1e59e-114">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="1e59e-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="1e59e-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="1e59e-115">-OrderBy</span></span>
<span data-ttu-id="1e59e-116">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="1e59e-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="1e59e-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="1e59e-117">-Skip</span></span>
<span data-ttu-id="1e59e-118">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="1e59e-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1e59e-119">-Top</span><span class="sxs-lookup"><span data-stu-id="1e59e-119">-Top</span></span>
<span data-ttu-id="1e59e-120">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="1e59e-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1e59e-121">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e59e-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1e59e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e59e-122">CommonParameters</span></span>
<span data-ttu-id="1e59e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e59e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e59e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e59e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e59e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e59e-125">INPUTS</span></span>

## <span data-ttu-id="1e59e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e59e-126">OUTPUTS</span></span>

### <span data-ttu-id="1e59e-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1e59e-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="1e59e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e59e-128">NOTES</span></span>

## <span data-ttu-id="1e59e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e59e-129">RELATED LINKS</span></span>

