---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303107"
---
# <span data-ttu-id="466ab-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="466ab-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="466ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="466ab-102">SYNOPSIS</span></span>
<span data-ttu-id="466ab-103">Ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="466ab-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="466ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="466ab-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="466ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="466ab-105">DESCRIPTION</span></span>
<span data-ttu-id="466ab-106">Das **Cmdlet "Get-AzVMImageSku"** ruft VMImage-SKUs ab.</span><span class="sxs-lookup"><span data-stu-id="466ab-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="466ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="466ab-107">EXAMPLES</span></span>

### <span data-ttu-id="466ab-108">Beispiel 1: Erhalten von VMImage-SKUs</span><span class="sxs-lookup"><span data-stu-id="466ab-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="466ab-109">Dieser Befehl ruft die SKUs für den angegebenen Herausgeber und das angegebene Angebot ab.</span><span class="sxs-lookup"><span data-stu-id="466ab-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="466ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="466ab-110">PARAMETERS</span></span>

### <span data-ttu-id="466ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466ab-111">-DefaultProfile</span></span>
<span data-ttu-id="466ab-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="466ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="466ab-113">-Location</span><span class="sxs-lookup"><span data-stu-id="466ab-113">-Location</span></span>
<span data-ttu-id="466ab-114">Gibt den Speicherort von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="466ab-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="466ab-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="466ab-115">-Offer</span></span>
<span data-ttu-id="466ab-116">Gibt den Typ des Angebots "VMImage" an.</span><span class="sxs-lookup"><span data-stu-id="466ab-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="466ab-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="466ab-117">-PublisherName</span></span>
<span data-ttu-id="466ab-118">Gibt den Herausgeber einer VMImage an.</span><span class="sxs-lookup"><span data-stu-id="466ab-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="466ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466ab-119">CommonParameters</span></span>
<span data-ttu-id="466ab-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466ab-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="466ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466ab-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="466ab-122">INPUTS</span></span>

### <span data-ttu-id="466ab-123">System.String</span><span class="sxs-lookup"><span data-stu-id="466ab-123">System.String</span></span>

## <span data-ttu-id="466ab-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="466ab-124">OUTPUTS</span></span>

### <span data-ttu-id="466ab-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="466ab-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="466ab-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="466ab-126">NOTES</span></span>

## <span data-ttu-id="466ab-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="466ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="466ab-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="466ab-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="466ab-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="466ab-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="466ab-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="466ab-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="466ab-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="466ab-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


