---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850156"
---
# <span data-ttu-id="f1477-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f1477-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="f1477-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1477-102">SYNOPSIS</span></span>
<span data-ttu-id="f1477-103">Ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="f1477-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1477-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1477-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1477-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1477-105">DESCRIPTION</span></span>
<span data-ttu-id="f1477-106">Das Cmdlet " **Get-AzureRmVMImageSku** " ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="f1477-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="f1477-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1477-107">EXAMPLES</span></span>

### <span data-ttu-id="f1477-108">Beispiel 1: Abrufen von VMImage-SKUs</span><span class="sxs-lookup"><span data-stu-id="f1477-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="f1477-109">Dieser Befehl ruft die SKUs für den angegebenen Herausgeber und das Angebot ab.</span><span class="sxs-lookup"><span data-stu-id="f1477-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="f1477-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1477-110">PARAMETERS</span></span>

### <span data-ttu-id="f1477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1477-111">-DefaultProfile</span></span>
<span data-ttu-id="f1477-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1477-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1477-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1477-113">-Location</span></span>
<span data-ttu-id="f1477-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f1477-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f1477-115">-Angebot</span><span class="sxs-lookup"><span data-stu-id="f1477-115">-Offer</span></span>
<span data-ttu-id="f1477-116">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="f1477-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="f1477-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f1477-117">-PublisherName</span></span>
<span data-ttu-id="f1477-118">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f1477-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="f1477-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1477-119">CommonParameters</span></span>
<span data-ttu-id="f1477-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1477-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1477-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1477-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1477-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1477-122">INPUTS</span></span>

### <span data-ttu-id="f1477-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f1477-123">None</span></span>
<span data-ttu-id="f1477-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f1477-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1477-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1477-125">OUTPUTS</span></span>

### <span data-ttu-id="f1477-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="f1477-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="f1477-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1477-127">NOTES</span></span>

## <span data-ttu-id="f1477-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1477-128">RELATED LINKS</span></span>

[<span data-ttu-id="f1477-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f1477-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f1477-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f1477-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f1477-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f1477-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f1477-132">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f1477-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


