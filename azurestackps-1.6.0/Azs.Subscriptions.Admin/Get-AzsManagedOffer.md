---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475413"
---
# <span data-ttu-id="0f234-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="0f234-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="0f234-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f234-102">SYNOPSIS</span></span>
<span data-ttu-id="0f234-103">Rufen Sie die Liste der Angebote als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="0f234-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="0f234-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f234-104">SYNTAX</span></span>

### <span data-ttu-id="0f234-105">Bauteile (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f234-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0f234-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0f234-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="0f234-107">Liste</span><span class="sxs-lookup"><span data-stu-id="0f234-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0f234-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f234-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0f234-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f234-109">DESCRIPTION</span></span>
<span data-ttu-id="0f234-110">Rufen Sie die Liste der Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="0f234-110">Get the list of offers.</span></span>

## <span data-ttu-id="0f234-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f234-111">EXAMPLES</span></span>

### <span data-ttu-id="0f234-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f234-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="0f234-113">Rufen Sie die Liste der Angebote als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="0f234-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="0f234-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f234-114">PARAMETERS</span></span>

### <span data-ttu-id="0f234-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f234-115">-Name</span></span>
<span data-ttu-id="0f234-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="0f234-116">Name of an offer.</span></span>

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

### <span data-ttu-id="0f234-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f234-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f234-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0f234-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0f234-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f234-119">-ResourceId</span></span>
<span data-ttu-id="0f234-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0f234-120">The resource id.</span></span>

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

### <span data-ttu-id="0f234-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="0f234-121">-Skip</span></span>
<span data-ttu-id="0f234-122">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="0f234-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0f234-123">-Top</span><span class="sxs-lookup"><span data-stu-id="0f234-123">-Top</span></span>
<span data-ttu-id="0f234-124">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="0f234-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0f234-125">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f234-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0f234-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f234-126">CommonParameters</span></span>
<span data-ttu-id="0f234-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f234-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f234-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f234-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f234-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f234-129">INPUTS</span></span>

## <span data-ttu-id="0f234-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f234-130">OUTPUTS</span></span>

### <span data-ttu-id="0f234-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="0f234-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="0f234-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f234-132">NOTES</span></span>

## <span data-ttu-id="0f234-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f234-133">RELATED LINKS</span></span>

