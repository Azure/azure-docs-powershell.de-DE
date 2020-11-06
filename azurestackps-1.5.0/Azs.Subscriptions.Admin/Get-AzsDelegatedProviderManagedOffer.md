---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57e195f1d42b4d1df26344133c10d7c0d40e1f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474706"
---
# <span data-ttu-id="558d4-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="558d4-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="558d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="558d4-102">SYNOPSIS</span></span>
<span data-ttu-id="558d4-103">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="558d4-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="558d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="558d4-104">SYNTAX</span></span>

### <span data-ttu-id="558d4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="558d4-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="558d4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="558d4-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="558d4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="558d4-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="558d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="558d4-108">DESCRIPTION</span></span>
<span data-ttu-id="558d4-109">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="558d4-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="558d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="558d4-110">EXAMPLES</span></span>

### <span data-ttu-id="558d4-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="558d4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="558d4-112">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="558d4-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="558d4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="558d4-113">PARAMETERS</span></span>

### <span data-ttu-id="558d4-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="558d4-114">-DelegatedProviderId</span></span>
<span data-ttu-id="558d4-115">DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="558d4-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="558d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="558d4-116">-Name</span></span>
<span data-ttu-id="558d4-117">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="558d4-117">Name of an offer.</span></span>

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

### <span data-ttu-id="558d4-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="558d4-118">-ResourceId</span></span>
<span data-ttu-id="558d4-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="558d4-119">The resource id.</span></span>

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

### <span data-ttu-id="558d4-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="558d4-120">-Skip</span></span>
<span data-ttu-id="558d4-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="558d4-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="558d4-122">-Top</span><span class="sxs-lookup"><span data-stu-id="558d4-122">-Top</span></span>
<span data-ttu-id="558d4-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="558d4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="558d4-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="558d4-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="558d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558d4-125">CommonParameters</span></span>
<span data-ttu-id="558d4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558d4-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="558d4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558d4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="558d4-128">INPUTS</span></span>

## <span data-ttu-id="558d4-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="558d4-129">OUTPUTS</span></span>

### <span data-ttu-id="558d4-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="558d4-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="558d4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="558d4-131">NOTES</span></span>

## <span data-ttu-id="558d4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="558d4-132">RELATED LINKS</span></span>

