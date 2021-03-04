---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 551774d61e7887dfe115f37f67ce66fe95147406
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922107"
---
# <span data-ttu-id="836c7-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="836c7-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="836c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="836c7-102">SYNOPSIS</span></span>
<span data-ttu-id="836c7-103">Ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="836c7-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="836c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="836c7-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="836c7-105">DESCRIPTION</span></span>
<span data-ttu-id="836c7-106">Das **Get-AzVMExtensionImageType-Cmdlet** ruft den Typ einer Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="836c7-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="836c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="836c7-107">EXAMPLES</span></span>

### <span data-ttu-id="836c7-108">Beispiel 1: Erhalten eines Erweiterungsbildtyps</span><span class="sxs-lookup"><span data-stu-id="836c7-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="836c7-109">Dieser Befehl ruft den Erweiterungsbildtyp für den angegebenen Herausgeber und Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="836c7-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="836c7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="836c7-110">PARAMETERS</span></span>

### <span data-ttu-id="836c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836c7-111">-DefaultProfile</span></span>
<span data-ttu-id="836c7-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="836c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="836c7-113">-Location</span><span class="sxs-lookup"><span data-stu-id="836c7-113">-Location</span></span>
<span data-ttu-id="836c7-114">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="836c7-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="836c7-115">Dieses Cmdlet ruft den Typ für eine Erweiterung an der von diesem Parameter angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="836c7-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="836c7-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="836c7-116">-PublisherName</span></span>
<span data-ttu-id="836c7-117">Gibt den Namen eines Herausgebers einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="836c7-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="836c7-118">Verwenden Sie zum Abrufen eines Erweiterungsherausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="836c7-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="836c7-119">Dieses Cmdlet ruft den Typ für eine Erweiterung vom Herausgeber ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="836c7-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="836c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836c7-120">CommonParameters</span></span>
<span data-ttu-id="836c7-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836c7-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="836c7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836c7-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="836c7-123">INPUTS</span></span>

### <span data-ttu-id="836c7-124">System.String</span><span class="sxs-lookup"><span data-stu-id="836c7-124">System.String</span></span>

## <span data-ttu-id="836c7-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="836c7-125">OUTPUTS</span></span>

### <span data-ttu-id="836c7-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="836c7-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="836c7-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="836c7-127">NOTES</span></span>

## <span data-ttu-id="836c7-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="836c7-128">RELATED LINKS</span></span>

[<span data-ttu-id="836c7-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="836c7-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="836c7-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="836c7-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


