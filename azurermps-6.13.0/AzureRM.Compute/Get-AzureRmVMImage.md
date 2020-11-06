---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 881f4ba2d9750c9edbcb988ce3d438e062934a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497510"
---
# <span data-ttu-id="fdbae-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fdbae-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="fdbae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdbae-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbae-103">Ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="fdbae-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdbae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdbae-104">SYNTAX</span></span>

### <span data-ttu-id="fdbae-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="fdbae-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdbae-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="fdbae-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdbae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdbae-107">DESCRIPTION</span></span>
<span data-ttu-id="fdbae-108">Das Cmdlet " **Get-AzureRmVMImage** " ruft alle Versionen eines VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="fdbae-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="fdbae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdbae-109">EXAMPLES</span></span>

### <span data-ttu-id="fdbae-110">Beispiel 1: Abrufen von VMImage-Objekten</span><span class="sxs-lookup"><span data-stu-id="fdbae-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"
```

<span data-ttu-id="fdbae-111">Dieser Befehl ruft alle Versionen von VMImage ab, die den angegebenen Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fdbae-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="fdbae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdbae-112">PARAMETERS</span></span>

### <span data-ttu-id="fdbae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbae-113">-DefaultProfile</span></span>
<span data-ttu-id="fdbae-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdbae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="fdbae-115">-FilterExpression</span></span>
<span data-ttu-id="fdbae-116">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="fdbae-117">-Location</span></span>
<span data-ttu-id="fdbae-118">Gibt die Position eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-119">-Angebot</span><span class="sxs-lookup"><span data-stu-id="fdbae-119">-Offer</span></span>
<span data-ttu-id="fdbae-120">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="fdbae-121">Verwenden Sie das Get-AzureRmVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fdbae-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fdbae-122">-PublisherName</span></span>
<span data-ttu-id="fdbae-123">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="fdbae-124">Verwenden Sie das Get-AzureRmVMImagePublisher-Cmdlet, um einen Bildherausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fdbae-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="fdbae-125">-Skus</span></span>
<span data-ttu-id="fdbae-126">Gibt eine VMImage-SKU an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="fdbae-127">Verwenden Sie das Get-AzureRmVMImageSku-Cmdlet, um eine SKU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fdbae-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-128">-Version</span><span class="sxs-lookup"><span data-stu-id="fdbae-128">-Version</span></span>
<span data-ttu-id="fdbae-129">Gibt die Version von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fdbae-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbae-130">CommonParameters</span></span>
<span data-ttu-id="fdbae-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdbae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbae-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdbae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbae-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdbae-133">INPUTS</span></span>

### <span data-ttu-id="fdbae-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fdbae-134">System.String</span></span>

## <span data-ttu-id="fdbae-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdbae-135">OUTPUTS</span></span>

### <span data-ttu-id="fdbae-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="fdbae-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="fdbae-137">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="fdbae-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="fdbae-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdbae-138">NOTES</span></span>

## <span data-ttu-id="fdbae-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdbae-139">RELATED LINKS</span></span>

[<span data-ttu-id="fdbae-140">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fdbae-140">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fdbae-141">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fdbae-141">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fdbae-142">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fdbae-142">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fdbae-143">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fdbae-143">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


