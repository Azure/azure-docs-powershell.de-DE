---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 94556ce0b78b90ae9c418aee175f090e9209adb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949520"
---
# <span data-ttu-id="0030c-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0030c-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="0030c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0030c-102">SYNOPSIS</span></span>
<span data-ttu-id="0030c-103">Ruft VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="0030c-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="0030c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0030c-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0030c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0030c-105">DESCRIPTION</span></span>
<span data-ttu-id="0030c-106">Das **Cmdlet Get-AzVMImageOffer** ruft die VMImage-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="0030c-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="0030c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0030c-107">EXAMPLES</span></span>

### <span data-ttu-id="0030c-108">Beispiel 1: Erhalten von Angebotstypen für einen Herausgeber</span><span class="sxs-lookup"><span data-stu-id="0030c-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="0030c-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Herausgeber in der Region "Usa, Mitte" ab.</span><span class="sxs-lookup"><span data-stu-id="0030c-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="0030c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0030c-110">PARAMETERS</span></span>

### <span data-ttu-id="0030c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0030c-111">-DefaultProfile</span></span>
<span data-ttu-id="0030c-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0030c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0030c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0030c-113">-Location</span></span>
<span data-ttu-id="0030c-114">Gibt den Speicherort des VMImages an.</span><span class="sxs-lookup"><span data-stu-id="0030c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="0030c-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0030c-115">-PublisherName</span></span>
<span data-ttu-id="0030c-116">Gibt den Namen eines Herausgebers eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="0030c-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0030c-117">Verwenden Sie das cmdlet Get-AzVMImagePublisher, um einen Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0030c-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0030c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0030c-118">CommonParameters</span></span>
<span data-ttu-id="0030c-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0030c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0030c-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0030c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0030c-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0030c-121">INPUTS</span></span>

### <span data-ttu-id="0030c-122">System.String</span><span class="sxs-lookup"><span data-stu-id="0030c-122">System.String</span></span>

## <span data-ttu-id="0030c-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0030c-123">OUTPUTS</span></span>

### <span data-ttu-id="0030c-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="0030c-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="0030c-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0030c-125">NOTES</span></span>

## <span data-ttu-id="0030c-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0030c-126">RELATED LINKS</span></span>

[<span data-ttu-id="0030c-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0030c-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0030c-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0030c-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0030c-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0030c-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0030c-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0030c-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


