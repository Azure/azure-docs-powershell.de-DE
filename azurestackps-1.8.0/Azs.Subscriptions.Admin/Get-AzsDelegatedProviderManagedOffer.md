---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827896"
---
# <span data-ttu-id="6df97-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="6df97-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="6df97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6df97-102">SYNOPSIS</span></span>
<span data-ttu-id="6df97-103">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="6df97-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="6df97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6df97-104">SYNTAX</span></span>

### <span data-ttu-id="6df97-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6df97-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="6df97-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6df97-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="6df97-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df97-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6df97-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6df97-108">DESCRIPTION</span></span>
<span data-ttu-id="6df97-109">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="6df97-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="6df97-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6df97-110">EXAMPLES</span></span>

### <span data-ttu-id="6df97-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6df97-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="6df97-112">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="6df97-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="6df97-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6df97-113">PARAMETERS</span></span>

### <span data-ttu-id="6df97-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="6df97-114">-DelegatedProviderId</span></span>
<span data-ttu-id="6df97-115">DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6df97-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df97-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6df97-116">-Name</span></span>
<span data-ttu-id="6df97-117">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="6df97-117">Name of an offer.</span></span>

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

### <span data-ttu-id="6df97-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6df97-118">-ResourceId</span></span>
<span data-ttu-id="6df97-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6df97-119">The resource id.</span></span>

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

### <span data-ttu-id="6df97-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="6df97-120">-Skip</span></span>
<span data-ttu-id="6df97-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6df97-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df97-122">-Top</span><span class="sxs-lookup"><span data-stu-id="6df97-122">-Top</span></span>
<span data-ttu-id="6df97-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="6df97-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6df97-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6df97-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df97-125">CommonParameters</span></span>
<span data-ttu-id="6df97-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df97-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df97-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df97-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6df97-128">INPUTS</span></span>

## <span data-ttu-id="6df97-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6df97-129">OUTPUTS</span></span>

### <span data-ttu-id="6df97-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="6df97-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="6df97-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6df97-131">NOTES</span></span>

## <span data-ttu-id="6df97-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6df97-132">RELATED LINKS</span></span>

