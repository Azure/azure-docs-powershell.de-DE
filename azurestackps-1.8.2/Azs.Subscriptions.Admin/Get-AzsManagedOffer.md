---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007032"
---
# <span data-ttu-id="c64c9-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="c64c9-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="c64c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c64c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c64c9-103">Rufen Sie die Liste der Angebote als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="c64c9-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="c64c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c64c9-104">SYNTAX</span></span>

### <span data-ttu-id="c64c9-105">Bauteile (Standard)</span><span class="sxs-lookup"><span data-stu-id="c64c9-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c64c9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c64c9-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c64c9-107">Liste</span><span class="sxs-lookup"><span data-stu-id="c64c9-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c64c9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c64c9-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c64c9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c64c9-109">DESCRIPTION</span></span>
<span data-ttu-id="c64c9-110">Rufen Sie die Liste der Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="c64c9-110">Get the list of offers.</span></span>

## <span data-ttu-id="c64c9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c64c9-111">EXAMPLES</span></span>

### <span data-ttu-id="c64c9-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c64c9-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="c64c9-113">Rufen Sie die Liste der Angebote als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="c64c9-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="c64c9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c64c9-114">PARAMETERS</span></span>

### <span data-ttu-id="c64c9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c64c9-115">-Name</span></span>
<span data-ttu-id="c64c9-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="c64c9-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c64c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="c64c9-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c64c9-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c64c9-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c64c9-119">-ResourceId</span></span>
<span data-ttu-id="c64c9-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c64c9-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64c9-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="c64c9-121">-Skip</span></span>
<span data-ttu-id="c64c9-122">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c64c9-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c64c9-123">-Top</span><span class="sxs-lookup"><span data-stu-id="c64c9-123">-Top</span></span>
<span data-ttu-id="c64c9-124">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="c64c9-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c64c9-125">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c64c9-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c64c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64c9-126">CommonParameters</span></span>
<span data-ttu-id="c64c9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64c9-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64c9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64c9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c64c9-129">INPUTS</span></span>

## <span data-ttu-id="c64c9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c64c9-130">OUTPUTS</span></span>

### <span data-ttu-id="c64c9-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="c64c9-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="c64c9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c64c9-132">NOTES</span></span>

## <span data-ttu-id="c64c9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c64c9-133">RELATED LINKS</span></span>

