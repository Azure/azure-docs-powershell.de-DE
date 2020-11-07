---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844580"
---
# <span data-ttu-id="f659f-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f659f-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="f659f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f659f-102">SYNOPSIS</span></span>
<span data-ttu-id="f659f-103">Ruft VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="f659f-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="f659f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f659f-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f659f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f659f-105">DESCRIPTION</span></span>
<span data-ttu-id="f659f-106">Das Cmdlet " **Get-AzVMImageOffer** " Ruft die VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="f659f-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="f659f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f659f-107">EXAMPLES</span></span>

### <span data-ttu-id="f659f-108">Beispiel 1: Abrufen von Angebotstypen für einen Publisher</span><span class="sxs-lookup"><span data-stu-id="f659f-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="f659f-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Verleger in der zentralen US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="f659f-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="f659f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f659f-110">PARAMETERS</span></span>

### <span data-ttu-id="f659f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f659f-111">-DefaultProfile</span></span>
<span data-ttu-id="f659f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f659f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f659f-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="f659f-113">-Location</span></span>
<span data-ttu-id="f659f-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f659f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f659f-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f659f-115">-PublisherName</span></span>
<span data-ttu-id="f659f-116">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f659f-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f659f-117">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f659f-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f659f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f659f-118">CommonParameters</span></span>
<span data-ttu-id="f659f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f659f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f659f-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f659f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f659f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f659f-121">INPUTS</span></span>

### <span data-ttu-id="f659f-122">Keine</span><span class="sxs-lookup"><span data-stu-id="f659f-122">None</span></span>
<span data-ttu-id="f659f-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f659f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f659f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f659f-124">OUTPUTS</span></span>

### <span data-ttu-id="f659f-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="f659f-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="f659f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f659f-126">NOTES</span></span>

## <span data-ttu-id="f659f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f659f-127">RELATED LINKS</span></span>

[<span data-ttu-id="f659f-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f659f-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f659f-129">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f659f-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f659f-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f659f-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f659f-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f659f-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


