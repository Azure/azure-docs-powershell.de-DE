---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503854"
---
# <span data-ttu-id="8cf0f-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8cf0f-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="8cf0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cf0f-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf0f-103">Ruft VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cf0f-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="8cf0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cf0f-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf0f-106">Das Cmdlet " **Get-AzureRmVMImageOffer** " Ruft die VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="8cf0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cf0f-107">EXAMPLES</span></span>

### <span data-ttu-id="8cf0f-108">Beispiel 1: Abrufen von Angebotstypen für einen Publisher</span><span class="sxs-lookup"><span data-stu-id="8cf0f-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="8cf0f-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Verleger in der zentralen US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="8cf0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cf0f-110">PARAMETERS</span></span>

### <span data-ttu-id="8cf0f-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="8cf0f-111">-Location</span></span>
<span data-ttu-id="8cf0f-112">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="8cf0f-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8cf0f-113">-PublisherName</span></span>
<span data-ttu-id="8cf0f-114">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="8cf0f-115">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8cf0f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf0f-116">CommonParameters</span></span>
<span data-ttu-id="8cf0f-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf0f-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf0f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf0f-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cf0f-119">INPUTS</span></span>

### <span data-ttu-id="8cf0f-120">Keine</span><span class="sxs-lookup"><span data-stu-id="8cf0f-120">None</span></span>
<span data-ttu-id="8cf0f-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8cf0f-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cf0f-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cf0f-122">OUTPUTS</span></span>

## <span data-ttu-id="8cf0f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cf0f-123">NOTES</span></span>

## <span data-ttu-id="8cf0f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cf0f-124">RELATED LINKS</span></span>

[<span data-ttu-id="8cf0f-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8cf0f-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8cf0f-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8cf0f-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8cf0f-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8cf0f-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8cf0f-128">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8cf0f-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


