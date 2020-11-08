---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177836"
---
# <span data-ttu-id="3703c-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3703c-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="3703c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3703c-102">SYNOPSIS</span></span>
<span data-ttu-id="3703c-103">Ruft VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="3703c-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="3703c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3703c-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3703c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3703c-105">DESCRIPTION</span></span>
<span data-ttu-id="3703c-106">Das Cmdlet " **Get-AzVMImageOffer** " Ruft die VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="3703c-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="3703c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3703c-107">EXAMPLES</span></span>

### <span data-ttu-id="3703c-108">Beispiel 1: Abrufen von Angebotstypen für einen Publisher</span><span class="sxs-lookup"><span data-stu-id="3703c-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="3703c-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Verleger in der zentralen US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="3703c-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="3703c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3703c-110">PARAMETERS</span></span>

### <span data-ttu-id="3703c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3703c-111">-DefaultProfile</span></span>
<span data-ttu-id="3703c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3703c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3703c-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="3703c-113">-Location</span></span>
<span data-ttu-id="3703c-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="3703c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3703c-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3703c-115">-PublisherName</span></span>
<span data-ttu-id="3703c-116">Gibt den Namen des Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="3703c-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="3703c-117">Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3703c-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="3703c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3703c-118">CommonParameters</span></span>
<span data-ttu-id="3703c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3703c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3703c-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3703c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3703c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3703c-121">INPUTS</span></span>

### <span data-ttu-id="3703c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3703c-122">System.String</span></span>

## <span data-ttu-id="3703c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3703c-123">OUTPUTS</span></span>

### <span data-ttu-id="3703c-124">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="3703c-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="3703c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3703c-125">NOTES</span></span>

## <span data-ttu-id="3703c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3703c-126">RELATED LINKS</span></span>

[<span data-ttu-id="3703c-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3703c-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3703c-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3703c-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3703c-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3703c-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="3703c-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3703c-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


