---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290765"
---
# <span data-ttu-id="9e571-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9e571-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="9e571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e571-102">SYNOPSIS</span></span>
<span data-ttu-id="9e571-103">Ruft die Angebote von VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="9e571-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="9e571-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e571-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e571-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e571-105">DESCRIPTION</span></span>
<span data-ttu-id="9e571-106">Das **Cmdlet "Get-AzVMImageOffer"** ruft die "VMImage"-Angebotstypen ab.</span><span class="sxs-lookup"><span data-stu-id="9e571-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="9e571-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e571-107">EXAMPLES</span></span>

### <span data-ttu-id="9e571-108">Beispiel 1: Erhalten von Angebotstypen für einen Herausgeber</span><span class="sxs-lookup"><span data-stu-id="9e571-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9e571-109">Dieser Befehl ruft die Angebotstypen für den angegebenen Herausgeber in der Region "USA, Mitte" ab.</span><span class="sxs-lookup"><span data-stu-id="9e571-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="9e571-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e571-110">PARAMETERS</span></span>

### <span data-ttu-id="9e571-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e571-111">-DefaultProfile</span></span>
<span data-ttu-id="9e571-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e571-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e571-113">-Location</span><span class="sxs-lookup"><span data-stu-id="9e571-113">-Location</span></span>
<span data-ttu-id="9e571-114">Gibt den Speicherort von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="9e571-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9e571-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9e571-115">-PublisherName</span></span>
<span data-ttu-id="9e571-116">Gibt den Namen eines Herausgebers eines VMImage an.</span><span class="sxs-lookup"><span data-stu-id="9e571-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9e571-117">Verwenden Sie zum Abrufen eines Herausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e571-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9e571-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e571-118">CommonParameters</span></span>
<span data-ttu-id="9e571-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e571-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e571-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e571-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e571-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e571-121">INPUTS</span></span>

### <span data-ttu-id="9e571-122">System.String</span><span class="sxs-lookup"><span data-stu-id="9e571-122">System.String</span></span>

## <span data-ttu-id="9e571-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e571-123">OUTPUTS</span></span>

### <span data-ttu-id="9e571-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="9e571-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="9e571-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e571-125">NOTES</span></span>

## <span data-ttu-id="9e571-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e571-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e571-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9e571-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9e571-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9e571-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9e571-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9e571-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9e571-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9e571-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


