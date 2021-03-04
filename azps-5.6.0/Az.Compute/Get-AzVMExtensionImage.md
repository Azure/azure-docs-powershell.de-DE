---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ce726675946b2b8dc40feb82a529ccf27ccef443
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949528"
---
# <span data-ttu-id="51d3b-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="51d3b-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="51d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="51d3b-103">Ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="51d3b-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="51d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51d3b-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="51d3b-106">Das **Get-AzVMExtensionImage-Cmdlet** ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="51d3b-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="51d3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="51d3b-108">Beispiel 1: Erhalten der Versionen eines Erweiterungsbilds</span><span class="sxs-lookup"><span data-stu-id="51d3b-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="51d3b-109">Dieser Befehl ruft alle Versionen des Erweiterungsbilds für den angegebenen Speicherort, Herausgeber und Typ ab.</span><span class="sxs-lookup"><span data-stu-id="51d3b-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="51d3b-110">Beispiel 2: Holen Sie sich die Versionen eines Erweiterungsbilds mit Filter über version.</span><span class="sxs-lookup"><span data-stu-id="51d3b-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="51d3b-111">Dieser Befehl ruft ab 12 alle Versionen des Erweiterungsbilds für den angegebenen Speicherort, Herausgeber, Typ und Version ab.</span><span class="sxs-lookup"><span data-stu-id="51d3b-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="51d3b-112">Beispiel 3: Holen Sie sich die Versionen eines Erweiterungsbilds mit Filter über version</span><span class="sxs-lookup"><span data-stu-id="51d3b-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="51d3b-113">Dieser Befehl ruft alle Versionen des Erweiterungsabbilds für den angegebenen Speicherort, Herausgeber, Typ und Version ab.</span><span class="sxs-lookup"><span data-stu-id="51d3b-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="51d3b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="51d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="51d3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d3b-115">-DefaultProfile</span></span>
<span data-ttu-id="51d3b-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51d3b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51d3b-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="51d3b-117">-FilterExpression</span></span>
<span data-ttu-id="51d3b-118">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="51d3b-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d3b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="51d3b-119">-Location</span></span>
<span data-ttu-id="51d3b-120">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="51d3b-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="51d3b-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="51d3b-121">-PublisherName</span></span>
<span data-ttu-id="51d3b-122">Gibt den Namen eines Erweiterungsherausgebers an.</span><span class="sxs-lookup"><span data-stu-id="51d3b-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="51d3b-123">Verwenden Sie zum Abrufen eines Erweiterungsherausgebers das Get-AzVMImagePublisher Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51d3b-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="51d3b-124">-Type</span><span class="sxs-lookup"><span data-stu-id="51d3b-124">-Type</span></span>
<span data-ttu-id="51d3b-125">Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="51d3b-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="51d3b-126">Verwenden Sie zum Abrufen eines Erweiterungstyps das Get-AzVMExtensionImageType Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51d3b-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="51d3b-127">-Version</span><span class="sxs-lookup"><span data-stu-id="51d3b-127">-Version</span></span>
<span data-ttu-id="51d3b-128">Gibt die Version der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="51d3b-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="51d3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d3b-129">CommonParameters</span></span>
<span data-ttu-id="51d3b-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51d3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d3b-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51d3b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d3b-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51d3b-132">INPUTS</span></span>

### <span data-ttu-id="51d3b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51d3b-133">System.String</span></span>

## <span data-ttu-id="51d3b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51d3b-134">OUTPUTS</span></span>

### <span data-ttu-id="51d3b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="51d3b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="51d3b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="51d3b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="51d3b-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="51d3b-137">NOTES</span></span>

## <span data-ttu-id="51d3b-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="51d3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="51d3b-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="51d3b-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="51d3b-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="51d3b-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="51d3b-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="51d3b-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


