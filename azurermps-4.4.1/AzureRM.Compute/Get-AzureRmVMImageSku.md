---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5bdce17c963cc2529fab3f328b9ab64cc549e1d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665403"
---
# <span data-ttu-id="f5ca8-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f5ca8-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="f5ca8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ca8-103">Ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ca8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5ca8-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ca8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ca8-106">Das Cmdlet " **Get-AzureRmVMImageSku** " ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="f5ca8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ca8-108">Beispiel 1: Abrufen von VMImage-SKUs</span><span class="sxs-lookup"><span data-stu-id="f5ca8-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="f5ca8-109">Dieser Befehl ruft die SKUs für den angegebenen Herausgeber und das Angebot ab.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="f5ca8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5ca8-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ca8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ca8-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ca8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5ca8-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5ca8-113">-Location</span></span>
<span data-ttu-id="f5ca8-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f5ca8-115">-Angebot</span><span class="sxs-lookup"><span data-stu-id="f5ca8-115">-Offer</span></span>
<span data-ttu-id="f5ca8-116">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="f5ca8-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f5ca8-117">-PublisherName</span></span>
<span data-ttu-id="f5ca8-118">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="f5ca8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ca8-119">CommonParameters</span></span>
<span data-ttu-id="f5ca8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ca8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ca8-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ca8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ca8-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5ca8-122">INPUTS</span></span>

## <span data-ttu-id="f5ca8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5ca8-123">OUTPUTS</span></span>

## <span data-ttu-id="f5ca8-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5ca8-124">NOTES</span></span>

## <span data-ttu-id="f5ca8-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5ca8-125">RELATED LINKS</span></span>

[<span data-ttu-id="f5ca8-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f5ca8-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f5ca8-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f5ca8-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f5ca8-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f5ca8-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f5ca8-129">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f5ca8-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


