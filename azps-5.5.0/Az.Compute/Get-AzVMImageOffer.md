---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166532"
---
# <span data-ttu-id="d89f1-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d89f1-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="d89f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d89f1-103">Ruft die Angebote von VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="d89f1-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="d89f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d89f1-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d89f1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d89f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d89f1-106">Das **Cmdlet "Get-AzVMImageOffer"** ruft die "VMImage"-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="d89f1-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="d89f1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d89f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d89f1-108">Beispiel 1: Erhalten von Angebotstypen für einen Herausgeber</span><span class="sxs-lookup"><span data-stu-id="d89f1-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="d89f1-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Herausgeber in der Region "USA, Mitte" ab.</span><span class="sxs-lookup"><span data-stu-id="d89f1-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="d89f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d89f1-110">PARAMETERS</span></span>

### <span data-ttu-id="d89f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89f1-111">-DefaultProfile</span></span>
<span data-ttu-id="d89f1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d89f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89f1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d89f1-113">-Location</span></span>
<span data-ttu-id="d89f1-114">Gibt den Speicherort von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="d89f1-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d89f1-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d89f1-115">-PublisherName</span></span>
<span data-ttu-id="d89f1-116">Gibt den Namen eines Herausgebers eines VMImages an.</span><span class="sxs-lookup"><span data-stu-id="d89f1-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d89f1-117">Verwenden Sie zum Abrufen eines Herausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d89f1-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d89f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89f1-118">CommonParameters</span></span>
<span data-ttu-id="d89f1-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89f1-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d89f1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89f1-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d89f1-121">INPUTS</span></span>

### <span data-ttu-id="d89f1-122">System.String</span><span class="sxs-lookup"><span data-stu-id="d89f1-122">System.String</span></span>

## <span data-ttu-id="d89f1-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d89f1-123">OUTPUTS</span></span>

### <span data-ttu-id="d89f1-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="d89f1-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="d89f1-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d89f1-125">NOTES</span></span>

## <span data-ttu-id="d89f1-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d89f1-126">RELATED LINKS</span></span>

[<span data-ttu-id="d89f1-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d89f1-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d89f1-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d89f1-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d89f1-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d89f1-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d89f1-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d89f1-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


