---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664686"
---
# <span data-ttu-id="fd7e6-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fd7e6-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="fd7e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e6-103">Ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd7e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7e6-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="fd7e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7e6-106">Das Cmdlet " **Get-AzureRmVMImageSku** " ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="fd7e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd7e6-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7e6-108">Beispiel 1: Abrufen von VMImage-SKUs</span><span class="sxs-lookup"><span data-stu-id="fd7e6-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="fd7e6-109">Dieser Befehl ruft die SKUs für den angegebenen Herausgeber und das Angebot ab.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="fd7e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7e6-110">PARAMETERS</span></span>

### <span data-ttu-id="fd7e6-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd7e6-111">-Location</span></span>
<span data-ttu-id="fd7e6-112">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="fd7e6-113">-Angebot</span><span class="sxs-lookup"><span data-stu-id="fd7e6-113">-Offer</span></span>
<span data-ttu-id="fd7e6-114">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="fd7e6-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="fd7e6-115">-PublisherName</span></span>
<span data-ttu-id="fd7e6-116">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="fd7e6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e6-117">CommonParameters</span></span>
<span data-ttu-id="fd7e6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e6-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7e6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e6-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd7e6-120">INPUTS</span></span>

### <span data-ttu-id="fd7e6-121">Keine</span><span class="sxs-lookup"><span data-stu-id="fd7e6-121">None</span></span>
<span data-ttu-id="fd7e6-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd7e6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd7e6-123">OUTPUTS</span></span>

## <span data-ttu-id="fd7e6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd7e6-124">NOTES</span></span>

## <span data-ttu-id="fd7e6-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd7e6-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd7e6-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fd7e6-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fd7e6-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fd7e6-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fd7e6-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fd7e6-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="fd7e6-129">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fd7e6-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


