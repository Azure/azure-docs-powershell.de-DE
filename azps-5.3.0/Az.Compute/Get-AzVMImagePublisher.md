---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473104"
---
# <span data-ttu-id="f9973-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f9973-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="f9973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9973-102">SYNOPSIS</span></span>
<span data-ttu-id="f9973-103">Ruft die HERAUSGEBER von VMImage ab.</span><span class="sxs-lookup"><span data-stu-id="f9973-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="f9973-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9973-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9973-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9973-105">DESCRIPTION</span></span>
<span data-ttu-id="f9973-106">Das **Cmdlet "Get-AzVMImagePublisher"** ruft die VMImage-Herausgeber ab.</span><span class="sxs-lookup"><span data-stu-id="f9973-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="f9973-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9973-107">EXAMPLES</span></span>

### <span data-ttu-id="f9973-108">Beispiel 1: Erhalten von VMImage-Herausgebern für eine Region</span><span class="sxs-lookup"><span data-stu-id="f9973-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="f9973-109">Dieser Befehl ruft die Herausgeber von "VMImage"-Instanzen für die Region "Usa, Mitte" in Ihrem Azure-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="f9973-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="f9973-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9973-110">PARAMETERS</span></span>

### <span data-ttu-id="f9973-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9973-111">-DefaultProfile</span></span>
<span data-ttu-id="f9973-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9973-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9973-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f9973-113">-Location</span></span>
<span data-ttu-id="f9973-114">Gibt den Speicherort von VMImage an.</span><span class="sxs-lookup"><span data-stu-id="f9973-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="f9973-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9973-115">CommonParameters</span></span>
<span data-ttu-id="f9973-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9973-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9973-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9973-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9973-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9973-118">INPUTS</span></span>

### <span data-ttu-id="f9973-119">System.String</span><span class="sxs-lookup"><span data-stu-id="f9973-119">System.String</span></span>

## <span data-ttu-id="f9973-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9973-120">OUTPUTS</span></span>

### <span data-ttu-id="f9973-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f9973-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="f9973-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f9973-122">NOTES</span></span>

## <span data-ttu-id="f9973-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f9973-123">RELATED LINKS</span></span>

[<span data-ttu-id="f9973-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f9973-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f9973-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f9973-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f9973-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f9973-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f9973-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f9973-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


