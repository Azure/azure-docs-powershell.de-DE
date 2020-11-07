---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826167"
---
# <span data-ttu-id="a25fb-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="a25fb-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="a25fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a25fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a25fb-103">Gibt Bilder virtueller Computer zurück, die in das Platform-Image-Repository geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="a25fb-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="a25fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a25fb-104">SYNTAX</span></span>

### <span data-ttu-id="a25fb-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a25fb-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a25fb-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a25fb-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a25fb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a25fb-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a25fb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a25fb-108">DESCRIPTION</span></span>
<span data-ttu-id="a25fb-109">Gibt Platt Form Bilder zurück.</span><span class="sxs-lookup"><span data-stu-id="a25fb-109">Returns platform images.</span></span>

## <span data-ttu-id="a25fb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a25fb-110">EXAMPLES</span></span>

### <span data-ttu-id="a25fb-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a25fb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="a25fb-112">Gibt die Bilder virtueller Computer zurück, die in das Platform-Image-Repository am Standort local geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="a25fb-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="a25fb-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a25fb-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="a25fb-114">Abrufen eines bestimmten Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="a25fb-114">Get a specific platform image.</span></span>

## <span data-ttu-id="a25fb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a25fb-115">PARAMETERS</span></span>

### <span data-ttu-id="a25fb-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="a25fb-116">-Location</span></span>
<span data-ttu-id="a25fb-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a25fb-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25fb-118">-Angebot</span><span class="sxs-lookup"><span data-stu-id="a25fb-118">-Offer</span></span>
<span data-ttu-id="a25fb-119">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="a25fb-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a25fb-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a25fb-120">-Publisher</span></span>
<span data-ttu-id="a25fb-121">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="a25fb-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a25fb-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a25fb-122">-ResourceId</span></span>
<span data-ttu-id="a25fb-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a25fb-123">The resource id.</span></span>

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

### <span data-ttu-id="a25fb-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="a25fb-124">-Sku</span></span>
<span data-ttu-id="a25fb-125">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="a25fb-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a25fb-126">-Version</span><span class="sxs-lookup"><span data-stu-id="a25fb-126">-Version</span></span>
<span data-ttu-id="a25fb-127">Die Version des Platt Form Bilds.</span><span class="sxs-lookup"><span data-stu-id="a25fb-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="a25fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25fb-128">CommonParameters</span></span>
<span data-ttu-id="a25fb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25fb-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25fb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a25fb-131">INPUTS</span></span>

## <span data-ttu-id="a25fb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a25fb-132">OUTPUTS</span></span>

### <span data-ttu-id="a25fb-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="a25fb-133">PlatformImageObject</span></span>

## <span data-ttu-id="a25fb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a25fb-134">NOTES</span></span>

## <span data-ttu-id="a25fb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a25fb-135">RELATED LINKS</span></span>

