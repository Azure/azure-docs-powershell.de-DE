---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849379"
---
# <span data-ttu-id="cba8d-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="cba8d-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="cba8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cba8d-102">SYNOPSIS</span></span>
<span data-ttu-id="cba8d-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="cba8d-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cba8d-104">SYNTAX</span></span>

### <span data-ttu-id="cba8d-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="cba8d-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba8d-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="cba8d-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba8d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cba8d-107">DESCRIPTION</span></span>
<span data-ttu-id="cba8d-108">Das Cmdlet " **Get-AzureRmVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="cba8d-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="cba8d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cba8d-109">EXAMPLES</span></span>

### <span data-ttu-id="cba8d-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="cba8d-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="cba8d-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cba8d-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="cba8d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cba8d-112">PARAMETERS</span></span>

### <span data-ttu-id="cba8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba8d-113">-DefaultProfile</span></span>
<span data-ttu-id="cba8d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cba8d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba8d-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="cba8d-115">-FilterExpression</span></span>
<span data-ttu-id="cba8d-116">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="cba8d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="cba8d-117">-Location</span></span>
<span data-ttu-id="cba8d-118">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="cba8d-119">-Angebot</span><span class="sxs-lookup"><span data-stu-id="cba8d-119">-Offer</span></span>
<span data-ttu-id="cba8d-120">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="cba8d-121">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cba8d-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="cba8d-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="cba8d-122">-PublisherName</span></span>
<span data-ttu-id="cba8d-123">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="cba8d-124">Verwenden Sie das Get-AzureRmVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cba8d-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="cba8d-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="cba8d-125">-Skus</span></span>
<span data-ttu-id="cba8d-126">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="cba8d-127">Verwenden Sie das Get-AzureRmVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cba8d-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="cba8d-128">-Version</span><span class="sxs-lookup"><span data-stu-id="cba8d-128">-Version</span></span>
<span data-ttu-id="cba8d-129">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="cba8d-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="cba8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba8d-130">CommonParameters</span></span>
<span data-ttu-id="cba8d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba8d-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba8d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cba8d-133">INPUTS</span></span>

### <span data-ttu-id="cba8d-134">Keine</span><span class="sxs-lookup"><span data-stu-id="cba8d-134">None</span></span>
<span data-ttu-id="cba8d-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cba8d-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cba8d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cba8d-136">OUTPUTS</span></span>

### <span data-ttu-id="cba8d-137">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="cba8d-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="cba8d-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="cba8d-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="cba8d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="cba8d-139">NOTES</span></span>

## <span data-ttu-id="cba8d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cba8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="cba8d-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="cba8d-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="cba8d-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cba8d-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="cba8d-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="cba8d-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="cba8d-144">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="cba8d-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


