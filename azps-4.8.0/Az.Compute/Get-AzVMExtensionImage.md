---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010022"
---
# <span data-ttu-id="a5d3a-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a5d3a-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="a5d3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d3a-103">Ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="a5d3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5d3a-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d3a-106">Das Cmdlet " **Get-AzVMExtensionImage** " ruft alle Versionen für eine Azure-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="a5d3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5d3a-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d3a-108">Beispiel 1: Abrufen der Versionen eines Erweiterungs Bilds</span><span class="sxs-lookup"><span data-stu-id="a5d3a-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="a5d3a-109">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, Herausgeber und Typ ab.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="a5d3a-110">Beispiel 2: Abrufen der Versionen eines Erweiterungs Bilds mit Filter über Version</span><span class="sxs-lookup"><span data-stu-id="a5d3a-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="a5d3a-111">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, den Herausgeber, den Typ und die Version ab, die mit 12 beginnen.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="a5d3a-112">Beispiel 3: Abrufen der Versionen eines Erweiterungs Bilds mit Filter über Version</span><span class="sxs-lookup"><span data-stu-id="a5d3a-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="a5d3a-113">Dieser Befehl ruft alle Versionen des Erweiterungs Bilds für den angegebenen Speicherort, Herausgeber, Typ und Version ab.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="a5d3a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5d3a-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d3a-115">-DefaultProfile</span></span>
<span data-ttu-id="a5d3a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d3a-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="a5d3a-117">-FilterExpression</span></span>
<span data-ttu-id="a5d3a-118">Gibt einen Filterausdruck an.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="a5d3a-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="a5d3a-119">-Location</span></span>
<span data-ttu-id="a5d3a-120">Gibt den Speicherort einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="a5d3a-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a5d3a-121">-PublisherName</span></span>
<span data-ttu-id="a5d3a-122">Gibt den Namen eines Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="a5d3a-123">Verwenden Sie zum Abrufen eines Erweiterungs Herausgebers das Get-AzVMImagePublisher-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a5d3a-124">-Typ</span><span class="sxs-lookup"><span data-stu-id="a5d3a-124">-Type</span></span>
<span data-ttu-id="a5d3a-125">Gibt den Typ der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="a5d3a-126">Verwenden Sie zum Abrufen eines Erweiterungstyps das Get-AzVMExtensionImageType-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="a5d3a-127">-Version</span><span class="sxs-lookup"><span data-stu-id="a5d3a-127">-Version</span></span>
<span data-ttu-id="a5d3a-128">Gibt die Version der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a5d3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d3a-129">CommonParameters</span></span>
<span data-ttu-id="a5d3a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d3a-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5d3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d3a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5d3a-132">INPUTS</span></span>

### <span data-ttu-id="a5d3a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d3a-133">System.String</span></span>

## <span data-ttu-id="a5d3a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5d3a-134">OUTPUTS</span></span>

### <span data-ttu-id="a5d3a-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a5d3a-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="a5d3a-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="a5d3a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="a5d3a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5d3a-137">NOTES</span></span>

## <span data-ttu-id="a5d3a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5d3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="a5d3a-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a5d3a-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="a5d3a-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a5d3a-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a5d3a-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a5d3a-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


