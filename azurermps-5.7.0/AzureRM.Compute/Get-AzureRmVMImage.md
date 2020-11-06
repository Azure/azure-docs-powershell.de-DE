---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478614"
---
# <span data-ttu-id="bce20-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bce20-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="bce20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bce20-102">SYNOPSIS</span></span>
<span data-ttu-id="bce20-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="bce20-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce20-104">SYNTAX</span></span>

### <span data-ttu-id="bce20-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="bce20-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="bce20-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="bce20-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="bce20-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bce20-107">DESCRIPTION</span></span>
<span data-ttu-id="bce20-108">Das Cmdlet " **Get-AzureRmVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="bce20-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="bce20-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bce20-109">EXAMPLES</span></span>

### <span data-ttu-id="bce20-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="bce20-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="bce20-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bce20-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="bce20-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bce20-112">PARAMETERS</span></span>

### <span data-ttu-id="bce20-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="bce20-113">-FilterExpression</span></span>
<span data-ttu-id="bce20-114">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="bce20-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="bce20-115">-Location</span></span>
<span data-ttu-id="bce20-116">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="bce20-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-117">-Angebot</span><span class="sxs-lookup"><span data-stu-id="bce20-117">-Offer</span></span>
<span data-ttu-id="bce20-118">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="bce20-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="bce20-119">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bce20-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="bce20-120">-PublisherName</span></span>
<span data-ttu-id="bce20-121">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="bce20-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="bce20-122">Verwenden Sie das Get-AzureRmVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bce20-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-123">-SKUs</span><span class="sxs-lookup"><span data-stu-id="bce20-123">-Skus</span></span>
<span data-ttu-id="bce20-124">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="bce20-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="bce20-125">Verwenden Sie das Get-AzureRmVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bce20-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-126">-Version</span><span class="sxs-lookup"><span data-stu-id="bce20-126">-Version</span></span>
<span data-ttu-id="bce20-127">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="bce20-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce20-128">CommonParameters</span></span>
<span data-ttu-id="bce20-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce20-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce20-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bce20-131">INPUTS</span></span>

### <span data-ttu-id="bce20-132">Keine</span><span class="sxs-lookup"><span data-stu-id="bce20-132">None</span></span>
<span data-ttu-id="bce20-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bce20-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bce20-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bce20-134">OUTPUTS</span></span>

## <span data-ttu-id="bce20-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bce20-135">NOTES</span></span>

## <span data-ttu-id="bce20-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bce20-136">RELATED LINKS</span></span>

[<span data-ttu-id="bce20-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bce20-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="bce20-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bce20-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="bce20-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bce20-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="bce20-140">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bce20-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


