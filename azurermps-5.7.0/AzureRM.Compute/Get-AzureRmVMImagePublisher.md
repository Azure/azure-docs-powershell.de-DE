---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664685"
---
# <span data-ttu-id="8c199-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8c199-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="8c199-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c199-102">SYNOPSIS</span></span>
<span data-ttu-id="8c199-103">Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="8c199-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c199-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c199-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## <span data-ttu-id="8c199-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c199-105">DESCRIPTION</span></span>
<span data-ttu-id="8c199-106">Das Cmdlet " **Get-AzureRmVMImagePublisher** " Ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="8c199-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="8c199-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c199-107">EXAMPLES</span></span>

### <span data-ttu-id="8c199-108">Beispiel 1: Abrufen von VMImage-Verlegern für eine Region</span><span class="sxs-lookup"><span data-stu-id="8c199-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="8c199-109">Dieser Befehl ruft die Herausgeber von VMImage-Instanzen für die zentrale US-Region innerhalb Ihres Azure-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="8c199-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="8c199-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c199-110">PARAMETERS</span></span>

### <span data-ttu-id="8c199-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="8c199-111">-Location</span></span>
<span data-ttu-id="8c199-112">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="8c199-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="8c199-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c199-113">CommonParameters</span></span>
<span data-ttu-id="8c199-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c199-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c199-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c199-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c199-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c199-116">INPUTS</span></span>

### <span data-ttu-id="8c199-117">Keine</span><span class="sxs-lookup"><span data-stu-id="8c199-117">None</span></span>
<span data-ttu-id="8c199-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8c199-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c199-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c199-119">OUTPUTS</span></span>

## <span data-ttu-id="8c199-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c199-120">NOTES</span></span>

## <span data-ttu-id="8c199-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c199-121">RELATED LINKS</span></span>

[<span data-ttu-id="8c199-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8c199-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8c199-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8c199-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8c199-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8c199-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8c199-125">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8c199-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


