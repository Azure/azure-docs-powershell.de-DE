---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 6355ce5cea881f66473ca8d541585187a79fe23e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652129"
---
# <span data-ttu-id="0ca7b-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0ca7b-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="0ca7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ca7b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca7b-103">Ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="0ca7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ca7b-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ca7b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca7b-106">Das Cmdlet " **Get-AzVMImageSku** " ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="0ca7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ca7b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ca7b-108">Beispiel 1: Abrufen von VMImage-SKUs</span><span class="sxs-lookup"><span data-stu-id="0ca7b-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="0ca7b-109">Dieser Befehl ruft die SKUs für den angegebenen Herausgeber und das Angebot ab.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="0ca7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ca7b-110">PARAMETERS</span></span>

### <span data-ttu-id="0ca7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca7b-111">-DefaultProfile</span></span>
<span data-ttu-id="0ca7b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca7b-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="0ca7b-113">-Location</span></span>
<span data-ttu-id="0ca7b-114">Gibt den Speicherort des VMImage an.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="0ca7b-115">-Angebot</span><span class="sxs-lookup"><span data-stu-id="0ca7b-115">-Offer</span></span>
<span data-ttu-id="0ca7b-116">Gibt den Typ des VMImage-Angebots an.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="0ca7b-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0ca7b-117">-PublisherName</span></span>
<span data-ttu-id="0ca7b-118">Gibt den Herausgeber eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="0ca7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca7b-119">CommonParameters</span></span>
<span data-ttu-id="0ca7b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca7b-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ca7b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca7b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ca7b-122">INPUTS</span></span>

### <span data-ttu-id="0ca7b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca7b-123">System.String</span></span>

## <span data-ttu-id="0ca7b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ca7b-124">OUTPUTS</span></span>

### <span data-ttu-id="0ca7b-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="0ca7b-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="0ca7b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ca7b-126">NOTES</span></span>

## <span data-ttu-id="0ca7b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ca7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ca7b-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0ca7b-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0ca7b-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0ca7b-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0ca7b-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0ca7b-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0ca7b-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0ca7b-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


