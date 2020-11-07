---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849375"
---
# <span data-ttu-id="1871b-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1871b-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="1871b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1871b-102">SYNOPSIS</span></span>
<span data-ttu-id="1871b-103">Ruft VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="1871b-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1871b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1871b-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1871b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1871b-105">DESCRIPTION</span></span>
<span data-ttu-id="1871b-106">Das Cmdlet " **Get-AzureRmVMImageOffer** " Ruft die VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="1871b-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="1871b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1871b-107">EXAMPLES</span></span>

### <span data-ttu-id="1871b-108">Beispiel 1: Abrufen von Angebotstypen für einen Publisher</span><span class="sxs-lookup"><span data-stu-id="1871b-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="1871b-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Verleger in der zentralen US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="1871b-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="1871b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1871b-110">PARAMETERS</span></span>

### <span data-ttu-id="1871b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1871b-111">-DefaultProfile</span></span>
<span data-ttu-id="1871b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1871b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1871b-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="1871b-113">-Location</span></span>
<span data-ttu-id="1871b-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="1871b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="1871b-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1871b-115">-PublisherName</span></span>
<span data-ttu-id="1871b-116">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="1871b-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="1871b-117">Verwenden Sie zum Abrufen eines Verlegers das Get-AzureRmVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1871b-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1871b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1871b-118">CommonParameters</span></span>
<span data-ttu-id="1871b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1871b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1871b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1871b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1871b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1871b-121">INPUTS</span></span>

### <span data-ttu-id="1871b-122">Keine</span><span class="sxs-lookup"><span data-stu-id="1871b-122">None</span></span>
<span data-ttu-id="1871b-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1871b-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1871b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1871b-124">OUTPUTS</span></span>

### <span data-ttu-id="1871b-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="1871b-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="1871b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1871b-126">NOTES</span></span>

## <span data-ttu-id="1871b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1871b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1871b-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1871b-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="1871b-129">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1871b-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1871b-130">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1871b-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1871b-131">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1871b-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


