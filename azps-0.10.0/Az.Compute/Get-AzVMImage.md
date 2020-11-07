---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844591"
---
# <span data-ttu-id="f3f2e-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f3f2e-101">Get-AzVMImage</span></span>

## <span data-ttu-id="f3f2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f2e-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="f3f2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3f2e-104">SYNTAX</span></span>

### <span data-ttu-id="f3f2e-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="f3f2e-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3f2e-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="f3f2e-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f2e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f2e-108">Das Cmdlet " **Get-AzVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="f3f2e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3f2e-109">EXAMPLES</span></span>

### <span data-ttu-id="f3f2e-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="f3f2e-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="f3f2e-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="f3f2e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3f2e-112">PARAMETERS</span></span>

### <span data-ttu-id="f3f2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f2e-113">-DefaultProfile</span></span>
<span data-ttu-id="f3f2e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f2e-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="f3f2e-115">-FilterExpression</span></span>
<span data-ttu-id="f3f2e-116">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="f3f2e-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f3f2e-117">-Location</span></span>
<span data-ttu-id="f3f2e-118">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="f3f2e-119">-Angebot</span><span class="sxs-lookup"><span data-stu-id="f3f2e-119">-Offer</span></span>
<span data-ttu-id="f3f2e-120">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="f3f2e-121">Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="f3f2e-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f3f2e-122">-PublisherName</span></span>
<span data-ttu-id="f3f2e-123">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="f3f2e-124">Verwenden Sie das Get-AzVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f3f2e-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="f3f2e-125">-Skus</span></span>
<span data-ttu-id="f3f2e-126">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="f3f2e-127">Verwenden Sie das Get-AzVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f3f2e-128">-Version</span><span class="sxs-lookup"><span data-stu-id="f3f2e-128">-Version</span></span>
<span data-ttu-id="f3f2e-129">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="f3f2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f2e-130">CommonParameters</span></span>
<span data-ttu-id="f3f2e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f2e-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f2e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f2e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3f2e-133">INPUTS</span></span>

### <span data-ttu-id="f3f2e-134">Keine</span><span class="sxs-lookup"><span data-stu-id="f3f2e-134">None</span></span>
<span data-ttu-id="f3f2e-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f3f2e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3f2e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3f2e-136">OUTPUTS</span></span>

### <span data-ttu-id="f3f2e-137">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="f3f2e-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="f3f2e-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="f3f2e-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="f3f2e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3f2e-139">NOTES</span></span>

## <span data-ttu-id="f3f2e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3f2e-140">RELATED LINKS</span></span>

[<span data-ttu-id="f3f2e-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f3f2e-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f3f2e-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f3f2e-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f3f2e-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f3f2e-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f3f2e-144">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f3f2e-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


